---
title: Power BI 보고서의 새 필터 환경(미리 보기)
description: Power BI의 필터에 새 기능과 새 디자인이 추가됩니다.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/16/2019
ms.author: maggies
LocalizationGroup: Reports
ms.openlocfilehash: 0a9e4986ae2f686eb8a8fd2d9fa07b169661ce60
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2019
ms.locfileid: "65853486"
---
# <a name="the-new-filter-experience-in-power-bi-reports-preview"></a>Power BI 보고서의 새 필터 환경(미리 보기)

Power BI에서 필터에 새로운 기능 및 새 디자인을 있습니다. 새 필터 환경으로 옵트인 하면 필터 창은 보고서의 나머지 부분을 같이 형식을 지정할 수 있습니다. 잠금 고도 필터를 숨길 수 있습니다. 보고서를 디자인할 때 시각화 창에서 전혀 이전 필터 창이 더 이상 표시 합니다. 모든 필터 편집 및 하나의 필터 창에서 서식 지정 하면 됩니다. 

![새 필터 환경](media/power-bi-report-filter-preview/power-bi-filter-reading.png)

> [!NOTE]
> 새 필터 환경은 미리 보기 상태입니다. 새 빌드는 이미 설정한 서식을 재정의할 수 있습니다.

보고서 디자이너는 다음과 같습니다. 새 단일 필터 창에서 수행할 수 있는 작업

- 추가 하 고 필터링 할 필드를 제거 합니다. 
- 필터 상태를 변경 합니다.
- 서식 지정 하 고 사용자 지정 필터 창에는 보고서의 일부 하다.
- 소비자가 보고서를 열 때 기본적으로 [필터] 창이 열려 있는지 또는 축소되어 있는지 여부를 정의합니다.
- 전체 필터 창 또는 보려는 보고서 소비자가 원하지 않는 특정 필터를 숨깁니다.
- 컨트롤 및 표시 유형, 심지어 책갈피를 연 상태의 새 필터 창 축소 됩니다.
- 소비자가 편집할 수 없도록 필터를 잠급니다.

새 필터 환경과 보고서 소비자가 또한 마우스로 가리키면 필터 또는 슬라이서는 시각적 개체에 영향을 주는 모든 읽기 전용 목록을 보려면 모든 시각적 개체입니다.

![시각적 개체에 대 한 필터 목록](media/power-bi-report-filter-preview/power-bi-filter-visual.png)

## <a name="turn-on-the-new-filter-experience"></a>새 필터 환경 설정 

Power BI Desktop에서 새 환경을 사용하도록 설정합니다. 그런 다음, 보고서나 Power BI 서비스(https://app.powerbi.com))에서 필터를 수정할 수 있습니다. 이 새 필터 환경은 미리 보기로 제공되므로 먼저 Power BI Desktop에서 사용하도록 설정해야 합니다. Power BI 서비스에서 보고서를 만들어 시작하면 새 필터를 사용할 수 없습니다.

### <a name="turn-on-new-filters-for-all-new-reports"></a>모든 새 보고서에 대해 새 필터 설정

1. Power BI Desktop에서 **파일** > **옵션 및 설정** > **옵션** > **미리 보기 기능**을 선택하고 **새 필터 환경** 확인란을 선택합니다. 
2. Power BI Desktop을 다시 시작하여 모든 새 보고서에서 새 필터 환경을 봅니다.

Power BI Desktop을 다시 시작한 후에는 사용자가 만드는 모든 새 보고서에 대해 기본적으로 새 필터를 사용할 수 있습니다.  

### <a name="turn-on-new-filters-for-an-existing-report"></a>기존 보고서에 대해 새 필터 설정

기존 보고서에 대해서도 새 필터를 사용하도록 설정할 수 있습니다.

1. 기존 보고서의 Power BI Desktop에서 **파일** > **옵션 및 설정** > **옵션**을 선택합니다.
2. 왼쪽된 탐색 모음에서 아래의 **현재 파일**를 선택 **설정을 보고**합니다.
3. 아래 **환경을 필터링**를 선택 **업데이트 된 필터 창 사용 하 고이 보고서에 대 한 시각적 개체 헤더에서 필터를 표시**합니다.

## <a name="view-filters-for-a-visual-in-reading-mode"></a>읽기 모드에 시각적 개체의 필터 보기

읽기 모드에서 시각적 개체의 필터 아이콘 위로 마우스를 올려 놓으면 해당 시각적 개체에 영향을 주는 모든 필터, 슬라이서 등이 포함된 팝업이 표시됩니다. 팝업의 형식 서식 지정 된 필터 창와 같습니다. 

![시각적 개체에 영향을 주는 필터](media/power-bi-report-filter-preview/power-bi-filter-per-visual.png)

다음은 이 보기에서 표시하는 필터 유형입니다. 
- 기본 필터
- 슬라이서
- 교차 강조 표시 
- 교차 필터링
- 고급 필터
- 상위 N 필터
- 상대 날짜 필터
- 슬라이서 동기화
- 포함/제외 필터
- URL을 통해 전달된 필터

## <a name="build-the-new-filters-pane"></a>빌드 새 필터 창

새 필터 창 사용 하도록 설정 하면 현재 보고서 설정에 따라 기본적으로 형식이 지정 된 보고서 페이지의 오른쪽에 참조 합니다. 새 필터 창을 사용 하 여를 포함 하 고 새 창에서 기존 필터를 업데이트 하는 필터를 구성 합니다. 새 필터 창에 어떤 보고서 소비자가 표시 됩니다 보고서를 게시 하는 경우를 보여 줍니다. 

1. 기본적으로 보고서 소비자 필터 창을 볼 수 있습니다. 이 확인 하도록 하지 않으려는 경우 눈 모양 아이콘 옆에 선택 **필터**합니다.

    ![Power BI 필터 눈 모양 아이콘](media/power-bi-report-filter-preview/power-bi-filter-eye.png)

2. 새 필터 창에 빌드를 시작 하려면 관심 분야로 새 필터 창에 시각적 개체에서 페이지도 끌거나 보고서 수준 필터입니다.

시각적 개체를 보고서 캔버스에 추가 하면 Power BI 시각적 개체의 각 필드에 대 한 필터 창에 필터를 자동으로 추가 합니다. 

## <a name="lock-or-hide-filters"></a>필터 잠그기 또는 숨기기

개별 필터 카드를 잠그거나 숨길 수 있습니다. 필터를 잠그면 보고서 소비자가 필터를 볼 수 있지만 변경할 수는 없습니다. 필터를 숨기면 볼 수도 없습니다. 일반적으로 필터 카드 숨기기는 null 또는 예기치 않은 값을 제외하는 데이터 정리 필터를 숨겨야 하는 경우에 유용합니다. 

- 새 필터 창에서 선택 하거나 선택을 취소 합니다 **잠금 필터** 또는 **숨기기 필터** 필터 카드의 아이콘입니다.

   ![필터 숨기기 또는 잠그기](media/power-bi-report-filter-preview/power-bi-filter-lock-hide.png)

새 필터 창에서 이러한 설정 및 해제를 설정한 보고서에 반영 된 변경 내용을 표시 됩니다. 숨겨진 필터는 시각적 개체의 필터 팝업에 표시되지 않습니다.

또한 보고서 책갈피를 사용 하 여 흐름에 새 필터 창 상태를 구성할 수 있습니다. 창의 열기, 닫기 및 표시 여부 상태에 모두 책갈피를 지정할 수 있습니다.
 
## <a name="format-the-new-filters-pane"></a>새 필터 분할 창 서식 지정

큰이 새로운 환경은 부분은 필터 창은 보고서의 모양과 느낌에 맞게을 형식을 지정할 수 있습니다. 필터 창은 보고서의 각 페이지 마다 다르게 서식을 지정할 수 있습니다. 다음은 서식을 지정할 수 있는 요소입니다. 

- 배경색
- 배경 투명도
- 켜거나 테두리
- 테두리 색
- 제목 및 헤더에서 사용 하는 글꼴, 색 및 텍스트 크기

적용 여부(설정됨) 또는 가용성(해제됨)에 따라 필터 카드에 대해 이러한 요소의 서식을 지정할 수도 있습니다. 

- 배경색
- 배경 투명도
- 테두리: 설정 또는 해제
- 테두리 색
- 글꼴, 색 및 텍스트 크기
- 입력 상자 색

### <a name="format-the-filters-pane-and-cards"></a>필터 창 및 카드 형식

1. 보고서에서 보고서 자체를 클릭하거나 배경(‘배경 화면’)을 클릭하고 **시각화** 창에서 **서식**을 선택합니다.  
    보고서 페이지, 배경 무늬, 필터 창 및 필터 카드 서식 지정에 대 한 옵션이 표시 됩니다.

    ![서식 아이콘 선택](media/power-bi-report-filter-preview/power-bi-filter-format.png)    

1. **필터 창**을 확장하여 배경, 아이콘 및 왼쪽 테두리의 색을 설정하여 보고서 페이지를 보완합니다.

    ![필터 창 확장](media/power-bi-report-filter-preview/power-bi-filter-format-pane-font.png)

1. **필터 카드**를 확장하여 **사용 가능** 및 **적용됨** 색과 테두리를 설정합니다. 사용 가능한 카드와 적용된 카드의 색을 다르게 만들면 적용되는 필터가 명확해집니다. 
  
    ![필터 카드 확장](media/power-bi-report-filter-preview/power-bi-filter-format-card-font.png)

## <a name="theming-for-filter-pane"></a>필터 창에 대 한 테마 설정
이제 테마 파일을 사용 하 여 필터 창의 기본 설정을 수정할 수 있습니다. 시작 하기 위한 샘플 테마 코드 조각은 다음과 같습니다.

 
```
"outspacePane": [{ 

"backgroundColor": {"solid": {"color": "#0000ff"}}, 

"foregroundColor": {"solid": {"color": "#00ff00"}}, 

"transparency": 50, 

"titleSize": 35, 

"headerSize": 8, 

"fontFamily": "Georgia", 

"border": true, 

"borderColor": {"solid": {"color": "#ff0000"}} 

}], 

"filterCard": [ 

{ 

"$id": "Applied", 

"transparency": 0, 

"backgroundColor": {"solid": {"color": "#ff0000"}}, 

"foregroundColor": {"solid": {"color": "#45f442"}}, 

"textSize": 30, 

"fontFamily": "Arial", 

"border": true, 

"borderColor": {"solid": {"color": "#ffffff"}}, 

"inputBoxColor": {"solid": {"color": "#C8C8C8"}} 

}, 

{ 

"$id": "Available", 

"transparency": 40, 

"backgroundColor": {"solid": {"color": "#00ff00"}}, 

"foregroundColor": {"solid": {"color": "#ffffff"}}, 

"textSize": 10, 

"fontFamily": "Times New Roman", 

"border": true, 

"borderColor": {"solid": {"color": "#123456"}}, 

"inputBoxColor": {"solid": {"color": "#777777"}} 

}] 
```

## <a name="sort-the-filter-pane"></a>정렬 필터 창

사용자 지정 정렬 기능은 새 필터 창 환경의 일부입니다. 보고서 작성자를 끌어서 원하는 순서 대로 다시 배치할 필터를 삭제할 수 있습니다.

![필터 정렬 순서를 다시 정렬](media/power-bi-report-filter-preview/power-bi-filter-sort.gif)

기본 정렬 순서는 필터에 대 한 사전순입니다. 사용자 지정 정렬 모드를 시작 하려면 방금 모든 필터를 새 위치로 끕니다. 만-예를 들어, 시각적 개체 수준, 페이지 수준 또는 보고서 수준 필터에 적용 되는 수준 내에서 필터를 정렬할 수 있습니다.

## <a name="filters-pane-scaling"></a>필터 창 크기 조정

새 필터 창 이므로 보고서 페이지 보고서 페이지 및 시각적 개체를 사용 하 여 배율을 하 고 서로 비율 창 유지 필터입니다.

## <a name="improved-filters-pane-accessibility"></a>향상 된 필터 창 내게 필요한 옵션

새 필터 창에 대 한 키보드 탐색을 개선 했습니다. 필터 창에는의 모든 부분을 통해 탭 하 고 키보드에서 Shift + F10 컨텍스트 키를 사용 하 여 상황에 맞는 메뉴를 열 수 있습니다.

![필터 창 내게 필요한 옵션](media/power-bi-report-filter-preview/power-bi-filter-accessible.png)

## <a name="rename-filters"></a>필터 이름 바꾸기
필터 창에서 편집할 때 제목을 편집을 두 번 클릭 합니다. 이름을 변경 하는 것은 최종 사용자에 대 한 더 잘 이해할 필터 카드를 업데이트 하려는 경우에 유용 합니다. 필터 카드 이름 바꾸기 명심 않습니다 *하지* 필드 목록의 필드의 표시 이름을 바꿉니다. 바로 필터 카드에 사용할 표시 이름을 변경 합니다.

![필터 이름 바꾸기](media/power-bi-report-filter-preview/power-bi-filter-rename.png)

## <a name="restrict-changes-to-filter-type"></a>필터 유형 변경 제한

Filtering 아래 사용자 필터 유형을 변경 하는 경우를 제어 하는 옵션이 있습니다 보고서 설정의 섹션을 경험 합니다.

![필터 유형 변경 제한](media/power-bi-report-filter-preview/power-bi-filter-restrict-change.png)

## <a name="next-steps"></a>다음 단계

새 필터 환경을 체험해 보세요. 이 기능 및 방법을 계속 수 있습니다를 향상에 대 한 피드백을 제공 합니다 [Power BI Ideas 사이트](https://ideas.powerbi.com/forums/265200-power-bi)합니다. 

- [보고서 필터를 사용하는 방법](consumer/end-user-report-filter.md)
- [필터 및 보고서에서 강조 표시](power-bi-reports-filters-and-highlighting.md)

궁금한 점이 더 있나요? [Power BI 커뮤니티를 이용하세요.](http://community.powerbi.com/)

