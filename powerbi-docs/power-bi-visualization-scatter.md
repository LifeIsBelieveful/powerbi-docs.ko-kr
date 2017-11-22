---
title: "Power BI의 분산형 차트(자습서)"
description: "자습서: Power BI의 분산형 차트"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: PVcfPoVE3Ys
qualityfocus: identified
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/27/2017
ms.author: mihart
ms.openlocfilehash: c1801db4135d6d97a940e593de37ca2886194b53
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/13/2017
---
# <a name="scatter-charts-and-bubble-charts-in-power-bi-tutorial"></a>Power BI의 분산형 차트 및 거품형 차트(자습서)
분산형 차트에는 항상 가로 축을 따라 하나의 숫자 데이터 집합을 표시하고 세로 축을 따라 다른 숫자 값 집합을 표시하는 두 개의 값 축이 있습니다. 차트에서 x 및 y 숫자 값의 교차점에 점이 표시되고 이러한 값이 단일 데이터 요소로 결합됩니다. 데이터에 따라 가로 축에 균등 또는 불균등하게 이러한 데이터 요소를 배포할 수 있습니다.

거품형 차트는 데이터 요소를 거품으로 바꾸며 거품 *크기*로 데이터의 추가 차원을 나타냅니다.

![](media/power-bi-visualization-scatter/power-bi-bubble-chart.png)

## <a name="when-to-use-a-scatter-chart-or-bubble-chart"></a>분산형 차트 또는 거품형 차트를 사용해야 하는 경우
### <a name="scatter-charts-are-a-great-choice"></a>다음과 같은 경우 분산형 차트를 사용하는 것이 좋습니다.
* 2개(분산형) 또는 3개(거품형) **숫자** 값 간의 관계를 표시하려는 경우.
* 두 개의 숫자 그룹을 일련의 xy 좌표로 그리려는 경우.
* 가로 축 눈금을 변경하려는 경우 꺾은선형 차트 대신.    
* 가로 축을 로그 눈금으로 전환하려는 경우.
* 쌍을 이루거나 그룹화된 값 집합을 포함하는 워크시트 데이터를 표시하려는 경우. 분산형 차트에서는 그룹화된 값에 대한 자세한 정보를 표시하기 위해 축의 개별 눈금을 조정할 수 있습니다.
* 선형 또는 비선형 추세, 클러스터, 이상값 등을 표시하여 큰 데이터 집합의 패턴을 표시하려는 경우.
* 시간에 관계없이 다수의 데이터 요소를 비교하려는 경우. 분산형 차트에 포함되는 데이터가 많을수록 비교가 더 정확해집니다.

### <a name="bubble-charts-are-a-great-choice"></a>다음과 같은 경우 거품형 차트를 사용하는 것이 좋습니다.
* 데이터에 각각 값 집합을 포함하는 세 가지 데이터 계열이 있는 경우.
* 재무 데이터를 제공하려는 경우.  다양한 거품 크기는 시각적으로 특정 값을 강조 표시하는 데 유용합니다.
* 사분면에 사용하려는 경우.

## <a name="create-a-scatter-chart"></a>분산형 차트 만들기
<iframe width="560" height="315" src="https://www.youtube.com/embed/PVcfPoVE3Ys?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

1. [편집용 보기](service-interact-with-a-report-in-editing-view.md)에서 소매점 분석 샘플을 열고 [새 보고서 페이지를 추가](power-bi-report-add-page.md)합니다.
2. 필드 창에서 **판매액** > **평방 미터당 매출** 및 **판매액** > **총 매출 분산 %**를 선택합니다.
3. 필드 창에서 **구역 > 구역**을 선택합니다.
   
    ![](media/power-bi-visualization-scatter/pbi_scatter_chart_pre_convert.png)
4. 분산형 차트로 변환합니다. 시각화 창에서 분산형 차트 아이콘을 선택합니다.
   ![](media/power-bi-visualization-scatter/pbi_scatter_chart_icon.png).
5. **세부 정보** 에서 **범례** 로 **구역**를 끌어다 놓습니다.
   
    ![](media/power-bi-visualization-scatter/pbi_scatter_chart_new.png)

이제 Y축에 총 매출 분산 %를 그리고 X축에 평방 미터당 매출을 그리는 분산형 차트가 있습니다.  데이터 요소 색은 구역을 나타냅니다.  이제 3차원을 추가해보겠습니다.

## <a name="create-a-bubble-chart"></a>거품형 차트 만들기
1. 필드 창에서 **판매량** > **올해 판매액** > **값**을 **크기** 영역으로 끌어다 놓습니다. 
   
   ![](media/power-bi-visualization-scatter/pbi_scatter_chart_size.png)
2. 거품을 마우스로 가리킵니다.  거품 크기는 **This Year Sales**의 값을 반영합니다.
   
    ![](media/power-bi-visualization-scatter/pbi_scatter_chart_hover.png)
3. 필요에 따라 [시각화 색, 레이블, 제목, 배경 등의 서식을 지정](service-getting-started-with-color-formatting-and-axis-properties.md)합니다.

## <a name="considerations-and-troubleshooting"></a>고려 사항 및 문제 해결
### <a name="your-scatter-chart-has-only-one-data-point"></a>**분산형 차트에 하나의 데이터 요소만 있음**
분산형 차트에 X축과 Y축의 모든 값을 집계하는 하나의 데이터 요소만 있나요?  또는 단일 수평선이나 수직선의 모든 값을 집계하나요?

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot1.png)

**세부 정보** 영역에 필드를 추가하여 Power BI에 값을 그룹화하는 방법을 알립니다. 필드는 그리려는 각 지점에 고유해야 합니다.  
단순 행 번호 또는 ID 필드와 같습니다.

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot.png)

또는 데이터에 해당 필드가 없는 경우 X 및 Y 값을 지점마다 고유한 항목으로 연결하는 필드를 만듭니다.

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot2.png)

새 필드를 만들려면 [Power BI Desktop 쿼리 편집기를 사용하여 인덱스 열을](desktop-add-custom-column.md) 데이터 집합에 추가합니다.  그런 다음 이 열을 시각화의 **세부 정보** 영역에 추가합니다.

## <a name="next-steps"></a>다음 단계
 [Power BI의 시각화 유형](power-bi-visualization-types-for-reports-and-q-and-a.md)

[사용해 보세요. 무료입니다!](https://powerbi.com/)  

궁금한 점이 더 있나요? [Power BI 커뮤니티를 이용하세요.](http://community.powerbi.com/)
