---
title: Power BI 사용자 지정 시각적 개체를 개발하는 방법 문제 해결
description: 이 문서에서는 사용자 지정 Power BI 시각적 개체를 개발하거나 만들 때 발생할 수 있는 몇 가지 일반적인 문제에 대해 설명합니다.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 11/06/2018
ms.openlocfilehash: d6f3f654574e9cca081ae2f8191fd7b9fc017afd
ms.sourcegitcommit: 02f918a4f27625b6f4e47473193ebc8219db40e2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2018
ms.locfileid: "51223574"
---
# <a name="troubleshoot-power-bi-custom-visuals"></a>Power BI 사용자 지정 시각적 개체 문제 해결

## <a name="debug"></a>디버그

**Pbiviz 명령어가 없습니다(또는 유사한 오류)**

`pbiviz`를 터미널/명령줄에서 실행하는 경우 도움말 화면이 표시됩니다. 그렇지 않은 경우 개발자 도구가 올바르게 설치되지 않았습니다. 4.0 버전 이상의 NodeJS를 설치했는지 확인합니다.

**시각화 탭에 디버그 시각적 개체가 없습니다**

**시각화** 탭에는 프롬프트 아이콘처럼 보이는 디버그 시각적 개체가 있습니다.

![시각적 개체 선택 영역](media/power-bi-custom-visuals-troubleshoot/powerbi-developer-visual-selection.png)

디버그 시각적 개체가 보이지 않으면 Power BI 설정에서 사용할 수 있도록 설정되었는지 확인합니다.

> [!NOTE]
> 디버그 시각적 개체는 현재 Power BI 서비스에서만 제공되며, Power BI Desktop이나 모바일 앱에는 제공되지 않습니다. 패키징된 시각적 개체는 어디서나 변함 없이 작동됩니다.

**시각적 개체 서버에 연결할 수 없습니다**

시각적 개체 프로젝트의 루트에 있는 터미널 명령줄에서 `pbiviz start` 명령으로 시각적 개체 서버를 실행합니다. 서버가 실행 중인 경우 SSL 인증서가 올바르게 설치되지 않았을 수도 있습니다.

## <a name="next-steps"></a>다음 단계

자세한 내용 및 질문과 대답은 [Power BI 사용자 지정 시각적 개체에 대한 질문과 대답](power-bi-custom-visuals-faq.md#organizational-custom-visuals)을 참조하세요.