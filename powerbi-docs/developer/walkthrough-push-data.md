---
title: 데이터 세트에 데이터 푸시
description: Power BI 데이터 세트에 데이터 푸시
author: rkarlin
ms.author: rkarlin
manager: kfile
ms.reviewer: madia
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 05/22/2019
ms.openlocfilehash: 9eb81610044f795b6f9dc5c58aeefad13de06542
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66222152"
---
# <a name="push-data-into-a-power-bi-dataset"></a>Power BI 데이터 세트에 데이터 푸시

Power BI API를 사용 하면 Power BI 데이터 집합에 데이터를 푸시합니다. 이 문서에서는 살펴보겠습니다 기존 데이터 집합에는 Product 테이블을 포함 하는 Sales Marketing 데이터 집합을 푸시하는 방법.

Azure Active Directory (Azure AD)를 시작 하기 전에 해야으로 [Power BI 계정](create-an-azure-active-directory-tenant.md)합니다.

## <a name="steps-to-push-data-into-a-dataset"></a>데이터 세트에 데이터를 푸시하는 단계

* 1단계: [Azure AD에 앱 등록](walkthrough-push-data-register-app-with-azure-ad.md)
* 2단계: [인증 액세스 토큰 가져오기](walkthrough-push-data-get-token.md)
* 3단계: [Power BI에서 데이터 세트 만들기](walkthrough-push-data-create-dataset.md)
* 4단계: [Power BI 테이블에 행을 추가할 데이터 세트 가져오기](walkthrough-push-data-get-datasets.md)
* 5단계: [Power BI 테이블에 행 추가](walkthrough-push-data-add-rows.md)

다음 섹션에서는 데이터를 푸시하는 Power BI API 작업에 대한 일반적인 내용을 설명합니다.

## <a name="power-bi-api-operations-to-push-data"></a>데이터를 푸시하는 Power BI API 작업

Power BI REST API를 사용하여 데이터 원본을 Power BI로 푸시할 수 있습니다. 앱 데이터 집합에 행을 추가 하면 대시보드 타일을 자동으로 새 데이터로 업데이트 합니다. 데이터를 푸시 하려면 사용 합니다 [PostDataset](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postdataset) 하 고 [PostRows](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postrows) 작업. 데이터 집합을 찾으려면 다음을 사용 합니다 [데이터 집합 가져오기](https://docs.microsoft.com/rest/api/power-bi/datasets/getdatasets) 작업 합니다. 이러한 작업에 대 한 그룹을 사용 하 여 작업 그룹 ID를 전달할 수 있습니다. 그룹 ID 목록의 사용 합니다 [그룹 가져오기](https://docs.microsoft.com/rest/api/power-bi/groups/getgroups) 작업 합니다.

데이터 세트에 데이터를 푸시하는 작업은 다음과 같습니다.

* [PostDataset](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postdataset)
* [데이터 세트 가져오기](https://docs.microsoft.com/rest/api/power-bi/datasets/getdatasets)
* [행 게시](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postrows)
* [그룹 가져오기](https://docs.microsoft.com/rest/api/power-bi/groups/getgroups)

Power BI에서 데이터 세트를 만들려면 Power BI 서비스에 JSON(JavaScript Object Notation) 문자열을 전달합니다. JSON에 대한 자세한 내용은 [JSON 소개](http://json.org/)를 참조하세요.

데이터 세트에 대한 JSON 문자열의 형식은 다음과 같습니다.

**Power BI 데이터 세트 JSON 개체**

    {"name": "dataset_name", "tables":
        [{"name": "", "columns":
            [{ "name": "column_name1", "dataType": "data_type"},
             { "name": "column_name2", "dataType": "data_type"},
             { ... }
            ]
          }
        ]
    }

Sales Marketing 데이터 집합 예제를 아래와 같이 JSON 문자열로 전달 합니다. 이 예에서 **SalesMarketing** 은 데이터 집합 이름, 및 **제품** 테이블 이름입니다. 테이블을 정의한 후 테이블 스키마를 정의할 수 있습니다. **SalesMarketing** 데이터 세트의 경우 테이블 스키마는 다음 열을 포함합니다. ProductID, Manufacturer, Category, Segment, Product 및 IsCompete.

**예제 데이터 세트 개체 JSON**

    {
        "name": "SalesMarketing",
        "tables": [
            {
                "name": "Product",
                "columns": [
                {
                    "name": "ProductID",
                    "dataType": "int"
                },
                {
                    "name": "Manufacturer",
                    "dataType": "string"
                },
                {
                    "name": "Category",
                    "dataType": "string"
                },
                {
                    "name": "Segment",
                    "dataType": "string"
                },
                {
                    "name": "Product",
                    "dataType": "string"
                },
                {
                    "name": "IsCompete",
                    "dataType": "bool"
                }
                ]
            }
        ]
    }

Power BI 테이블 스키마에는 다음과 같은 데이터 형식을 사용할 수 있습니다.

## <a name="power-bi-table-data-types"></a>Power BI 테이블 데이터 형식

| **데이터 형식** | **제한 사항** |
| --- | --- |
| Int64 |Int64.MaxValue 및 Int64.MinValue는 허용되지 않습니다. |
| Double |Double.MaxValue 및 Double.MinValue 값은 허용되지 않습니다. NaN 지원 되지 않습니다. + Infinity 및-Infinity는 일부 함수 (예: Min, Max)에서 지원 되지 않습니다. |
| Boolean |없음 |
| Datetime |데이터 로드 동안 일 분수가 1/300 초 (3.33ms)의 배수에 대를 사용 하 여 값 양자화 합니다. |
| String |현재 최대 128k 자를 허용합니다. |

## <a name="learn-more-about-pushing-data-into-power-bi"></a>Power BI에 데이터 푸시에 대해 자세히 알아보기

데이터 세트에 데이터 푸시를 시작하려면 왼쪽 탐색 창에서 [1단계: Azure AD에 앱 등록](walkthrough-push-data-register-app-with-azure-ad.md)을 참조하세요.

[다음 단계 >](walkthrough-push-data-register-app-with-azure-ad.md)

## <a name="next-steps"></a>다음 단계

[Power BI에 등록](create-an-azure-active-directory-tenant.md)  
[JSON 개요](http://json.org/)  
[Power BI REST API 개요](overview-of-power-bi-rest-api.md)  
궁금한 점이 더 있나요? [Power BI 커뮤니티를 이용하세요.](http://community.powerbi.com/)