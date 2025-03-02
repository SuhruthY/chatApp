# ChatApp - Real-Time WebSocket Chat Application

## 📌 Introduction
ChatApp is a real-time web chat application built with **Spring Boot**, **WebSockets**, and **STOMP** for backend communication, along with a **Bootstrap & JavaScript** frontend. This application enables users to exchange messages in real-time using WebSockets.

![chat-app test](https://github.com/SuhruthY/chatApp/blob/master/ChatAppTest.png)

## 🚀 Features
- **Real-time messaging** using Spring WebSockets & STOMP
- **Multiple users** can send and receive messages instantly
- **Dynamic UI updates** without refreshing the page
- **Bootstrap UI** for a responsive and clean chat interface
- **Enter key support** for quick message sending
- **Previous message fetching** (if database integration is added)

## 🛠️ Technologies Used
### Backend:
- **Java 8+**
- **Spring Boot** (Web, WebSocket, STOMP, Thymeleaf)
- **Maven** (Dependency Management)

### Frontend:
- **HTML, CSS, Bootstrap 5** (UI Styling)
- **JavaScript** (Client-Side Logic)
- **SockJS & STOMP.js** (WebSocket Communication)

## 📂 Project Structure
```
chatApp/
│── src/main/java/com/suhruth/ChatApp/
│   ├── controller/ChatController.java  # WebSocket Controller
│   ├── controller/model/ChatMessage.java  # Chat Message Model
│── src/main/resources/static/
│   ├── chat.html  # Chat UI
│   ├── test-image.png  # Test Image File
│── pom.xml  # Project Dependencies
│── README.md  # Project Documentation
```

## 📜 How It Works
1. **User opens the chat page (`/chat`).**
2. **WebSocket connection is established** when the page loads.
3. **Users enter their name & message** and press **Send** or hit **Enter**.
4. **Message is sent to the WebSocket endpoint** (`/app/sendMessage`).
5. **Spring Boot broadcasts the message** to all connected users via STOMP (`/topic/messages`).
6. **All clients receive and display the message instantly.**

## ⚙️ Setup & Run Locally
### 1️⃣ Clone the Repository
```sh
git clone https://github.com/SuhruthY/chatApp.git
cd chatApp
```
### 2️⃣ Build & Run the Application
```sh
mvn spring-boot:run
```
### 3️⃣ Open Chat Application
Visit **[http://localhost:8080/chat](http://localhost:8080/chat)** in your browser.

## 🔧 Future Enhancements
- ✅ Store chat history in a **database** (MySQL/PostgreSQL)
- ✅ Add **user authentication** (Spring Security)
- ✅ Improve UI with **real-time user presence indicators**

## 🤝 Contributing
Pull requests are welcome! Feel free to **fork** the repository and create new features. If you find any issues, please **open an issue**.

## 📄 License
This project is **open-source** under the MIT License.

---
💡 **Developed by [Suhruth Yambakam](https://github.com/SuhruthY/)** 🚀

