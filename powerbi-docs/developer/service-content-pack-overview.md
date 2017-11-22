---
title: "Power BI 서비스 콘텐츠 팩 프로그램의 개요"
description: "콘텐츠 팩 인증 프로그램"
services: powerbi
documentationcenter: 
author: guyinacube
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/09/2017
ms.author: asaxton
ms.openlocfilehash: 4a8ea2acfcfe41192b82addfe52dbe67a0df8088
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/15/2017
---
# <a name="overview-of-the-power-bi-service-content-pack-program"></a>Power BI 서비스 콘텐츠 팩 프로그램의 개요
콘텐츠 팩은 사용자가 원본에서 즉시 정보를 얻을 수 있도록 해주는 기본 제공 콘텐츠 집합입니다. 일반적으로 콘텐츠 팩은 역할, 도메인, 워크플로에 대한 정보를 제공하는 특정 비즈니스 시나리오에 초점을 둡니다.

ISV는 고객이 자신의 계정에 연결하고 인스턴스화할 수 있는 템플릿 콘텐츠 팩을 빌드할 수 있습니다. 도메인 전문가는 비즈니스 사용자가 쉽게 사용할 수 있는 방식으로 데이터의 잠금을 해제할 수 있습니다. 콘텐츠 팩은 보고 인프라에 대한 과도한 투자 없이도 고객에게 애드혹 모니터링 및 분석 기능을 제공합니다. 

서식 파일 콘텐츠 팩을 구축하는 이러한 ISV는 Power BI 콘텐츠 팩 갤러리(app.powerbi.com/getdata/services) 및 Microsoft AppSource(appsource.microsoft.com)에서 공개적으로 사용할 수 있도록 Power BI 팀에 제출될 수 있습니다. 공용 콘텐츠 팩 환경에 대한 예는 [여기](template-content-pack-experience.md)에서 확인할 수 있습니다.

## <a name="overview"></a>개요
템플릿 콘텐츠 팩을 개발 및 제출하는 일반적은 프로세스는 여러 단계로 구성됩니다.

 ![프로세스](media/service-content-pack-overview/developer-content-pack-overview.png)

1. [요구 사항을 검토](#requirements)하고 충족하는지 확인
2. Power BI Desktop에서 [콘텐츠 빌드](template-content-pack-authoring.md#queries)
3. PowerBI.com에서 [대시보드 만들기](template-content-pack-authoring.md#dashboard)
4. [콘텐츠 팩을 조직 내에서 직접 테스트](template-content-pack-testing.md)
5. 게시를 위해 Power BI에 콘텐츠 [제출](template-content-pack-testing.md#submission)

<a name="requirements"></a>

## <a name="requirements"></a>요구 사항
PowerBI 서비스 및 AppSource에 게시될 콘텐츠 팩을 빌드하고 제출하려면 다음 요구 사항을 충족해야 합니다.

* 비즈니스 사용자가 사용할 SaaS 응용 프로그램이 있습니다.
* SaaS 응용 프로그램에 Power BI에서 시각화될 수 있는 사용자 데이터가 있습니다.
* SaaS 응용 프로그램에 공용 인터넷을 통해 액세스할 수 있는 API가 있습니다. 이상적으로 API는 REST 기반 API 또는 OData 피드입니다. Power BI 콘텐츠 팩은 기본 인증, OAuth 2.0 및 API 키와 같은 여러 인증 유형을 지원합니다. 
* 서명된 파트너 계약입니다. [제출 단계](template-content-pack-testing.md#submission)에서 해당 작업을 수행합니다.

기술 요구 사항에 대한 자세한 내용은 [제작](template-content-pack-authoring.md) 섹션을 검토하세요.

## <a name="business-scenario"></a>비즈니스 시나리오
콘텐츠 팩은 특정 비즈니스 시나리오에 초점을 맞춘 정보와 메트릭을 제공합니다. 대상 그룹과 콘텐츠 팩에서 얻게 되는 이점을 이해하면 사용자가 콘텐츠를 성공적으로 활용하도록 할 수 있습니다.

### <a name="tips"></a>팁
* 대상 그룹 및 수행하려는 작업 파악  
* 특정 기간(지난 90일) 또는 최근 N개 결과에 초점을 둠  
* 시나리오에 관련된 테이블/열만 가져오기  
* 별도의 고유한 시나리오에 대해 두 개 이상의 콘텐츠 팩을 제공하는 방법 고려  

## <a name="frequently-asked-questions"></a>질문과 대답
**소유하지 않은 타사 SaaS 응용 프로그램에 대한 Power BI 서비스 콘텐츠 팩을 빌드할 수 있습니까?**

아니요, 현재 서비스에서 콘텐츠 팩을 게시하기 전에 SaaS 응용 프로그램의 소유자와 파트너 계약을 서명해야 합니다.

**내 서비스에 대한 공용 개발자 API가 없습니다. 데이터 저장소에서 데이터를 직접 가져오는 Power BI 서비스 콘텐츠 팩을 빌드할 수 있습니까?**

아니요, Power BI 서비스 콘텐츠 팩에는 공용 인터넷을 통해 액세스할 수 있는 개발자 API가 필요합니다.

**서비스 콘텐츠 팩에서 지원되는 API의 유형은 무엇이며 함께 사용할 수 있는 인증 유형은 무엇입니까?**

Power BI 서비스 콘텐츠 팩은 모든 REST API 또는 OData 피드를 지원합니다. Power BI는 기본 인증, OAuth2.0 및 웹 API 키를 비롯 한 여러 인증 유형과 함께 작업할 수 있습니다. 기술 요구 사항에 대한 자세한 내용은 [제작](template-content-pack-authoring.md#dashboard) 문서를 참조하세요.

**서비스 콘텐츠 팩에 대한 더 많은 질문이 있습니다. 어떻게 연락할 수 있습니까?**

pbiservicesapps@microsoft.com으로 메일을 보내 자유롭게 질문하세요.

## <a name="support"></a>지원
개발 중에 지원을 받으려면 [https://powerbi.microsoft.com/support](https://powerbi.microsoft.com/support)를 사용하세요. 적극적으로 모니터링 및 관리됩니다. 고객 인시던트에서 해당 팀에 연락하는 방법을 신속하게 찾을 수 있습니다.

## <a name="next-step"></a>다음 단계
[작성](template-content-pack-authoring.md)
