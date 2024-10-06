# hanghae_week3

**예매하기**
```mermaid
flowchart TD
    A["토큰 발급 API"] -- UUID 및 대기열 정보 포함 --> B["토큰 발급 완료"]
    B --> C["대기열 정보 확인"]
    C --> D["예매창 입장 가능 여부 확인"]
    D -- NO --> E["대기열 유지"]
    D -- YES --> F["예약 가능 날짜 / 좌석 조회"]
    F --> G["좌석 예약 요청"]
    G --> H["좌석 선점 유무 확인"]
    H -- YES --> I["좌석 재선택"]
    H -- NO --> J["결제"]
    J --> K["좌석 임시 배정 만료 여부"]
    K -- NO --> L["좌석 예약 실패"]
    K -- YES --> M["좌석 예약 성공"]

    style E color:#FFFFFF, fill:#AA00FF, stroke:#AA00FF
    style I color:#FFFFFF, stroke:#2962FF, fill:#2962FF
    style L fill:#00C853,stroke:#00C853,color:#FFFFFF
