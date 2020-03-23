# PortFolio

안녕하세요! 

첫 개발입니다.

국비학원에서 진행한 프로젝트 포트폴리오 입니다.

6명의 팀으로 구성되어 프로젝트를 진행 하였고, 제가 맡은 모듈만 설명하려합니다.

● 프로젝트 주제 : 영화 프랜차이즈 3사 통합 예매 서비스 MOVMOVMOV

● 서류를 제외한 프로젝트 실제 개발 기간 : 2020.01.28 ~ 2020.03.11 (1개월 15일)

● 총 개발 인원 : 6명

● 시스템 개요 : 기존의 잘 알려진 영화 예매 사이트 ( CGV, 롯데시네마, 메가박스 )는 해당 프랜차이즈사 웹페이지를 이용하지 않으면,
               예매정보 확인이 불가능하므로, 이 불편함을 해소하고자, 이 3사의 영화 예매 정보를 한눈에 비교하고, 영화를 예매할 수 있는 서비스 제공을 목표로하는 웹을 제작하기로 하였습니다.

● 기술적 고려사항 :
 
    ■ Web Application Architecture  
      – 2Layer / MVC 
    ■ Front End  
      – HTML5 / CSS3 / Bootstrap / javascript / jQuery / Ajax / Datepicker / FulCalendar / summernote/ Moment.js 
        Font Awesome / DWL Carousel / Google Font / sweet Alert  
    ■ Back End 
      – Java / Spring Framework / Mybatis / Apache / ApacheTomcat 
    ■ DB / Tool  
      – selenium / oracle / starUML / OvenApp.io / eclipse / GitHub / DBeaver  
    ■ Open API  
      – SNS로그인 : 네이버 / 카카오 / 구글  
      –SMS(문자서비스) : 청기와랩  
      –Email : javaMail  
      –결제 : 아임포트  
      –Map : 카카오맵 
      –영화정보 : KMDb (한국영화데이터베이스) / KOBIS(한국영화진흥원) / 네이버(서치) / Youtube 
             
● 업무 영역 :


     ■ 회원 관리 시스템
     
     
     ■ 마이페이지 
     
     
     ■ 영화 관리 시스템
     
     
     ■ 영화 예매 시스템  
     
     
     ■ 스토어 시스템 
     
     
     ■ 결제 시스템 
     
     
     ■ 이벤트 시스템  
     
     
     ■ 고객센터 시스템
     
     
   
 그 중 **저는 시스템 핵심인 극장별 비교예매가 있는 영화 예매 시스템을 맡았습니다.** 
 
 간단한 특징은 다음과 같습니다. 
 
 예매 시스템의 **실질적인 개발기간은 3주** 입니다. 
 
 개발하다가 다른 모듈의 개발속도 문제로, 적정선에서 중단하고 **완벽구현하지 않았습니다.**
 
 **프론트는 HTML5, CSS3, 제이쿼리+자바스크립트** 로 모두 작성하였습니다.  
 
 **백엔드는 자바+스프링 프레임워크, 오라클과 마이바티스**로 작성하였습니다.
 
  # 영화 예매 시스템 특징
   
   
  
   ### -- 예매 정보 선택 --
   
   
    1. 일반 예매, 극장별 비교 예매기능을 제공합니다.
    
    
    2. 영화, 상영관, 프랜차이즈, 날짜를 자유롭게 선택하고, 모두 선택하는 경우 상영시간 선택이 가능합니다.
    
    
    3. 특정 항목 선택 시, 다른 항목들이 정렬됩니다.
    
    
      ( 예로 영화를 선택했는데, 그 영화를 상영하지 않는 프랜차이즈 혹은 날짜는 OPACITY가 변하고, 하단 정렬됩니다. )
      
      
    4. 상영시간 데이터는 일주일을 기준으로 합니다. (크롤링 1번 할 경우)
    
    
    5. 지속적으로 데이터를 추가 할 경우, 상영시간 중복처리를 하지않았습니다.
    
    
    6. 모든 영화 데이터는 맥스무비 https://ticket.maxmovie.com/Reserve/Date 의 날짜 선택 영역에서 모두 크롤링해왔습니다.
    
    
       
   ### -- 좌석 선택 --    
   
   
    1. 관객 타입은 청소년, 일반, 우대가 있습니다
    
    
    2. 좌석 타입은 economy, standard, prime, sweetBox가 있습니다.
    
    
    3. 좌석은 총 130석 고정 구현하였습니다, 각 프랜차이즈별 그리고 상영관별로 총 좌석수와 타입이 전부 다르나, 이것이 로직이
    
    
       있는게아니라, 실제 건물에 맞춰 제작됐기때문에 규칙성이 없다는것을 파악했습니다. 수동입력입니다. 구현이 더 중요했고,
       
       
       중요한게 아니라서 모두 고정 좌석수를 가집니다.
       
       
    4. 좌석 선택 시 인원수가 1명이나 혹은 2명이상이냐에 따라 마우스 온오버, 클릭 이벤트가 다르게 작동합니다.
    
    
    5. 1명은 자유롭게 다시선택 가능하나, 2명이상은 중간에는 다시선택가능하나 모두 선택했다면, 다시 선택 버튼 혹은 인원수를 재 선택하여       
       초기화 해야합니다. 
       
       
    6. 인원수 재 선택시 선택한것이 초기화됩니다.
    
    
    7. 청소년, 일반, 우대가 다수 선택됐다면 앞에서부터 2명씩 처리합니다. 로직은 아래에서 자세히 설명합니다.
    
    
    8. 지금 선택하려는 관객타입, 좌석타입에 따라서 가격을 다르게 저장합니다. 로직은 아래에서 자세히 설명합니다.
    
    
  
  
  
  # 영화 예매 시스템 로직
  
  예매 선택부분은 크게 어렵지 않다고 생각이 들어서, 좌석선택부분만 설명하려합니다.  
  
  관객타입을 객체로 각각 정리합니다, 객체는 그 속성값으로 가격, 좌석 등급등을 가지고 있고, 메소드를 정의하여, 
  
  메소드 실행 시 가격값, 좌석등급 값이   달라집니다. **인원수에서 선택한 관객타입, 그 숫자를 배열로 저장합니다.**
  
  이해하기 어려우니 설명하자면
  
  인원수에서 청소년 2명, 일반 2명, 우대 2명을 선택했다면
  
  var totalArray = [ new 청소년, new 청소년, new 일반, new 일반, new 우대, new 우대 ]
  
  가 들어있다고 생각하시면되겠습니다.
  
  1명이냐 2명이냐에따라서, 배열 내부 index에따라서 2명씩 처리하면됩니다.
  
  **즉, 첫 좌석 클릭할 경우 그 정보에 따라, 배열 내 인덱스0부터 2명의 가격,좌석등급이 결정됩니다.**
  
  이후 인덱스를 2옮겨 일반 처리를 합니다. 이걸 끝까지 반복합니다.
  
  **단, 배열의 길이가 전체 2이상이고 홀수라면, 2씩 옮길경우 오류가 발생하기때문에,**
  
  **홀짝 여부를 체크해서 마지막에는 1칸만 옮겨줘야합니다.**
  
  이거 외에도 고려할것이 있습니다.
  
  
  바로 ***선택 도중 선택 해제 할 경우*** 입니다.
  
  1명 일 경우는 아무 문제 없으나, 2명 이상 일 경우 고려해봐야할 것이있습니다.
  
  30명을 선택해야하는데 거기서 24명 선택도중 6명을 취소했다면, 취소한 인원을 다시선택할 수 있게 해줘야합니다
  
  위를 이용해 설명하자면
  
   [ new 청소년, new 청소년, new 일반, new 일반, new 우대, new 우대 ]  에서  일반만 취소했다면 
   
   일반만 다시선택 할 수 있게 해줘야합니다.
   
   이게 무작위로 취소했다면 고려할 것이 많아집니다. 
   
   저는 이것을 이렇게 해결했습니다.
   
   1. 총 선택해야할 선택횟수를 지정합니다. 선택 시 좌석에 그 선택 순서가 표시됩니다. ( [ex] A1,A2 좌석에 Sequence0 )
   2. 전 좌석에서 선택된 부분만을 반복문을 돌려 모두 체크합니다.  
   3. 체크된 경우, 선택한 객체를 따로 배열로 저장하고 초기의 전체 배열과 비교하여 선택되지 않은 index를 sequence로 가집니다.  
   4. 이를 취소하거나, 선택할 경우 매번 체크합니다. 그럼 어떤 시퀀스 몇을 취소했든 배열내에서는 그 해당값을 찾을 수 있게됩니다. 
   
      예로 시퀀스 1,2,3,4,5 에서 1,2,3,4 선택 도중 2,3 시퀀스 부분을 취소하면
      
      선택되지 않은 시퀀스가 2,3,5 이므로 2부터 돌아가 다시 선택가능한것입니다. 
      
      4는 이미 선택했으므로 4는 넘어가고 2,3선택 후 5선택가능합니다.  
   
  
  
  # 시스템의 문제점
  
  1. 웹소켓으로 구현하려했으나, 팀원과 상의한 결과 Ajax로 구현하게 됐습니다. 실시간으로 좌석정보를 받지 않습니다.
  
     단, 주기적으로 요청받을 수 있는 코드는 짜놨습니다. 주석 처리해놨습니다. 자바스크립트 setInterval로 처리했습니다.
     
  2. 크롤링 데이터를 기반으로 하기때문에, 크롤링하는 사이트가 마비되면 데이터를 가져올 방법이 없습니다.  
  
  3. 그 당시 영화정보를 담당했던 조원이 일이 있어, 개발속도를 맞추지 못하여 크롤링 시 영화 데이터와 상영정보 데이터가 따로있습니다. 
  이것이 무슨말이냐면
  
     영화정보 크롤링 -> 그 기반의 데이터로 상영시간 데이터를 저장 해야 하는데
     
     영화 정보 크롤링 따로, 상영시간 정보 따로 크롤링합니다. 아쉽습니다.
     
  4. 동기화 문제를 체크하지 못했습니다. java로 개발하기때문에 syncrhonized를 붙이긴했지만 제대로 테스트 해보진 않았습니다.
     이에 대해 제대로 알지도 못하고 있습니다. 
     개발시간이 조금 더 있었다면 제대로 체크해 볼 수 있었다고 생각합니다. 조금 아쉽습니다.
     
     
     
  # 조금 아쉬웠던 점
  
  1. 백엔드보다는 프론트엔드 실력이 상대적으로 늘었습니다. 
  
     자바, 스프링보다 자바스크립트와 함께한 시간이 조금 더 많았던 것 같습니다.  
  
  2. 제가 맡은 모듈 이외에 다른 팀원들의 모듈도 해보고 싶다는 생각이 들었습니다. 
     
  
  
  # 프로젝트를 진행하면서 배운점
  
  1. 실질적인 코드 구현 이외에도 분석이나 설계등의 프로젝트 전반적인 진행과정을 이해하게 되었습니다.
  
  2. 자바스크립트의 동기/비동기 처리를 이해할 수 있게 되었습니다.  

  3. 개인적인 생각으로는, 백엔드만큼이나 프론트도 상당히 어려운 것 같습니다.

  4. 팀 프로젝트를 진행하면서, 협업의 중요성을 깨달았습니다. 
  
     팀원들 서로간의 끊임없는 소통과 배려가 반드시 필요한 것 같습니다. 
