# XSSInspector
XSSInspector는 Reflected XSS 가능성이 존재하는 파라미터를 식별하는 도구입니다.

XSS Inspector is a tool that identifies parameters that exist for reflected XSS possibilities.

# Installation
https://github.com/RacilU/XSSInspector/releases

# Usage
1. 옵션을 선택합니다. (Select options.)
   
   http / https 둘 중 하나의 옵션을 선택합니다. 일부 서비스에선 https 연결을 지원하지 않기 때문에 http 옵션을 추가하였습니다.
   default 값은 https 입니다.
   
   Select either http / https option. We added the http option because some services do not support https connectivity.

   일부 서비스에선 request path를 응답 값에 그대로 포함시켜 반환하는 경우가 있습니다.
   이 경우 모든 파라미터가 공격 가능성이 존재하는 파라미터로 식별되기 때문에 각 파라미터에 대한 정확한 테스트가 어렵습니다.
   따라서 'Unique String Count (default : 1)' 값을 증가시켜 테스트를 수행해야합니다.
   해당 값은 응답 값에 포함되는 Unique String의 개수로, 2를 입력하게 될 경우 응답 값에 Unique String이 2개 이상인 경우에만 식별하겠다는 뜻입니다.

   Some services may return the request path in the response value.
   In this case, accurate testing for each parameter is challenging, since all parameters are identified as those in which the attack potential exists.
   So, the test should be carried out by increasing the value of 'Unique String Count (default: 1).
   This is the number of unique strings included in the response value, which means that if 2 is entered, the response value will only be identified if there are two or more unique strings.

   ![1](https://github.com/RacilU/XSSInspector/assets/168049442/ebe0a6fa-877f-476f-98b9-97ffb04591e9)

3. 취약점이 존재하는 파라미터를 식별합니다. (Identifies parameters where vulnerabilities exist.)
   
   ※ 해당 툴은 Burp Suite를 기반으로 개발되었기 때문에, Burp Suite 사용을 권장드립니다.
   
   ※ Because the tool was developed based on Burp Suite, I recommend using Burp Suite.

   1) Burp Suite Request를 복사합니다.
          
      Copy the Buff Suite Request.

   ![2](https://github.com/RacilU/XSSInspector/assets/168049442/a2370fb9-d729-415a-b55f-95cf6d13e68f)

   3) Text 필드에 붙여넣은 후, Search 버튼을 누릅니다.

      Paste into the Text field and press the Search button.

   ![3](https://github.com/RacilU/XSSInspector/assets/168049442/686ae7ca-3ea5-42f9-a733-254cdc2b5f24)

   3) 잠시 기다립니다.
      
      Please wait a moment.

   4) 취약한 파라미터가 출력됩니다. 해당 파라미터를 통해 Reflected XSS를 점검합니다.
      
      Vulnerable parameters are output.
      Check the Reflected XSS using the corresponding parameters.

   ![4](https://github.com/RacilU/XSSInspector/assets/168049442/f26e5635-241d-492f-a525-b6f66eec34f5)

   ![5](https://github.com/RacilU/XSSInspector/assets/168049442/6a7fece3-5a9d-41d6-bea5-a8c8df937e4c)

   ![6](https://github.com/RacilU/XSSInspector/assets/168049442/f7112fb1-26a2-4c78-9506-9f505959bdee)


# Upcoming update
- GUI
- XSS Attack
- json, xml

개선사항이나 문의는 아래 주소로 연락주세요! 감사합니다.

For any improvements or inquiries, please contact us at the address below! Thank you!

luke2005@naver.com.
