graph TD
    subgraph "Hardware / IoT"
        A[Arduino Sensors<br>토양수분, 온도 등]
    end

    subgraph "Front-end (Client)"
        B[Web Browser]
        C[JSP / HTML / CSS / JS<br>UI & View Rendering]
    end

    subgraph "Back-end (Server)"
        D[Spring MVC<br>Business Logic & API]
        E[WebSocket<br>Real-time Chat & Data]
        F[MyBatis<br>ORM / Data Mapper]
    end

    subgraph "Database"
        G[(Oracle DB<br>Data Storage)]
    end

    %% 데이터 흐름
    A -- "센서 데이터 전송 (HTTP/Socket)" --> D
    B -- "페이지 요청 / API 호출" --> C
    C -- "HTTP Request / Response" --> D
    B <=="실시간 채팅 / 모니터링"==> E
    D <--> F
    F <--> G
    E -. "데이터 동기화" .- D
