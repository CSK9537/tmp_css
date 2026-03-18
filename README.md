## 시스템 아키텍쳐
// Home Sweet Farm System Architecture

[Web Browser] {icon: chrome}
[Arduino Sensors] {icon: cpu}

Spring Backend {
  [Spring MVC] {icon: spring}
  [WebSocket] {icon: server}
  [MyBatis] {icon: database}
}

[Oracle DB] {icon: oracle}

// Data Flow
[Arduino Sensors] > [Spring MVC]: Sensor Data
[Web Browser] <> [Spring MVC]: HTTP Request / Response (JSP)
[Web Browser] <> [WebSocket]: Real-time Chat / Monitoring
[Spring MVC] > [MyBatis]: Data Mapping
[WebSocket] > [Spring MVC]: Sync
[MyBatis] <> [Oracle DB]: Read / Write
