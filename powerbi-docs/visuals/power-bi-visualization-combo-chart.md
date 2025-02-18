---
title: Power BI의 콤보 차트
description: 콤보 차트에 대한 이 자습서에서는 Power BI 서비스 및 Desktop에서 콤보 차트를 사용하는 시기와 만드는 방법을 설명합니다.
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: lnv66cTZ5ho
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/22/2019
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: e461480f53f4a97aeb4282e64a8a03eb8e1418d1
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66187780"
---
# <a name="combo-chart-in-power-bi"></a>Power BI의 콤보 차트
Power BI 콤보 차트는 꺾은선형 차트와 세로 막대형 차트를 결합한 단일 시각화 요소입니다. 2개 차트를 하나로 결합하면 데이터를 더 빠르게 비교할 수 있습니다.

콤보 차트에는 하나 또는 두 개의 Y축이 있을 수 있습니다.

## <a name="when-to-use-a-combo-chart"></a>콤보 차트를 사용하는 경우
다음과 같은 경우 콤보 차트를 사용하는 것이 좋습니다.

* X축이 동일한 꺾은선형 차트와 세로 막대형 차트가 있는 경우
* 여러 값 범위와 여러 측정값을 비교하는 경우
* 두 측정값 간의 상관관계를 하나의 시각화에 보여주는 경우
* 하나의 측정값이 다른 측정값으로 정의된 목표를 충족하는지 확인하는 경우
* 캔버스 공간을 절약하려는 경우

### <a name="prerequisites"></a>필수 조건
콤보 차트는 Power BI 서비스 및 Power BI Desktop에서 사용할 수 있습니다. 이 자습서에서는 Power BI 서비스를 사용하여 콤보 차트를 만듭니다. 자습서를 따라 하려면 Power BI 서비스를 열고 "소매 분석" 샘플([아래 지침](#create))에 연결합니다.


## <a name="create-a-basic-single-axis-combo-chart"></a>기본, 단일 축, 콤보 차트 만들기
Will이 판매 및 샘플 마케팅을 사용하여 콤보 차트를 만드는 과정을 시청합니다.

<iframe width="560" height="315" src="https://www.youtube.com/embed/lnv66cTZ5ho?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>  

<a name="create"></a>고유한 콤보 차트를 만들려면 Power BI 서비스에 로그인하고 **데이터 가져오기 \> 샘플 \> 소매 분석 샘플 &gt; 연결 &gt; 대시보드로 이동**을 선택합니다.

1. "소매 분석 샘플" 대시보드에서 **Total Stores** 타일을 선택하여 "소매 분석 샘플" 보고서를 엽니다.
2. **보고서 편집** 을 선택하여 편집용 보기에서 보고서를 엽니다.
3. 새 보고서 페이지를 추가합니다.
4. 올해의 판매액 및 총 수익을 월별로 표시하는 세로 막대형 차트를 만듭니다.

    a.  필드 창에서 **Sales** \> **This Year Sales** > **Values**를 선택합니다.

    b.  **Sales** \> **Gross Margin This Year**을 **값** 영역에 끌어다 놓습니다.

    c. **Time** \> **FiscalMonth**를 선택하여 **축** 영역에 추가합니다.

    ![](media/power-bi-visualization-combo-chart/combotutorial1new.png)
5. 시각화의 오른쪽 위 모서리에 있는 줄임표(...)를 선택하고 **정렬 기준 > FiscalMonth**를 선택합니다. 정렬 순서를 변경하려면 줄임표를 다시 선택하고 **오름차순 정렬** 또는 **내림차순 정렬**을 선택합니다.

6. 세로 막대형 차트를 콤보 차트로 변환합니다. 사용 가능한 두 가지 콤보 차트는 다음과 같습니다. **꺾은선형 및 누적 세로 막대형** 및 **꺾은선형 및 묶은 세로 막대형**. 세로 막대형 차트를 선택한 상태로 **시각화** 창에서 **꺾은선형 및 묶은 세로 막대형 차트**를 선택합니다.

    ![](media/power-bi-visualization-combo-chart/converttocombo_new2.png)
7. **필드** 창에서 **Sales** \> **Last Year Sales**를 **꺾은선형 값** 버킷으로 끌어다 놓습니다.

   ![](media/power-bi-visualization-combo-chart/linevaluebucket.png)

   콤보 차트가 다음과 같이 표시됩니다.

   ![](media/power-bi-visualization-combo-chart/combochartdone-new.png)

## <a name="create-a-combo-chart-with-two-axes"></a>두 개의 축이 있는 콤보 차트 만들기
이 작업에서는 총 수익과 매출을 비교하겠습니다.

1. 추적 하는 새로운 꺾은선형 차트를 만듭니다 **작년 % Gross Margin** 하 여 **FiscalMonth**합니다. **월별** 및 **오름차순** 기준으로 정렬하려면 줄임표를 선택합니다.  
1월에는 GM%가 35%였고, 4월에 45% 고점에 도달했으며, 7월에 감소하고, 8월에 다시 고점에 도달했습니다. 작년과 금년의 매출 패턴이 유사할까요?

   ![](media/power-bi-visualization-combo-chart/combo1_new.png)
2. **This Year Sales > Value** 및 **Last Year Sales**를 꺾은선형 차트에 추가합니다. **Gross Margin Last Year(%)** 의 눈금은 **Sales** 눈금보다 훨씬 작기 때문에 비교하기가 어렵습니다.      

   ![](media/power-bi-visualization-combo-chart/flatline_new.png)
3. 보다 쉽게 읽고 해석 가능한 시각적 개체를 만들려면 꺾은선형 차트를 꺾은선형 및 누적 세로 막대형 차트로 변환합니다.

   ![](media/power-bi-visualization-combo-chart/converttocombo_new.png)
4. **Gross Margin Last Year(%)** 을 **세로 막대 값**에서 **꺾은선형 값**으로 끌어다 놓습니다. Power BI가 두 개의 축을 만들기 때문에 데이터 세트의 크기를 다르게 조정할 수 있습니다. 왼쪽은 판매액(달러)을 측정하고, 오른쪽은 백분율을 측정합니다. 질문에 대한 답변이 보입니다. 즉, 유사한 패턴이 확인됩니다.

   ![](media/power-bi-visualization-combo-chart/power-bi-clustered-combo.png)    

## <a name="add-titles-to-the-axes"></a>축에 제목 추가
1. 페인트 롤러 아이콘 ![](media/power-bi-visualization-combo-chart/power-bi-paintroller.png)을 선택하여 서식 창을 엽니다.
2. 아래쪽 화살표를 선택하여 **Y축** 옵션을 확장합니다.
3. 에 대 한 **y 축 (열)** 설정 **위치** 하 **왼쪽**설정 **제목** 에 **에**,  **스타일** 하 **제목만 표시**, 및 **표시 단위** 으로 **수백만**합니다.

   ![](media/power-bi-visualization-combo-chart/power-bi-open-y.png)
4. 아래 **y 축 (열)** 에 표시 될 때까지 아래로 스크롤하여 **보조 표시**합니다. Y 축에 대 한 많은 옵션 이기 때문에 두 스크롤 막대를 사용 해야 합니다. 보조 표시 섹션에는 콤보 차트의 꺾은선형 차트 서식 지정 옵션이 표시 됩니다.

   ![](media/power-bi-visualization-combo-chart/power-bi-secondary.png)
5. **Y축(선)** 에 대해 **위치**는 그대로 **오른쪽**으로 두고, **제목**을 **켬**으로 설정하고, **스타일**을 **제목만 표시**로 설정합니다.

   이제 콤보 차트에 이중 축과 제목이 표시됩니다.

   ![](media/power-bi-visualization-combo-chart/power-bi-2-titles.png)

6. 차트의 가독성을 높일 수 있도록 필요에 따라 텍스트 글꼴, 크기 및 색을 수정하고 기타 서식 옵션을 설정합니다.

여기서 다음과 같은 작업을 수행할 수 있습니다.

* [대시보드 타일로 콤보 차트를 추가합니다](../service-dashboard-tiles.md).
* [보고서를 저장합니다](../service-report-save.md).
* [장애가 있는 사용자가 보고서에 액세스할 수 있도록 만듭니다](../desktop-accessibility.md).

## <a name="cross-highlighting-and-cross-filtering"></a>교차 강조 표시 및 교차 필터링

콤보 차트에서 특정 세로 막대 또는 꺾은선을 강조 표시하면 보고서 페이지의 다른 시각화 요소가 교차 강조 표시 및 교차 필터링되며 그 반대의 경우도 마찬가지입니다. 이 기본 동작을 변경하려면 [시각적 상호 작용](../service-reports-visual-interactions.md)을 사용합니다.

## <a name="next-steps"></a>다음 단계

[Power BI의 도넛형 차트](power-bi-visualization-doughnut-charts.md)

[Power BI의 시각화 유형](power-bi-visualization-types-for-reports-and-q-and-a.md)
