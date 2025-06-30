<p align="center">
  <a href="https://www.uit.edu.vn/" title="University of Information Technology" style="border: none;">
    <img src="https://i.imgur.com/WmMnSRt.png" alt="University of Information Technology | University of Information Technology">
  </a>
</p>

<h1 align="center"><b>IE104.P11 - Internet and Web Technology</b></h1>

## Team Members:
| **No.** | **Student ID** | **Full Name**       | **Role**       | **Email**                   |
| ------- | -------------- | ------------------- | -------------- | --------------------------- |
| 1       | 22521172       | Vo Nhat Phuong      | Team Leader    | 22521172@gm.uit.edu.vn      |
| 2       | 22521641       | Nguyen Dang Huong Uyen | Member     | 22521641@gm.uit.edu.vn      |
| 3       | 22520298       | Le Nguyen Thuy Duong | Member        | 22520298@gm.uit.edu.vn      |
| 4       | 22520861       | Hoang Gia Minh       | Member        | 22520861@gm.uit.edu.vn      |
| 5       | 22521121       | Le Thien Phuc        | Member        | 22521121@gm.uit.edu.vn      |

## Course Introduction:
* **Course Name:** Internet and Web Technology  
* **Course Code:** IE104.P11  
* **Academic Year:** Semester 1 (2024 - 2025)  
* **Instructor:** MSc. Vo Tan Khoa  


# **:memo:MELON - Online Movie Streaming Website**

**MELON** is a modern online movie streaming website, delivering a great entertainment experience with a user-friendly interface and smart features. Explore a rich movie library and easily save your favorite titles.

---
## 🎬 Key Features

- **🎥 High-Quality Streaming**: Smooth movie-watching experience with multiple quality options.  
- **❤️ Favorites List**: Save your favorite movies for later viewing with ease.  
- **📜 Watch History**: Keep track of your watch history — never miss a thing.  
- **⏰ Sleep Timer**: Set reminders to sleep, helping you manage your time even while enjoying movies.  
- **🌐 Social Sharing**: Easily share your favorite films via social media or QR code.  
- **💎 VIP Subscription**: Unlock unlimited access with the VIP membership package.  
- **💬 Comments and Ratings**: Join the community in reviewing and discussing films.  
- **🔍 Smart Search**: Find films quickly with smart filters.  
- **🎞️ Movie & Show Library**: Continuously updated with hundreds of movies and exciting shows like *2 Days 1 Night*, *Hello Brother*, etc.  
- **🤖 Smart Chatbot**: Get information, ask questions, and receive assistance from our chatbot.

## ⚙️ System Requirements
- **🟢 Node.js**: Version 16 or higher to ensure compatibility with libraries and frameworks.  
- **📦 npm**: Package manager to install project dependencies.

## 📚 Technologies Used
- **React.js**: Version 16+ for compatibility with modern libraries and tools.  
- **Tailwind CSS**: Utility-first CSS framework for rapid and beautiful UI development.  
- **Firebase**: For online data storage, real-time database, Firestore, and authentication.  
- **Momo Payment**: Integrated for fast, online payments through Momo.  
- **Ngrok**: Creates forwarding URLs for development and external testing.  
- **Python**: Used for chatbot development with libraries like `nltk`, `transformers` for NLP tasks.  
- **Node.js**: JavaScript runtime for backend development and building RESTful/WebSocket APIs.

## 📂 Project Directory Structure
```
├── vs/                    # System support resources.
├── Data/                  # Source data or datasets.
├── chipmunk/segmenter     # Text segmentation tools.
├── experimental/          # Experimental and incomplete code.
├── languages.shorttext/   # Resources for short text processing.
├── languages/             # Language resources for NLP models.
├── lemming/lemma/         # Lemmatization tools.
├── marmot/                # Data processing tools.
├── net/arnx/jsonic/       # Network and JSON libraries.
├── public/                # Static resources (images, CSS, JS).
├── server/                # Server source code (Momo).
├── src/                   # Main source code.
│   ├── Chatbot/           # Chatbot functionality.
│   ├── Components/        # UI components.
│   ├── Context/           # State management.
│   ├── Data/              # Data helpers and search filters.
│   ├── Layout/            # UI layouts.
│   ├── Screens/           # Application screens.
├── src_vn/                # Vietnamese language resources.
├── vn/                    # Vietnamese language language resources.
├── .env                   # Environment variables.
├── .gitignore             # Git ignore file.
├── LICENSE                # Project license.
├── README.md              # Project documentation.
├── get-pip.py             # Pip installer.
├── log4j.properties       # Logging configuration.
├── package.json           # Node.js dependencies and info.
└── tailwind.config.js     # Tailwind CSS configuration.
```
## :clipboard: **Installation Guide**

1. **Download Source Code and Install Dependencies**  
   ```bash
   git clone https://github.com/vonhatphuongahihi/MOVIE-WEB
   cd MOVIE-WEB
   npm install aos firebase react-router-dom react-toastify styled-components react-icons classnames swiper 

2. **Setup Required Configurations**

   2.1. Install Ngrok
      - Visit [ngrok](https://ngrok.com/) and create an account.
      - Log in with your new account (or use Google login).  
      - In the **Setup & Installation** tab, select **Download** and get the version that fits your operating system. 
      - Extract the zip file and open `ngrok.exe`.

      2.2. Configure and run ngrok
      - Add your personal authentication token using the command:
   
         ```bash
         ngrok config add-authtoken $YOUR_AUTHTOKEN
         ```
      - Replace `$YOUR_AUTHTOKEN` with the token found in the **Your Authtoken** section.
      - Run the following command to create a forwarding URL:
         ```bash
         ngrok http 5000
         ```
      - Copy the forwarding URL shown under  **Forwarding**, e.g., `https://f53a-113-161-91-27.ngrok-free.app`.

      2.3. Configure ipnUrl
      - Open this file in Visual Studio Code:
   
           ```
           server/src/momo/momo_server.js
           ```
      - Go to line 40 and update the value of the `ipnUrl` variable with the forwarding URL you copied, keeping the `/callback` at the end. Save the file.

      2.4. Start the server
      - Open a new terminal and run:

         ```bash
         node .\server\src\momo\momo_server.js
         ```
3. **Install and Run Chatbot**

   3.1. Cài đặt Chabot
      - Navigate to the Chatbot folder:
   
         ```bash
         cd src/Chatbot
         ```
      - Install required Python packages:
      
         ```bash
         pip install transformers numpy sentence-transformers flask flask-cors
         ```
   3.2. Train and run the chatbot
      - Train the chatbot model:
          
         ```bash
         python train.py
         ```
      - Run the chatbot:
       
         ```bash
         python chat.py
         ```
      - Launch the chatbot with Flask:

        ```bash
         python chatbot.py
         ```
4. **Start the project**
  ```bash
   npm run start
  ```

## :rocket: **Upcoming Features**
- 🤖 Integrate AI-based movie recommendations based on user preferences
- 🌍 Support multiple languages
- 🌐 Deploy website on hosting
- 📱 Develop MELON mobile app
  
## :link: **Important Links**
- [Project GitHub Repository](https://github.com/vonhatphuongahihi/MOVIE-WEB)
- [MELON Website deployed on Vercel](https://melon-movie-web.vercel.app/)

## 📊 GitHub Stats
![GitHub stars](https://img.shields.io/github/stars/vonhatphuongahihi/MOVIE-WEB?style=social)
![GitHub forks](https://img.shields.io/github/forks/vonhatphuongahihi/MOVIE-WEB?style=social)
![GitHub issues](https://img.shields.io/github/issues/vonhatphuongahihi/MOVIE-WEB)
![GitHub pull requests](https://img.shields.io/github/issues-pr/vonhatphuongahihi/MOVIE-WEB)

## :email: **Contact**
If you have any questions or need support, please contact me via email: [vonhatphuongahihi@gmail.com](mailto:vonhatphuong@gmail.com).

