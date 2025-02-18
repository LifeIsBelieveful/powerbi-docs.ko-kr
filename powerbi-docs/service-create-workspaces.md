---
title: Power BI에서 클래식 작업 영역 만들기
description: 작업 영역에서 대시보드, 보고서 및 조직에 대 한 주요 메트릭을 제공 하도록 제작 된 페이지 매긴된 보고서의 컬렉션을 만드는 방법에 알아봅니다.
author: maggiesMSFT
manager: kfile
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 04/18/2019
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: dcf9b8befabfec98fcae154e6276f8e698b3ddc2
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2019
ms.locfileid: "61150957"
---
# <a name="create-classic-workspaces-in-power-bi"></a>Power BI에서 클래식 작업 영역 만들기

Power BI에서 만들 수 있습니다 *작업 영역*, 작성 하 고 대시보드, 보고서의 컬렉션을 구체화 하는 동료와 공동 작업을 배치 하 고 페이지를 매긴 보고서입니다. 다음으로 컬렉션을 함께 묶을 수 있습니다 *앱* 를 전체 조직 또는 특정 사람 또는 그룹을 배포할 수 있습니다. 

**알고 계십니까?** Power BI는 이제 새로운 작업 영역 환경을 제공 합니다. 읽기 [새 작업 영역에서 작업을 구성](service-new-workspaces.md) 새 작업 영역에 대 한 세부 정보에 대 한 합니다. 

클래식 작업 영역을 만들면 기본, 연결 된 Office 365 그룹을 만드는 합니다. 모든 작업 영역 관리는 Office 365에 위치합니다. 동료를 이러한 작업 영역에 구성원 또는 관리자로 추가할 수 있습니다. 작업 영역에 있는 대시보드, 보고서는 물론, 더 광범위한 대상 그룹에 게시할 계획이 있는 기타 문서에 대해 공동 작업할 수 있습니다. 작업 영역에 있는 추가된 모든 사용자에게는 Power BI Pro 라이선스가 필요합니다. 

## <a name="video-apps-and-app-workspaces"></a>비디오: 앱 및 앱 작업 영역
<iframe width="640" height="360" src="https://www.youtube.com/embed/Ey5pyrr7Lk8?showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="create-a-classic-app-workspace-based-on-an-office-365-group"></a>Office 365 그룹에 따라 클래식 앱 작업 영역 만들기

앱 작업 영역을 만들 때 Office 365 그룹에 기반합니다.

[!INCLUDE [powerbi-service-create-app-workspace](./includes/powerbi-service-create-app-workspace.md)]

처음 만들 때 작업 영역에서 Office 365에 전파하도록 한 시간 정도 기다려야 합니다. 

### <a name="add-an-image-to-your-office-365-app-workspace-optional"></a>Office 365 앱 작업 영역에 이미지 추가(선택 사항)
기본적으로 Power BI는 해당 앱에 앱의 이니셜이 포함된 작은 컬러 원을 만듭니다. 하지만 이미지로 사용자 지정할 수도 있습니다. 이미지를 추가하려면 Exchange Online 라이선스가 필요합니다.

1. **작업 영역**을 선택하고 작업 영역 이름 옆의 줄임표(...), **구성원**을 차례로 선택합니다. 
   
     ![작업 영역 구성원 선택](media/service-create-distribute-apps/power-bi-apps-workspace-members.png)
   
    작업 영역에 대한 Office 365 Outlook 계정은 새로운 브라우저 창에서 열립니다.
2. 왼쪽 위에 있는 컬러 원에 마우스를 올려 놓으면 연필 아이콘으로 바뀝니다. 선택합니다.
   
     ![Office 365 연필 아이콘](media/service-create-distribute-apps/power-bi-apps-workspace-edit-image.png)
3. 연필 아이콘을 다시 선택한 후 사용하려는 이미지를 찾습니다.
   
     ![연필 아이콘 다시 선택](media/service-create-distribute-apps/power-bi-apps-workspace-edit-group.png)

     이미지는.png,.jpg,.bmp 파일을 수 있습니다. 파일 크기는 3MB로 등록 클 수 있습니다. 

4. **저장**을 선택합니다.
   
     ![저장 선택](media/service-create-distribute-apps/power-bi-apps-workspace-save-image.png)
   
    이미지는 Office 365 Outlook 창에서 컬러 원을 대체합니다. 
   
     ![사용자 지정된 이미지](media/service-create-distribute-apps/power-bi-apps-workspace-image-in-office-365.png)
   
    몇 분 후 Power BI의 앱에도 나타납니다.
   
     ![사용자 지정된 이미지](media/service-create-distribute-apps/power-bi-apps-image.png)

## <a name="add-content-to-your-app-workspace"></a>앱 작업 영역에 콘텐츠 추가

앱 작업 영역을 만들면 콘텐츠를 추가할 수 있습니다. 이 작업은 작업 영역의 다른 사람이 보고 작업할 수도 있다는 점을 제외하고 내 작업 영역에 콘텐츠를 추가하는 것과 같습니다. 큰 차이점은 완료되면 콘텐츠를 앱으로 게시할 수 있다는 것입니다. 앱 작업 영역에서 콘텐츠 목록의 콘텐츠를 볼 때 앱 작업 영역의 이름이 소유자로 나열됩니다.

### <a name="connect-to-third-party-services-in-app-workspaces"></a>앱 작업 영역에서 타사 서비스에 연결

앱은 Power BI에서 지원하는 모든 타사 서비스에 제공됩니다. 그러면 Microsoft Dynamics CRM, Salesforce 또는 Google Analytics 등 사용하는 서비스에서 데이터를 가져올 수 있습니다. 조직 앱을 게시하여 필요한 데이터를 사용자에게 제공할 수 있습니다.

현재 작업 영역에서 Microsoft Dynamics CRM, Salesforce 또는 Google Analytics 등 조직 콘텐츠 팩 및 타사 콘텐츠 팩을 사용하여 연결할 수 있습니다. 앱에 조직 콘텐츠 팩을 마이그레이션하는 것이 좋습니다.

## <a name="distribute-an-app"></a>앱 배포

조직 내에서 대규모 대상에 게 공식 콘텐츠를 배포 하려는 경우에 작업 영역에서 앱을 게시할 수 있습니다.  대시보드 및 보고서를 게시 하려면를 선택 하 고 다음으로 게시 하 콘텐츠가 준비 되 면 프로그램 *앱*합니다. 각 작업 영역에서 하나의 앱을 만들 수 있습니다.

왼쪽된 탐색 영역에서 앱은 이전에 설치한 모든 앱을 보여 줍니다. 동료는 몇 가지 다른 방법으로 앱을 설치할 수 있습니다. 
- 찾을 수 하며 Microsoft AppSource에서 앱을 설치 합니다.
- 이러한 직접 링크를 보낼 수 있습니다. 
- Power BI 관리자가 사용자에게 사용 권한을 부여한 경우 동료의 Power BI 계정에서 해당 앱을 자동으로 설치할 수 있습니다. 

작업 영역에서 업데이트를 게시 한 후 업데이트 된 앱 콘텐츠를 자동으로 표시 하는 사용자. 작업 영역에서 앱 콘텐츠를 사용한 데이터 집합의 새로 고침 일정을 설정 하 여 데이터를 새로 고치는 빈도 제어할 수 있습니다. 참조 [Power BI에서 새 작업 영역에서 앱을 게시할](service-create-distribute-apps.md) 세부 정보에 대 한 합니다.

## <a name="power-bi-classic-apps-faq"></a>Power BI 클래식 앱 FAQ

### <a name="how-are-apps-different-from-organizational-content-packs"></a>앱이 조직 콘텐츠 팩과 다른점
앱은 조직 콘텐츠 팩이 진화된 것입니다. 조직 콘텐츠 팩이 이미 있는 경우 앱과 함께 계속 작동합니다. 앱 및 콘텐츠 팩에는 몇 가지 주요 차이점이 있습니다. 

* 비즈니스 사용자가 콘텐츠 팩을 설치한 후에는 그룹화된 ID를 잃게 됩니다. 그저 다른 대시보드 및 보고서가 혼재된 대시보드 및 보고서 목록일 뿐입니다. 한편으로, 앱은 설치 후에도 그룹화와 ID를 유지합니다. 이 그룹화를 통해 비즈니스 사용자는 시간이 지나도 계속 해당 앱으로 쉽게 이동할 수 있습니다.
* 어떠한 작업 영역에서도 여러 콘텐츠 팩을 만들 수 있지만 앱은 해당 작업 영역과 일대일 관계를 맺습니다. 
* 시간이 지나면 조직 콘텐츠 팩의 사용을 중단할 계획이므로, 지금부터 앱을 만드는 것이 좋습니다.  
* 새 작업 영역 환경 미리 보기를 사용하여 조직 콘텐츠 팩의 사용을 중단하는 첫 번째 조치를 취합니다. 미리 보기 작업 영역에서 해당 앱을 사용하거나 만들 수 없습니다.

[기존 앱 작업 영역과 새 앱 작업 영역의 차이점은?](service-new-workspaces.md#how-are-the-new-workspaces-different-from-current-workspaces)를 참조하여 둘을 비교합니다. 

## <a name="next-steps"></a>다음 단계
* [Power BI에서 앱 설치 및 사용](service-create-distribute-apps.md)
- [새 작업 영역 만들기(미리 보기)](service-create-the-new-workspaces.md)
* 궁금한 점이 더 있나요? [Power BI 커뮤니티에 질문합니다.](http://community.powerbi.com/)
