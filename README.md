# hanghae_week3

**예매하기 FLOW CHART**
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
```

![image](https://github.com/user-attachments/assets/b3429db6-917d-4e08-8a19-ec517417edc6)

**[대기열 다이어그램 링크](https://www.mermaidchart.com/app/projects/100d9e03-3136-4578-90b4-2fa1d5595bb6/diagrams/95c31869-1abf-458c-85c6-bd54237bfb58/version/v0.1/edit)**

![image](https://github.com/user-attachments/assets/1151c654-f60d-4715-bca6-e8dfb2e014a9)

**[예매 다이어그램 링크](https://www.mermaidchart.com/app/projects/100d9e03-3136-4578-90b4-2fa1d5595bb6/diagrams/8e0b7df1-5377-4323-a58c-58b175e6dc05/version/v0.1/edit)**

![image](https://github.com/user-attachments/assets/75e47f7b-c13d-4a33-9adb-2e2938c4f930)

**[결재 다이어그램 링크](https://www.mermaidchart.com/app/projects/100d9e03-3136-4578-90b4-2fa1d5595bb6/diagrams/3d82a63e-9eb1-4a5a-8969-673014bd7d73/version/v0.1/edit)**
