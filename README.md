# Irya Ilya 프로젝트 개발기⭐

https://www.kusedcar.store/

## 1. 프로젝트 배경

딜러인 친구의 차량 판매를 돕고 커미션을 얻기 위해 프로젝트를 시작했습니다.<br>
외국인을 대상으로 한 판매가 주요 목표였으며, 1인 개발자가 한국에서 전 세계의 외국인을 상대로 비즈니스를 수행할 수 있는 가능성을 실험해보고자 했습니다.

## 2. 기술 스택 선정과 이유

이 프로젝트는 저의 첫 웹 프로젝트로, 비용 절감과 유지보수 간소화를 최우선으로 고려했습니다.<br>
서버를 별도로 구축하지 않고, Next.js의 API 기능을 활용하였으며, 외부 서비스를 적극적으로 사용했습니다:

	• 프론트엔드: Next.js
	• 이미지 저장: Imgur
	• DB 서버: Google Sheets
	• 폼 데이터 저장: Airtable

초기에는 더 강력한 자동화를 위해 Apps Script 등의 기술도 시도했으나, 간단한 구조와 최소한의 기술만 사용하는 방향으로 전환했습니다.<br>
이 과정에서 불필요한 기술을 지양하고, 필요한 것에만 집중하는 방법을 배웠습니다.

## 3. 개발 기간

MVP(최소 기능 제품) 완성까지 7일이 소요되었습니다. 하루 종일 집중하여 작업한 결과입니다.

## 4. 개발 과정 중 겪었던 문제와 해결

비용을 최소화하면서 사이트를 유지하는 것이 가장 큰 도전이었습니다.<br>
수만 대의 차량 정보를 관리하려면 데이터베이스(DB) 프로그램이 필요한데, 클라우드 DB를 사용하면 비용이 청구될 가능성이 높고, 온프레미스 운영도 전기세 등의 유지비용이 발생할 수 있었습니다.<br>
따라서 비용 청구의 우려가 없으면서도 많은 데이터를 다룰 수 있는 대체 제품을 찾는 것이 초기의 큰 고민거리였습니다.

여러 옵션을 검토한 끝에 Google Sheets를 DB 대용으로 사용하기로 결정했습니다. Google Sheets는 무료로 제공되며, 일정량의 데이터를 관리하는 데 충분히 유용했습니다.

또한, 차량 정보를 업로드하는 데 드는 시간과 노력을 줄이기 위해 완전 자동화를 목표로 설계했습니다.<br>
외부 DB 프로그램에서 데이터를 선별해 가공한 뒤 Google Sheets와 Imgur에 업로드하고, 유효한 이미지 URL을 추출해 다시 Google Sheets에 최종 입력하는 방식이었습니다.<br>
그러나 이 방식은 실현 가능성이 낮아 보였고, 현재는 최소한의 수작업이 필요하도록 유지하고 있습니다.

앞으로는 이 자동화 프로세스를 네이버 카페와 같은 다른 플랫폼에 적용해볼 계획입니다.

## 5. 앞으로의 계획

이 프로젝트는 지속적으로 개발됩니다.<br>
Google 검색 결과와 Google Analytics 데이터를 분석하여, 필요에 따라 기능을 개선할 계획입니다.<br>
또한, 다국어 지원(러시아어, 폴란드어)과 외국인을 대상으로 한 네이버 카페 운영도 함께 진행하고 있습니다.

![Screenshot 2024-09-07 at 5 43 56 AM](https://github.com/user-attachments/assets/1839c82c-80b5-4b3a-a13a-84ee3c4532a2)

![Screenshot 2024-09-07 at 5 44 11 AM](https://github.com/user-attachments/assets/59c8318b-d303-4a47-9aae-3d39259e0537)

- Google Search Console 등록 완료, Google Analytics와 Vercel Analytics 적용 완료
- Infinite Scroll 적용(2024-09-17)

---
여기서부터는 편하게 기록한다.<br>
1. 관련 사업이 생각한대로 진행되지 않았다. 그래서 차량 등록을 제대로 할 수 없었기에 본 사이트가 놀고 있다.<br>
중고차 업계는 정말로 무시무시한 곳이다.<br>
아주 오래전부터 정말 많은 사람들이 중고차 시장에 블록체인 시스템을 도입하고자 했는데 왜 빠그라진 건지 너무나도 잘 알 것 같다.<br>
여기는 약간 야생의 거시기다. ㅋ<br>
블록체인 같은 걸로 '투명하게' 차량의 흐름이 기록되면 절대 안 된다.<br>
관계자들 어느 누구도 그런 거 원치 않는다.<br>
시스템이 그렇게 만들어지면 사람들이 돈을 못 번다.<br>
그래서 난 앞으로도 이 시장에 블록체인 시스템 같은 거 절대 못 들어올 거라 생각하고<br>
설사 누군가, 아니, 대기업이 그런 시스템을 돌린다 해도 성공하지 못 할 거라 생각한다.<br>

2. 처음에 나는 자동화 프로그램을 만들어 딜러 DB에서 데이터 추출하고 그걸 본 사이트든 어디든 자동으로 등록하려고 했는데<br>
내가 그렇게 써도 되는 차량, 안 되는 차량이 있었고<br>
차량을 얼마에 올릴지도 친구가 먼저 결정을 해야 했다.<br>
따라서 나는 어느 순간부터 본 사이트에 대한 개발을 멈췄다.<br>
즐거웠다.<br>
매물 정보만 좀 자유롭게 가져올 수 있으면 이건 여전히 해 볼 만한 작업이라 생각한다.<br>
문제는 DB였다.<br>
2024-11-29에 기록.<br>
---
