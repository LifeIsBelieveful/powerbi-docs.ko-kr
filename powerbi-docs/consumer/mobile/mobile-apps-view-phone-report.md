---
title: 전화에 대해 최적화된 Power BI 보고서 보기
description: Power BI 휴대폰 앱에서 보도록 최적화된 보고서 페이지와의 상호 작용에 대해 알아봅니다.
author: mshenhav
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 04/22/2019
ms.author: mshenhav
ms.openlocfilehash: 79ca47f83bb39ab9d6df141b5a26dcb54e00c72c
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2019
ms.locfileid: "65100961"
---
# <a name="view-power-bi-reports-optimized-for-your-phone"></a>전화에 대해 최적화된 Power BI 보고서 보기

적용 대상:

| ![iPhone](./media/mobile-apps-view-phone-report/ios-logo-40-px.png) | ![Android 휴대폰](./media/mobile-apps-view-phone-report/android-logo-40-px.png) |
|:--- |:--- |
| iPhone |Android 휴대폰 |

휴대폰에서 Power BI 보고서를 볼 때 Power BI 보고서를 휴대폰에 최적화 된 경우를 확인 합니다. 가 있는 경우 Power BI는 자동으로 최적화 된 보고서를 세로 보기로 열립니다.

![세로 모드 보고서](./media/mobile-apps-view-phone-report/07-power-bi-phone-report-portrait.png)

전화에 최적화 보고서 없다면 보고서는 열리지만 최적화되지 않은 가로 보기 화면으로 열립니다. 휴대폰에 최적화된 보고서에서도 휴대폰를 옆으로 돌리면 보고서는 최적화 되지 않은 보기에서 원본 보고서 레이아웃으로 열립니다. 일부 페이지만 최적화된 경우, 사용자는 세로 보기 메시지를 보게 될 것이며 이는 보고서가 가로 보기로 사용 가능하다는 것을 의미합니다.

![최적화되지 않은 보고서 페이지](./media/mobile-apps-view-phone-report/06-power-bi-phone-report-page-not-optimized.png)

Power BI 보고서의 다른 모든 기능은 휴대폰에 최적화된 보고서에서 여전히 작동합니다. 다음의 경우 무엇을 할 수 있는지에 관해 자세히 알아봅니다.

* [Iphone 상의 보고서](mobile-reports-in-the-mobile-apps.md). 
* [안드로이드 폰 상의 보고서](mobile-reports-in-the-mobile-apps.md).

## <a name="filter-the-report-page-on-a-phone"></a>휴대폰에서 보고서 페이지 필터링
휴대폰에 최적화된 보고서에 정의된 필터가 있는 경우 휴대폰에서 보고서를 볼 때 해당 필터를 사용할 수 있습니다. 휴대폰의 웹에 보고서에서 필터링 되는 값으로 필터링 된 보고서가 열립니다. 페이지에 활성 필터가 있다는 메시지가 표시됩니다. 휴대폰에서 필터를 변경할 수 있습니다.

1. 필터 아이콘을 탭합니다. ![휴대폰 필터 아이콘](./media/mobile-apps-view-phone-report/power-bi-phone-filter-icon.png) 휴대폰 필터 아이콘을 탭합니다. 
2. 기본 또는 고급 필터링을 사용하여 원하는 결과를 확인합니다.
   
    ![휴대폰 BI 휴대폰 보고서 고급 필터](./media/mobile-apps-view-phone-report/power-bi-iphone-advanced-filter-toronto.gif)

## <a name="cross-highlight-visuals"></a>시각적 개체을 강조 표시합니다.
세로 방향의 시각적 개체를 강조 보기 가로 보기로 휴대폰에서 Power BI 서비스에 수행 방식으로 작동 합니다. 한 시각적 개체에서 데이터를 선택하면 그 페이지의 다른 시각적 개체에 있는 관련 데이터도 강조 표시됩니다.

[Power BI에서 필터링 및 강조 표시](../../power-bi-reports-filters-and-highlighting.md)에 대해 자세히 알아보세요.

## <a name="select-visuals"></a>시각적 개체 선택
휴대폰 보고서에서 시각적 개체를 선택하면 휴대폰 보고서는 그 시각적 개체를 강조 표시하고, 그것에 초점을 맞추고, 캔버스 제스처를 무효화합니다.

선택된 시각적 개체를 사용하여 시작적 개체 내에서 스크롤하기와 같은 작업을 수행할 수 있습니다. 시각적 개체를 선택 취소하려면, 시각적 개체 영역 밖 아무 곳이나 그냥 터치합니다.

## <a name="open-visuals-in-focus-mode"></a>시각적 개체를 포커스 모드로 열기
휴대폰 보고서에는 또한 포커스 모드를 제공합니다. 더 크게 보고 단일 시각적을 보다 쉽게 탐색해보세요.

* 휴대폰 보고서에서 시각적 개체의 오른쪽 위 모서리에 있는 줄임표( **...** ) > **포커스 모드로 확장**을 누릅니다.
  
    ![포커스 모드로 확장](././media/mobile-apps-view-phone-report/power-bi-phone-report-focus-mode.png)

보고서 캔버스에서 그 반대로 습득 포커스 모드에서 수행할 작업입니다. 예를 들어, 시각적 개체에서 값을 강조 표시 전체 보고서로 돌아가는 경우에 보고서 시각적 개체에서 강조 표시 된 값으로 필터링 됩니다.

일부 작업은  화면 크기 제약 때문에 포커스 모드에서만 가능합니다.

* 시각적 개체에 표시되는 정보를 **드릴다운**합니다. 휴대폰 보고서에서 [드릴업 및 드릴다운](mobile-apps-view-phone-report.md#drill-down-in-a-visual)하는 방법은 아래에서 자세히 알아보세요.
* 시각적 개체의 값을 **정렬**합니다.
* **되돌리기**: 시각적 개체에서 수행한 탐색 과정을 지우고 보고서가 만들어졌을 때 설정된 정의로 되돌립니다.
  
    시각적 개체에서 모든 탐색을 지우려면 줄임표( **...** ) > **되돌리기**를 누릅니다 .
  
    ![되돌리기](././media/mobile-apps-view-phone-report/power-bi-phone-report-revert-levels.png)
  
    되돌리기 모든 시각적 개체에서 탐색을 지우는 보고서 수준에서 또는 선택한 시각적 개체에서 탐색을 지우는 시각적 수준에서 제공 됩니다.   

## <a name="drill-down-in-a-visual"></a>시각적 개체에서 드릴 다운
시각적 개체에 계층 수준이 정의된 경우 시각적 개체에 표시되는 자세한 정보를 드릴다운한 후 백업할 수 있습니다. Power BI 서비스 또는 Power BI Desktop에서 [시각적 개체에 드릴다운을 추가](../end-user-drill.md)할 수 있습니다.

드릴 다운의 몇 가지 종류가 있습니다.

### <a name="drill-down-on-a-value"></a>값에 대해 드릴 다운
1. 긴 시각적 개체에서 데이터 요소 (누르고)를 탭 합니다.
2. 도구 설명이 나타납니다 및 계층 구조에 정의 된 경우 다음 도구 설명의 바닥글 표시 됩니다 드릴 다운 및 드릴업 화살표입니다.
3. 드릴 다운에 대 한 아래쪽 화살표를 탭 합니다.

    ![눌러서 드릴 다운](././media/mobile-apps-view-phone-report/report-drill-down.png)
    
4. 드릴업에 위쪽 화살표를 누릅니다.

### <a name="drill-to-next-level"></a>다음 수준 표시/숨기기
1. 휴대폰 보고서에서 오른쪽 위 모서리에 있는 줄임표( **...** ) > **포커스 모드로 확장**을 누릅니다.
   
    ![포커스 모드로 확장](././media/mobile-apps-view-phone-report/power-bi-phone-report-focus-mode.png)
   
    이 예제에서 막대는 시/도 값을 보여줍니다.
2. 탐색 아이콘을 탭합니다 ![탐색 아이콘](./media/mobile-apps-view-phone-report/power-bi-phone-report-explore-icon.png) 왼쪽 아래에서.
   
    ![탐색 모드](./media/mobile-apps-view-phone-report/power-bi-phone-report-explore-mode.png)
3. **다음 수준 표시** 또는 **다음 수준으로 확장**을 누릅니다.
   
    ![다음 수준으로 확장](./media/mobile-apps-view-phone-report/power-bi-phone-report-expand-levels.png)
   
    이제 막대는 구/군/시 값을 보여줍니다.
   
    ![확장된 수준](./media/mobile-apps-view-phone-report/power-bi-phone-report-expanded-levels.png)
4. 왼쪽 위 모서리에 있는 화살표를 누르면 하위 수준으로 값이 여전히 확장되어 있는 휴대폰 보고서로 돌아갑니다.
   
    ![하위 수준으로 여전히 확장됨](./media/mobile-apps-view-phone-report/power-bi-back-to-phone-report-expanded-levels.png)
5. 원래 수준으로 다시 올라가려면 줄임표( **...** )를 다시 누르고 **되돌리기**를 누릅니다.
   
    ![되돌리기](././media/mobile-apps-view-phone-report/power-bi-phone-report-revert-levels.png)

## <a name="drill-through-from-a-value"></a>값에서 드릴스루
드릴스루는 다른 보고서 페이지를 사용 하 여 보고서 페이지에서 값을 연결합니다. 다른 보고서 페이지에 데이터 요소에서 드릴스루할 데이터 요소 값을 페이지를 통해 드릴는 필터링에 사용 되 때나 선택한 데이터의 컨텍스트에서 됩니다.
보고서 작성자가 수 [드릴스루 정의](https://docs.microsoft.com/power-bi/desktop-drillthrough) 보고서를 만들 때.

1. 긴 시각적 개체에서 데이터 요소 (누르고)를 탭 합니다.
2. 도구 설명이 나타납니다를 살펴보고 드릴스루에 정의 된 경우 다음 도구 설명의 바닥글 화살표 드릴스루 합니다.
3. 드릴스루에 대 한 화살표를 탭 합니다.

    ![드릴스루를 탭 합니다.](././media/mobile-apps-view-phone-report/report-drill-through1.png)

4. 드릴스루 보고서 페이지를 선택 합니다.

    ![보고서 페이지를 선택 합니다.](././media/mobile-apps-view-phone-report/report-drill-through2.png)

5. 앱 헤더에서 시작 페이지로 돌아가려면 뒤로 단추를 사용 합니다.


## <a name="next-steps"></a>다음 단계
* [Power BI 휴대폰 앱에 대해 최적화된 보고서 만들기](../../desktop-create-phone-report.md)
* [Power BI에서 대시보드 휴대폰 보기 만들기](../../service-create-dashboard-mobile-phone-view.md)
* [모든 크기에 최적화된 반응형 시각적 개체 만들기](../../visuals/desktop-create-responsive-visuals.md)
* 궁금한 점이 더 있나요? [Power BI 커뮤니티에 질문합니다.](http://community.powerbi.com/)

