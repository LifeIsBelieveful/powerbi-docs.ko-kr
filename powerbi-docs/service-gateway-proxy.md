---
title: 온-프레미스 데이터 게이트웨이에 대한 프록시 설정 구성
description: 온-프레미스 데이터 게이트웨이에 대한 프록시 설정의 구성과 관련된 정보.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: conceptual
ms.date: 11/21/2017
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: 2122ce9bd6eb850a51a06188ca1c10faf78f4bb1
ms.sourcegitcommit: ac63b08a4085de35e1968fa90f2f49ea001b50c5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/18/2019
ms.locfileid: "57964666"
---
# <a name="configuring-proxy-settings-for-the-on-premises-data-gateway"></a>온-프레미스 데이터 게이트웨이에 대한 프록시 설정 구성
작업 환경은 인터넷에 액세스하도록 프록시를 통과해야 합니다. 온-프레미스 데이터 게이트웨이가 서비스에 연결되지 못하도록 할 수 있습니다.

## <a name="does-your-network-use-a-proxy"></a>네트워크에서 프록시를 사용합니까?
superuser.com의 다음 게시물은 네트워크에 프록시가 있는지 확인하도록 시도할 수 있는 방법을 설명합니다.

[사용하고 있는 프록시 서버를 어떻게 알 수 있습니까? (SuperUser.com)](https://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using)

## <a name="configuration-file-location-and-default-configuration"></a>구성 파일 위치 및 기본 구성
프록시 정보는 .NET 구성 파일 내에서 구성됩니다. 위치 및 파일 이름은 사용하고 있는 게이트웨이에 따라 달라질 수 있습니다.

### <a name="on-premises-data-gateway"></a>온-프레미스 데이터 게이트웨이
온-프레미스 데이터 게이트웨이와 관련된 두 가지 주요 구성 파일이 있습니다.

**구성**

첫 번째는 실제로 게이트웨이를 구성하는 구성 화면에 대한 것입니다. 게이트웨이를 구성하는 데 문제가 있는 경우 확인할 수 있는 파일입니다.

    C:\Program Files\On-premises data gateway\enterprisegatewayconfigurator.exe.config

**Windows 서비스**

두 번째는 Power BI 서비스와 상호 작용하고 요청을 처리하는 실제 Windows 서비스입니다.

    C:\Program Files\On-premises data gateway\Microsoft.PowerBI.EnterpriseGateway.exe.config

## <a name="configuring-proxy-settings"></a>프록시 설정 구성
기본 프록시 구성은 다음입니다.

```
<system.net>
    <defaultProxy useDefaultCredentials="true" />
</system.net>
```


기본 구성은 Windows 인증과 함께 작동합니다. 프록시가 다른 형식의 인증을 사용하는 경우 설정을 변경해야 합니다. 확실하지 않은 경우 네트워크 관리자에게 문의해야 합니다. 기본 프록시 인증은 권장되지 않으며, 기본 프록시 인증을 사용하려고 하면 게이트웨이가 제대로 구성되지 않는 프록시 인증 오류가 발생할 수 있습니다. 이 문제를 해결하려면 더 강력한 프록시 인증 메커니즘을 사용하세요.

기본 자격 증명을 사용하는 것 외에도 <proxy> 요소를 추가하여 프록시 서버 설정을 자세히 정의할 수 있습니다. 예를 들어 온-프레미스 데이터 게이트웨이가 bypassonlocal 매개 변수를 false로 설정하여 로컬 리소스에 대해서도 프록시를 사용하도록 지정할 수 있습니다. 그러면 프록시 로그 파일의 온-프레미스 데이터 게이트웨이에서 발생한 모든 https 요청을 추적하려는 경우 상황의 문제를 해결하는 데 도움이 됩니다. 다음 샘플 구성은 모든 IP 주소가 192.168.1.10인 특정 프록시를 통해 요청이 이동하도록 지정합니다.

```
<system.net>
    <defaultProxy useDefaultCredentials="true">
        <proxy  
            autoDetect="false"  
            proxyaddress="http://192.168.1.10:3128"  
            bypassonlocal="false"  
            usesystemdefault="true"
        />  
    </defaultProxy>
</system.net>
```

또한, 게이트웨이에서 프록시를 통해 클라우드 데이터 원본에 연결하려면 *C:\Program Files\On-premises data gateway\Microsoft.Mashup.Container.NetFX45.exe* 파일을 업데이트합니다. 파일에서 아래 콘텐츠가 포함되도록 `<configurations>` 섹션을 확장하고 `proxyaddress` 특성을 프록시 정보로 업데이트합니다. 다음 예제에서는 IP 주소가 192.168.1.10인 특정 프록시를 통해 모든 클라우드 요청을 라우팅합니다.

```
<configuration>
<system.net>
    <defaultProxy useDefaultCredentials="true" enabled="true">
    <proxy proxyaddress=""http://192.168.1.10:3128" bypassonlocal="true" />
    </defaultProxy>
</system.net>
</configuration>
```

.NET 구성 파일에 대한 프록시 요소의 구성에 대해 자세히 알아보려면 [defaultProxy 요소(네트워크 설정)](https://msdn.microsoft.com/library/kd3cf2ex.aspx)를 참조하세요.

## <a name="changing-the-gateway-service-account-to-a-domain-user"></a>게이트웨이 서비스 계정을 도메인 사용자로 변경
위의 설명처럼, 기본 자격 증명을 사용하도록 프록시 설정을 구성하는 경우, 프록시 인증 문제가 발생할 수 있습니다. 이것은 기본 서비스 계정이 인증된 도메인 사용자가 아니라 서비스 SID이기 때문입니다. 프록시와의 적절한 인증을 허용하도록 게이트웨이의 서비스 계정을 변경할 수 있습니다.

> [!NOTE]
> 관리 서비스 계정을 사용하여 암호를 재설정할 필요가 없도록 하는 것이 좋습니다. Active Directory 내에서 [관리 서비스 계정](https://technet.microsoft.com/library/dd548356.aspx)을 만드는 방법을 알아보세요.
> 
> 

### <a name="change-the-on-premises-data-gateway-service-account"></a>온-프레미스 데이터 게이트웨이 서비스 계정 변경
1. **온-프레미스 데이터 게이트웨이 서비스**에 대한 Windows 서비스 계정을 변경합니다.

    이 서비스에 대한 기본 계정은 *NT SERVICE\PBIEgwService*입니다. 이것을 Active Directory 도메인에 속하는 도메인 사용자 계정으로 변경합니다. 또는 관리 서비스 계정을 사용하여 암호를 변경할 필요가 없도록 합니다.

    Windows 서비스의 속성 내에 있는 **로그온** 탭에서 계정을 변경합니다.
2. **온-프레미스 데이터 게이트웨이 서비스**를 다시 시작합니다.

    관리자 명령 프롬프트에서, 다음 명령을 실행합니다.

        net stop PBIEgwService

        net start PBIEgwService
3. **온-프레미스 데이터 게이트웨이 서비스 구성기**를 시작합니다. Windows 시작 단추를 선택하고 ‘온-프레미스 데이터 게이트웨이’를 검색합니다.
4. Power BI에 로그인합니다.
5. 복구 키를 사용하여 게이트웨이를 복원합니다.

    이렇게 하면 새 서비스 계정이 데이터 원본에 대해 저장된 자격 증명을 해독할 수 있습니다.

> [!NOTE]
> 서비스 제어판을 사용하여 서비스 계정을 직접 변경하면 ACL이 자동으로 업데이트되지 않습니다. 새 서비스 계정에 설치 파일 및 폴더에 대한 액세스 권한이 있는지 확인해야 합니다. C:\Program Files\On-premises data gateway에서 게이트웨이 설치 폴더를 찾을 수 있습니다. 
> 

## <a name="next-steps"></a>다음 단계
[온-프레미스 데이터 게이트웨이(개인 모드)](service-gateway-personal-mode.md)
[방화벽 정보](service-gateway-onprem-tshoot.md#firewall-or-proxy)  
궁금한 점이 더 있나요? [Power BI 커뮤니티를 이용하세요.](http://community.powerbi.com/)

