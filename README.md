# 🎭 My Musical Log (가제)

## 1. 프로젝트 개요

**My Musical Log**는 뮤지컬 관람 정보를 체계적으로 기록하고, 나중에 추억하거나 참고할 수 있도록 돕는 개인 기록용 안드로이드 앱입니다.

> 매 공연마다 프로그램북을 구매하기엔 비용이나 보관 문제 등 부담이 존재합니다. 또한 커뮤니티에 후기를 남기기엔 위치를 찾기 어렵고 글도 길어지기 쉽습니다.  
> 이에, 사용자가 원하는 방식으로 공연 정보를 간편하게 저장할 수 있는 앱을 만들고자 기획하게 되었습니다.

- **목적**: 뮤지컬 관람 기록 및 추억 보존
- **대상 사용자**: 뮤지컬을 자주 관람하는 모든 관객

---

## 2. 주요 기능

| 기능 | 설명 |
|------|------|
| 공연 정보 기록 | 공연 제목, 일시, 장소 입력 |
| 좌석 정보 기록 | 예매한 좌석 입력 및 저장 |
| 캐스트 정보 입력 | 주연 및 조연 배우 이름 입력 |
| 캐스트별 후기 | 배우별 개인 감상 메모 작성 |
| 넘버별 후기 | 특정 넘버(곡)에 대한 감상 기록 |
| 티켓 사진 업로드 | 예매 티켓 사진 업로드 (갤러리/카메라) |
| 포토존 사진 업로드 | 공연장 내 포토존 사진 첨부 |
| (확장) 배우별 통계 | 배우별 관람 횟수 통계 |
| (확장) 공연장 지도 연동 | 공연장 위치를 네이버 지도와 연동하여 표시 |

---

## 3. 화면 구성 (예정)

> 초기 단계이므로 아직 화면 설계는 미완료입니다. 다음과 같은 구성으로 발전 가능성이 있습니다.

- 홈: 기록된 공연 리스트 + 새 기록 추가 버튼
- 기록 추가 화면: 공연 정보, 배우, 좌석, 사진 첨부 등 입력
- 상세 화면: 전체 정보 + 후기 열람
- 통계/검색 화면 (확장)

---

## 4. 데이터 구조 (예시)

```java
class MusicalLog {
    String title;
    String date;
    String location;
    String seat;
    List<CastReview> castReviews;
    List<NumberReview> numberReviews;
    String ticketImagePath;
    String photoZoneImagePath;
}

class CastReview {
    String actorName;
    String role; // 주연 / 조연
    String review;
}

class NumberReview {
    String numberTitle;
    String review;
}
