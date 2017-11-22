---
title: "Power BI Desktop에서 조건부 테이블 서식 지정"
description: "테이블에 사용자 지정된 서식 지정을 적용합니다."
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 5e5366b9f4ba8515f0fe6e2dc7fd0abe761bab8c
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/13/2017
---
# <a name="conditional-formatting-in-tables"></a>테이블에서 조건부 서식 지정
테이블에 대한 조건부 서식 지정을 사용하여 그라데이션 색 사용을 포함하는 셀 값을 기반으로 하는 사용자 지정된 셀 배경색을 지정할 수 있습니다. 조건부 서식 지정에 액세스하려면 Power BI Desktop에서 **시각화** 창의 **필드**에서 서식을 지정하려는 **값**의 값 옆에 있는 아래쪽 화살표를 선택합니다(또는 필드를 마우스 오른쪽 단추로 클릭). 필드에 대한 조건부 서식은 **필드**의 **값** 영역에서만 관리할 수 있습니다.

![](media/desktop-conditional-table-formatting/table-formatting_1.png)

대화 상자가 나타나면 색은 물론 *최소* 및 *최대* 값을 구성할 수 있습니다. **분기** 상자를 선택하면 선택적인 *가운데* 값도 구성할 수 있습니다.

![](media/desktop-conditional-table-formatting/table-formatting_2.png)

테이블에 적용되는 경우 위에 설명된 단계 사용에 적용된 사용자 지정된 서식 지정은 조건에 따라 서식 지정된 셀에 적용된 모든 사용자 지정 테이블 스타일을 재정의합니다.

![](media/desktop-conditional-table-formatting/table-formatting_3.png)

시각화에서 조건부 서식 지정을 제거하려면 필드를 다시 마우스 오른쪽 단추로 클릭하고 **조건부 서식 지정 제거**를 선택합니다.

![](media/desktop-conditional-table-formatting/table-formatting_4.png)
