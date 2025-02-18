---
ms.openlocfilehash: d7f30dd43fe875380939520f3dc54fcbbe2f4c9c
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2019
ms.locfileid: "61273659"
---
**DAX** 및 Excel 수식 언어 간의 중요한 차이점은 DAX를 사용하여 단일 값으로 제한되는 것이 아니라 식 사이에 전체 테이블을 전달할 수 있다는 점입니다.  DAX를 사용하는 경우 한 가지 강력한 효과는 해당 식에서 테이블을 필터링한 다음 필터링된 일련의 값으로 작업할 수 있다는 점입니다.

![](media/7-6-dax-tables-and-filtering/dax-tables-filtering_1.png)

DAX를 사용하면 완전히 새로운 계산 테이블을 만들 수 있으며 데이터 모델에서 해당 테이블과 다른 테이블 간의 관계를 만드는 것을 포함하여 다른 테이블처럼 다룰 수 있습니다.

## <a name="dax-table-functions"></a>DAX 테이블 함수
DAX에는 다음을 포함하여 풍부한 **테이블** 기능이 있습니다.

* FILTER
* ALL
* VALUES
* DISTINCT
* RELATEDTABLE

이러한 함수는 값이 아닌 전체 테이블을 반환합니다. 일반적으로 최종 값을 반환한 테이블을 사용하지 않고 추가 분석에서 **테이블** 함수의 결과를 더 규모가 큰 식의 일부로 사용할 수 있습니다. 테이블 함수를 사용하는 경우 결과는 해당 열 관계를 상속해야 합니다.

각 식에서 테이블을 사용하고 테이블을 반환하면 식에서 테이블 함수를 혼합할 수 있습니다. 예를 들어, 다음 DAX 식을 살펴봅니다.

    FILTER (ALL (Table), Condition)

해당 식은 현재 필터 내용을 무시하고 전체 테이블을 필터링합니다. 

DISTINCT 함수는 현재 컨텍스트에서도 볼 수 있는 열의 고유 값을 반환합니다. 따라서 위의 DAX 식 예제를 사용하기 위해 해당 식에서 **ALL**을 사용하면 필터를 무시하는 반면 **ALL**을 **DISTINCT**로 대체하면 관찰합니다.

## <a name="counting-values-with-dax"></a>DAX를 사용하여 값 계산
Power BI 보고서 작성기가 대답을 원하는 한 가지 일반적인 질문은 다음과 같습니다.

* 이 열에 있는 값의 개수는 몇 개인가요?

이는 사용자 앞에 표시된 테이블을 통해 답변할 수 있는 간단한 질문일 수 있지만 DAX에서는 특히 테이블 간에 관계가 있는 경우 다른 방식으로 접근합니다.

예를 들어 Power BI와 DAX는 제대로 교차 인덱싱되지 않은 값을 포함합니다. 들어오는 관계가 중단된 경우 DAX는 모든 필드에서 공백이 있는 관련 테이블에 새 행을 추가하고 해당하는 새 행을 인덱싱되지 않은 행에 연결하여 참조 무결성을 보장합니다. **ALL**을 사용하는 경우처럼 함수에 빈 행이 포함되면 해당하는 비어 있는 행은 해당 열에 반환된 값의 개수에 포함됩니다.

DAX 함수를 사용하여 전체 계산 테이블을 만들 수도 있습니다. DAX를 사용하여 만든 계산 테이블에는 **NAME** 및 **TABLE** 함수가 필요합니다. 계산 테이블은 관계를 설정하는 등 다른 테이블처럼 사용할 수 있습니다.

> [Alberto Ferrari, SQLBI](http://www.sqlbi.com/learning-dax)의 비디오 콘텐츠 출처
> 
> 

