---
title: "Power BI의 소매점 분석 샘플: 둘러보기"
description: "Power BI의 소매점 분석 샘플: 둘러보기"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 10/27/2017
ms.author: mihart
ms.openlocfilehash: 338f45ec7aa4564dfd17678b5c5296a08c078334
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/13/2017
---
# <a name="retail-analysis-sample-for-power-bi-take-a-tour"></a>Power BI의 소매점 분석 샘플: 둘러보기
## <a name="about-the-retail-analysis-sample"></a>소매점 분석 샘플 정보
이 업계 샘플 대시보드 및 기본 보고서는 여러 상점과 구역에서 판매된 항목의 소매점 판매 데이터를 분석합니다. 메트릭은 새 상점 분석뿐 아니라 판매, 단위, 총 수익 및 차이 영역에서 작년과 금년의 실적을 비교합니다. 이 샘플은 익명화된 obviEnce([www.obvience.com](http://www.obvience.com))의 실제 데이터입니다.

[이 샘플에 대한 데이터 집합(Excel 통합 문서)만 다운로드](http://go.microsoft.com/fwlink/?LinkId=529778)할 수도 있습니다.

![](media/sample-retail-analysis/retail1.png)

## <a name="start-on-the-dashboard-and-open-the-report"></a>대시보드 시작 및 보고서 열기
1. 대시보드에서 "Total Stores" 타일을 선택합니다.
   
   ![](media/sample-retail-analysis/retail-analysis-7.png)  
   
   그러면 보고서의 "Store Sales Overview" 페이지로 이동합니다. 총 104개의 상점이 있고 그중 10개는 새 상점임을 알 수 있습니다. Fashions Direct 및 Lindseys라는 두 개의 체인이 있습니다. Fashions Direct 상점은 평균적으로 더 큽니다.
2. 원형 차트에서 **Fashions Direct**를 선택합니다.
   
   ![](media/sample-retail-analysis/retail3.png)  
   
   거품형 차트의 결과를 확인합니다.
   
   ![](media/sample-retail-analysis/pbi_sample_retanlbubbles.png)  
   
   FD-01 구역에는 제곱 피터당 최고 평균 판매량이, FD 02에는 작년 대비 가장 차이가 적은 판매량이 있으며, FD-03과 FD 04는 전반적으로 가장 부진한 실적을 나타냅니다.
3. 개별 거품형 차트 또는 다른 차트를 선택하여 선택 항목의 영향을 보여 주는 교차 강조 표시를 확인합니다.
4. 대시보드로 돌아가려면 맨 위 탐색 모음에서 그 이름을 선택합니다(breadcrumbs). 
   
   ![](media/sample-retail-analysis/power-bi-breadcrumbs.png)
5. 대시보드에서 "This Year’s Sales"라는 타일을 선택합니다.
   
   ![](media/sample-retail-analysis/pbi_sample_retanlthisyrsales.png)
   
   이는 질문 상자에 "This year sales"를 입력하는 것과 같습니다.
   
   다음 화면이 표시됩니다.
   
   ![](media/sample-retail-analysis/retail7.png)

## <a name="review-a-tile-created-with-power-bi-qa"></a>Power BI 질문 및 답변을 사용하여 만든 타일 검토
보다 자세히 살펴보겠습니다.

1. 질문에 “this year sales **by district**”를 추가합니다. 결과를 확인합니다. 답변이 가로 막대형 차트에 자동으로 배치되며 다른 구를 제안합니다.
   
   ![](media/sample-retail-analysis/retail8.png)
2. 이제 질문을 “this year sales **by zip and chain**”으로 변경합니다.
   
   적절한 차트를 사용하여 질문을 입력할 때 어떻게 답을 얻을 수 있는지 확인합니다.
3. 더 많은 질문을 입력하여 얻을 수 있는 결과의 종류를 확인합니다.
4. 준비가 되면 대시보드로 돌아갑니다.

## <a name="dive-deeper-into-the-data"></a>데이터를 심층적으로 알아보기
이제 보다 자세한 수준에서 구역의 실적을 살펴보겠습니다.

1. 대시보드에서 올해와 작년의 판매를 비교하는 타일을 선택합니다.
   
   ![](media/sample-retail-analysis/pbi_sample_retanlareacht.png)
   
   작년에 대한 편차 %에서 큰 변화를 확인할 수 있으며 1월, 4월 및 7월은 특히 나쁜 달입니다.
   
   ![](media/sample-retail-analysis/pbi_sample_retanlsalesvarcol.png)
   
   문제가 발생할 수 있는 위치의 범위를 좁힐 수 있는지 살펴보겠습니다.
2. 거품형 차트를 선택하고 **020-남성복**을 선택합니다.
   
   ![](media/sample-retail-analysis/retail11.png)  
   
   4월에는 남성복 범주가 전체 비즈니스 만큼 심각하게 영향을 받지 않았지만, 1월과 7월은 여전히 문제의 달입니다.
3. 이제 **010-여성복의 거품형 차트**를 선택합니다.
   
   ![](media/sample-retail-analysis/retail12.png)
   
   여성복 범주는 모든 달에 걸쳐 전체 비즈니스보다 훨씬 부진하며, 전년도에 비해 거의 모든 달에서 훨씬 부진합니다.
4. 다시 거품을 선택하여 필터를 지웁니다.

## <a name="try-out-the-slicer"></a>슬라이서 사용해 보기
특정 구역에서는 어떻게 수행되는지 살펴보겠습니다.

1. 왼쪽 위에 있는 슬라이서에서 Allan Guinot을 선택합니다.
   
   ![](media/sample-retail-analysis/retail13.png)
   
   Allan의 구역은 작년 3월과 6월의 실적이 우수했습니다.
2. 이제 Allan을 계속 선택한 상태에서 여성복 거품형 차트를 선택합니다.
   
   ![](media/sample-retail-analysis/power-bi-allan.png)
   
   여성복 범주의 경우, 그의 구역은 작년 물량을 충족하지 못했습니다.
3. 다른 구역 관리자 및 범주를 살펴봅니다. 어떤 사항을 파악할 수 있을까요?
4. 준비가 되면 대시보드로 돌아갑니다.

## <a name="what-is-our-data-telling-us-about-sales-growth-this-year"></a>데이터는 올해 매출 성장에 대해 어떤 정보를 알려주나요?
마지막으로 살펴볼 영역은 성장으로 올해에 개업한 신규 매장입니다.

1. 'Stores Opened This Year' 타일을 선택합니다.
   
   ![](media/sample-retail-analysis/retail15.png)
   
   타일에서 알 수 있듯이 올해 개업한 Lindseys 매장보다 더 많은 Fashions Direct 매장이 더 많습니다.
2. 'Sales Per Sq Ft by Name' 차트를 관찰합니다.
   
   ![](media/sample-retail-analysis/retail14.png)
   
    신규 매장의 Average Sales per SQF에 약간의 차이가 있습니다.
3. 오른쪽 위 차트에서 Fashions Direct 범례 항목을 클릭합니다. 동일한 체인의 경우에도 최고 매장(Winchester Fashions Direct)과 최하위 매장(Cincinnati 2 Fashions Direct)의 실적이 각각 $21.22 대 $12.86로 최고 매장이 현저하게 우수함을 확인할 수 있습니다.
   
   ![](media/sample-retail-analysis/power-bi-lindseys.png)
4. 슬라이서에서 Winchester Fashions Direct를 클릭하고 꺾은선형 차트를 관찰합니다. 첫 번째 판매 수치가 2월에 보고되었습니다.
5. 슬라이서에서 Cincinnati 2 Fashions Direct를 클릭합니다. 꺾은선형 차트에서 이 매장은 6월에 개업했으며 실적이 최악인 매장으로 보입니다.
6. 이전과 마찬가지로 전체 차트에서 막대형, 꺾은선형 및 거품형 차트를 클릭하여 검색할 수 있는 내용을 확인합니다.

이제 재생하는 데 안전한 환경입니다. 언제든지 변경 내용을 저장하지 않도록 선택할 수 있습니다. 그러나 변경 내용을 저장하면 언제든지 이 샘플의 새 복사본에 대해 데이터 가져오기로 이동할 수 있습니다.

## <a name="next-steps-connect-to-your-data"></a>다음 단계: 데이터에 연결
이 둘러보기가 Power BI 대시보드, 질문 및 답변, 보고서를 통해 소매 데이터를 파악하는 방법을 확인하는 데 도움이 되었기를 바랍니다. 이제 사용자 데이터에 연결할 차례입니다. Power BI를 사용하여 다양한 데이터 소스에 연결할 수 있습니다. [Power BI 시작하기](service-get-started.md)에 대해 자세히 알아보세요.

## <a name="next-steps"></a>다음 단계
* [소매점 분석 샘플 콘텐츠 팩 다운로드](sample-tutorial-connect-to-the-samples.md)    
* [이 Power BI 샘플에 대한 Excel 통합 문서 다운로드](http://go.microsoft.com/fwlink/?LinkId=529778)    
* [Power BI에 대한 데이터 가져오기](service-get-data.md)    
* [Power BI - 기본 개념](service-basic-concepts.md)    
* 궁금한 점이 더 있나요? [Power BI 커뮤니티를 이용하세요.](http://community.powerbi.com/)
