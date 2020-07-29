---
title: "Koodon - Internship Week 2-2 log"
date: "2020-07-26T22:40:32.169Z"
template: "post"
draft: false
slug: "summer-internship-2020"
category: "Internship"
tags:
  - "Python"
  - "Django"
  - "Backend"
  - "Web Development"
  - "Internship"
description: "A weekly log for my Software Engineering summer internship at Koodon - Week 2 - second log"
socialImage: "/media/42-line-bible.jpg"
---

![42-line-bible.jpg](/media/42-line-bible.jpg)

-	다만 데이터 관리 및 웹 서비스 보안에 대한 고민이 생겼다.
-	오늘은 스키마(데이터베이스) 모델링을 위주로 진행!

Day 2
-	경환님이 제안한 아이디어: 기존 고도몰 서버에서 판매 대행을 하는 방식(구글 타입폼 – 매뉴얼하게 고도몰 디비에 입력)을 우리가 개발할 판매 대행 엔드포인트 및 디비로 부분적으로 교체하면 어떻겠냐
-	해당 아이디어가 어려웠던 이유는, 고도몰에 저장된 쿠돈의 유저 디비를 우리가 가져올 방법이 없고, 그렇기 때문에 구매시/판매시 따로 로그인을 하거나 이중 로그인을 해야 하는 문제가 생김 – 고도몰 로그인 상태를 우리 판매 서비스를 이용할 때 유지할 수가 없음(연동 불가)
-	거기에 디비가 따로따로 쌓일테니, 차라리 첫 날 계획했던 대로 디비 및 서비스를 처음부터 새로 구축하는 것이 나음.

Day 3
-	프론트 개발 및 웹앱/서버에 대한 이해가 부족해서 그런지 경환님의 질문에 대답해드리기가 힘듬. 예리님 및 다른 멘토님들에게 도움을 구해서 어떻게든 답을 해 드리고, 내일 회의에서 의논할 내용을 정리하는 시간을 가짐.
-	공부할 것이 정말 많다.. 

1.	찜 리스트 - 선택 - 장바구니를 거치게 할 것인지 // 아닐지
-	눌렀을 때 상세 페이지로 가는 기능을 넣음
-	바로구매하는 기능 (장바구니를 안 거치는 것 – 해당 상품만 결제) 

2.	소셜 로그인을 할 때  여러 개의 계정이 중복된 전화번호/이메일을 가질때 이를 허용할지 (한 유저당 유효한 계정이 4개일 수 있음) – 허용하지 않는 걸로 (이메일 유효성/중복 여부 검사) check

3.	본인인증 (sms 인증) // 계좌 인증 등 – 유효한 유저인지 체크하는 외부 모듈/api 사용? E.g. T PASS, 1원 인증(1달러 인증) 등등

-	SMS 인증: 굳이 외부 모듈을 사용해서 보안성을 강화할 필요가 있느냐
-	개인정보 보관:
-	결제 보안: 네이버페이 등 외부 보안모듈 사용
-	입금받을 계좌는 처음에 받아서 그걸 계속 사용하게 할 수 있음
-	그러나 여러 개를 저장해서 선택하게 하고 싶지는 않음 (하나만으로)

-	수거 입력 정보 -> 유저에 저장 // 주소/연락처/이름 – 암호화

-	수거 

-	회원가입을 했을 때 고도몰에도 가입이 되고, 우리 DB에도 반영이 되었을 때 

4.	취소/교환/반품/환불 – 정책이 어떻게 되어 있는지. // 물품의 상태가 총 몇개가 있는지 (운영팀하고 논의할 사항)
-	취소: 사려고 했는데
-	환불: 결제까지 했는데 아직 배송 
-	반품: 사용자가 받고 다시 보내는 것 – 환불을 같이 적어줌

5.	판매 / 구매했을 시 모두 쿠돈에 대한 리뷰를 남길 수 있게 할 것인지 – 판매 대행을 맡기고 완료한 사람에게 리뷰를 요청하여 판매자 리뷰를 따로 만듬 (나중에 판단)
6.	선호 브랜드를 어떻게 설정할 것인지 (이 단계에서 선택할건지 / 찜 및 구매 이력 리스트에서 가져올건지)
-	선호 브랜드를 본인이 선택하게 하는 쪽으로 (발렌시아가 무슨 가방이 들어오면 알려주세요!) / 멀티 테이블 check

7.	% 기준인지 할인액인지 (할인액을 정하고 % 계산 – 앱 안에서 )

8.	판매대행 동의 저장? – 기록하기 (더 명확한 방어체계 하나 구축) – 4개의 컬럼을 두고 1,1,1,1을 전부 찍기



로그 테이블에 user_id // product_id 넣을지 아니면 컨텐츠에만 표시할지

구매 확정한 사람만 리뷰를 쓸 수 있게 할 것인지



본인인증 / 유효한 유저인지 체크하는 모듈이 있어야. (민감한 정보이기 떄문에)

1원 인증 (이 계좌가 이 실명에 해당하는지)

삭제된 유저는 제외하고 


선호 브랜드를 어떻게 설정할건지 (선택할건지 / 찜 및 구매 리스트에서 가져올건지)

취소 / 교환 / 반품 / 환불 - 정책이 어떻게 된 건지

프로덕트에 판매가별 수수료를 저장할건지

판매 / 구매했을 시 모두 리뷰를 쓸 수 있게 만들 것인지

% 기준인지 할인액인지

Extra:
판매 Admin 페이지 구성? (장고 UI?)





신청 완료 
검수 중
판매 중
판매 완료
회수 신청
회수 완료

Status가 바뀌면 잔디로 보낼 수 있게 하는 알림 (크리티컬한 status인 경우)



상품을 올리는 것은 고도몰 – 수거/배송

유저에 대한 정보를 마치 가입한 것처럼 암호화해서 저장 – 이미 판매대행 한 이력이 있으시네요? – 필요한 정보만을 받아서 가입 신청

(일단 아마존 서버에 판매대행한 사람들이 마치 회원가입한 유저처럼 위치하여 있어야 함)

사용자 – 판매 상태를 체크할 수 있도록

운영 – 어드민

고도몰과 유저 정보를 공유할 수 있을지 (솔루션

판매대행 신청 단계에서 전화번호와 이름을 받는 과정이 들어갈 것임. (고도몰에 로그인이 되어 있을 경우 키값을 가져와서 )

고도몰과 아마존 서버가 동기화가 되는지

판매대행 소개 페이지 숫자 동적으로 업데이트

판매소요 기간 (판매 처음 -> 판매 된 날짜 차이 계산)

브랜드 / 카테고리 데이터 csv로 수령 – 선택할 수 있는 카테고리 선택

Chanel(샤넬)이 아니라 Chanel, 샤넬


고도몰에서 비밀번호 및 계정 정보 이관 불가 // csv 파일로 밀어넣기 -> 패스워드 설정하게

전체 회원 전화번호 & 이메일 – 만약 전화번호가 있다면 sms 인증을 거쳐서 새로운 비밀번호를 설정하게 만듬 – 해당 계좌를 우리 DB에 저장.



The work environment here at **Koodon Inc.**, located in the middle of Gangnam District in Seoul, was way better than I thought! Even though it is a small startup having 6-10 employees in total, my fellow interns and I received our seats and tools we need, such as monitors.

I was very surprised since the company wants us, four software engineer interns, to build an entire website and mobile app that would replace its current website. AND **THERE IS NO PROGRAMMER in this team at the moment!**

This week, I have had several meetings, on daily basis, with entire staffs and fellow interns to talk about product design and to set up the timeline for this project.

I was wondering why the company wants to build its own website although their service has been active almost for a year (and quite successful).

The current website and mobile apps of Koodon were created under an e-commerce website solution, but the company wants to step out of the platform because both the CEO and a UX/UI designer believe changing User Interface is necessary to bring their business to the next level.

In this sense, even if this could be a little challenging mission for an unexperienced software developer, building/planning the web program that will be live on market from the scratch, I think this would be an interesting and rewarding journey to start on.

