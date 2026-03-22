# Distributed Programming Technologies

A collection of six university projects demonstrating progressive mastery of Java distributed and network programming - from low-level NIO file operations to enterprise messaging with JMS.

Built with **Java 17**.

## Projects

### TPO1 - File Processing with NIO

Recursive directory traversal and character encoding conversion utility. Walks a directory tree, reads files encoded in CP1250, converts them to UTF-8, and writes the concatenated result using `FileChannel`.

**Key concepts:** Java NIO, `FileChannel`, `ByteBuffer`, `CharBuffer`, `SimpleFileVisitor`, charset conversion

---

### TPO2 - Weather & Currency Desktop App

Hybrid Swing + JavaFX desktop application that fetches weather data from the OpenWeatherMap API and currency exchange rates from the NBP (Polish National Bank) API. Includes an embedded WebView browser for Wikipedia pages.

**Key concepts:** Swing/JavaFX interop, REST API consumption, GSON JSON parsing, multi-threading with `Platform.runLater`

---

### TPO3 - Translation Proxy Server

Socket-based proxy server that routes translation requests to dynamically registered language-specific servers (English, French, German). Clients connect through a JavaFX GUI.

**Key concepts:** Proxy pattern, service discovery, `ServerSocket`/`Socket`, `ExecutorService`, thread-per-client model, custom text protocol

---

### TPO4 - Pub/Sub Message Broker with NIO

Non-blocking publish/subscribe message broker built with Java NIO selectors. Publishers create topics and broadcast messages; subscribers receive them in real-time through a JavaFX GUI.

**Key concepts:** Reactor pattern, `Selector`, `SelectionKey`, `SocketChannel`, non-blocking I/O, topic-based pub/sub, `LinkedBlockingQueue`

---

### TPO5 - Car Database Web Application

Servlet-based web application backed by Apache Derby. Users query a car database through a form, and results are rendered as dynamic HTML tables. Deployed as a WAR on Tomcat.

**Key concepts:** Java Servlets, JNDI `DataSource`, Apache Derby, JSP/JSTL, Maven WAR packaging, `ResultSetMetaData`

---

### TPO6 - JMS Chat Application

Real-time multi-user chat application using Java Message Service over ActiveMQ. Messages are published to a shared JMS topic and delivered to all connected subscribers via a JavaFX GUI.

**Key concepts:** JMS `TopicPublisher`/`TopicSubscriber`, ActiveMQ, JNDI, message listeners, asynchronous messaging

---

## Technologies

| Category | Technologies |
|---|---|
| Language | Java 17 |
| GUI | JavaFX, Swing, FXML |
| Networking | Blocking sockets, Java NIO (non-blocking), HTTP Servlets, JMS |
| Data | GSON, Apache Derby, CSV, JNDI |
| Messaging | ActiveMQ, custom text protocols |
| Build | Maven, VS Code launch configurations |
| Server | Apache Tomcat |

## Running

Each project is self-contained in its own directory (`TPO{1-6}_PK_S20265`). Requirements vary per project:

- **TPO1–TPO4:** Compile and run with Java 17. JavaFX SDK required for GUI projects.
- **TPO5:** Build with Maven (`mvn package`), deploy the WAR to Tomcat with a running Derby instance.
- **TPO6:** Requires a running ActiveMQ broker on `localhost:61616`.

VS Code launch configurations are provided in `.vscode/launch.json` for convenience, including compound configurations for multi-process projects (e.g., server + client).
