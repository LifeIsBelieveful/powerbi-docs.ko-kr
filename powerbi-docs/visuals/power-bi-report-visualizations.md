---
title: Power BI 서비스 및 Desktop의 보고서 시각화 개요
description: Microsoft Power BI의 보고서 시각화(시각적 개체)에 대한 개요입니다.
author: mihart
ms.author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: SYk_gWrtKvM
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/28/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: d470a262bd8a5e6590746fb07889b1230f5cfc25
ms.sourcegitcommit: 8bf2419b7cb4bf95fc975d07a329b78db5b19f81
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66375658"
---
# <a name="visualizations-in-power-bi-reports"></a>Power BI 보고서의 시각화

시각화(즉, 시각적 개체)는 데이터에서 발견된 정보를 표시합니다. Power BI 보고서에 시각적 개체가 하나 있는 단일 페이지가 포함될 수도 있고 시각적 개체로 가득한 여러 페이지가 포함될 수도 있습니다. Power BI 서비스에서 시각적 개체를 [보고서에서 대시보드에 고정](../service-dashboard-pin-tile-from-report.md)할 수 있습니다.

보고서 간의 차이점을 확인 해야 *디자이너가* 및 보고서 *소비자* 작성 하거나 보고서를 수정 하는 사용자 경우 디자이너는 합니다.  디자이너는 보고서 및 해당 기본 데이터 집합 편집 권한이 있습니다. 즉, Power BI Desktop에서는 데이터 뷰에서 데이터 세트를 열고 보고서 보기에서 시각적 개체를 만들 수 있습니다. Power BI 서비스에서 즉, 데이터 집합 또는 보고서의 보고서 편집기에서 열면 [편집용 보기](../consumer/end-user-reading-view.md)합니다. 보고서 또는 대시보드가 [사용자와 공유](../consumer/end-user-shared-with-me.md)되는 경우 사용자는 보고서 **소비자**입니다. 보고 보고서 및 시각적 개체와 상호 작용할 수 있지만 주요 변경 내용을 저장할 수 없습니다.

Power BI 시각화 창에서 바로 사용할 수 있는 다양한 시각적 개체 유형이 있습니다.

![](media/power-bi-report-visualizations/power-bi-templates.png)

더 많은 선택 옵션을 보려면 [Microsoft AppSource 커뮤니티 사이트](https://appsource.microsoft.com)를 방문하여 Microsoft와 커뮤니티에서 제공하는 [사용자 지정 시각적 개체](../developer/custom-visual-develop-tutorial.md)를 찾아서 [다운로드](https://appsource.microsoft.com/marketplace/apps?page=1&product=power-bi-visuals)하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/SYk_gWrtKvM?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>


  Power BI를 처음 사용하거나 복습이 필요하면, 아래 링크를 사용하여 Power BI 시각화의 기본 사항을 알아봅니다.  또는, 목차(문서의 왼쪽에 있는)를 사용하여 훨씬 더 유용한 정보를 찾아봅니다.

## <a name="add-a-visualization-in-power-bi"></a>Power BI에서 시각화 개체 추가

보고서의 페이지에 [시각화를 만듭니다](power-bi-report-add-visualizations-i.md). [사용 가능한 시각화 및 사용 가능한 시각화 자습서의 목록](power-bi-visualization-types-for-reports-and-q-and-a.md)을 찾아봅니다. 

## <a name="upload-a-custom-visualization-and-use-it-in-power-bi"></a>사용자 지정 시각화 개체의 업로드 및 Power BI에서 사용

직접 만든 또는 [Microsoft AppSource 커뮤니티 사이트](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals)에서 찾은 사용자 지정 시각화를 추가합니다. 창의성이 느껴지나요? 소스 코드를 더 자세히 살펴보고 [개발자 도구](../developer/custom-visual-develop-tutorial.md)를 사용하여 새로운 시각화 유형을 만들고 [커뮤니티에도 공유](../developer/office-store.md)해 주세요. 사용자 지정 시각적 개체를 개발하는 방법을 자세히 알아보려면 [Power BI 사용자 지정 시각적 개체 개발](../developer/custom-visual-develop-tutorial.md)을 참조하세요.

## <a name="change-the-visualization-type"></a>시각화 형식 변경

[시각화 형식을 변경](power-bi-report-change-visualization-type.md)하여 어떤 것이 데이터와 가장 최적으로 작동하는지 봅니다.

## <a name="pin-the-visualization"></a>시각화 고정

Power BI에서 원하는 방식의 시각화가 있는 경우 타일 형태로 [대시보드에 고정](../service-dashboard-pin-tile-from-report.md)할 수 있습니다. 시각화를 고정한 후 보고서에 사용되는 시각화를 변경하면 대시보드의 타일이 변경되지 않습니다. 꺾은선형 차트인 경우 보고서에서 도넛형 차트로 변경하더라도 꺾은선형 차트를 유지합니다.

## <a name="limitations-and-considerations"></a>제한 사항 및 고려 사항
- 데이터 원본 필드 (측정값 또는 열)의 수에 따라 시각적 개체는 느린 로드할 수 있습니다.  가독성 및 성능 이유로 모두 10 ~ 20 총 필드에 시각적 개체를 제한 하는 것이 좋습니다. 

- 시각적 개체에 대 한 상한 제한은 100 필드 (측정값 또는 열)입니다. 시각적 개체를 로드 하지 못하는 경우에 필드의 수를 줄입니다.   

## <a name="next-steps"></a>다음 단계

* [Power BI의 시각화 유형](power-bi-visualization-types-for-reports-and-q-and-a.md)
* [사용자 지정 시각적 개체](../power-bi-custom-visuals.md)