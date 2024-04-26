# XSSInspector
XSSInspector는 Reflected XSS 가능성이 존재하는 파라미터를 식별하는 도구입니다.

XSS Inspector is a tool that identifies parameters that exist for reflected XSS possibilities.

# Usage
1. 옵션을 선택합니다.
   http / https 둘 중 하나의 옵션을 선택합니다. 일부 서비스에선 https 연결을 지원하지 않기 때문에 http 옵션을 추가하였습니다.
   default 값은 https 입니다.
   
   Select either http / https option. We added the http option because some services do not support https connectivity.

   일부 서비스에선 request path를 응답 값에 그대로 포함시켜 반환하는 경우가 있습니다.
   이 경우 모든 파라미터가 공격 가능성이 존재하는 파라미터로 식별되기 때문에 각 파라미터에 대한 정확한 테스트가 어렵습니다.
   이럴 경우 'Unique String Count (default : 1)' 값을 증가시켜 테스트를 수행해야합니다.
   해당 값은 응답 값에 포함되는 Unique String의 개수로, 2를 입력하게 될 경우 응답 값에 Unique String이 2개 이상인 경우에만 식별하겠다는 뜻입니다.



