# ⚡ Power Line Fault Logger

![Logger Screenshot](../assets/logger.png)

## 🚀 Overview
The **Power Line Fault Logger** is a web-based tool that allows users to efficiently record power line faults. It features:
- A **web-based interface** for selecting fault types
- **CSV logging** for fault reports
- **Real-time updates** with an Express.js backend
- **Observer & Depot management**
- **Downloadable reports** in CSV format
- **Server shutdown control**

## 🖥️ Web Interface
The frontend is a clean, structured UI built with **HTML, CSS, and JavaScript**, featuring:
- **Categorized fault buttons** (Poles, Crossarms, Conductors, etc.)
- **Modal pop-ups** for detailed fault specifications
- **Observer & Depot selection**
- **Connection status bar** to indicate server availability
- **Download CSV** and **Shutdown** buttons

🔗 **Live Demo:** 
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; background: #000;">
    <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" 
        src="https://www.youtube.com/embed/_0lU9sIuLnQ" 
        frameborder="0" allowfullscreen>
    </iframe>
</div>
📜 **Source Code:** [GitHub Repository](https://github.com/your-username/logger-app)

## 🔧 Installation & Setup

### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/your-username/logger-app.git
cd logger-app
```

### **2️⃣ Install Dependencies**
```sh
npm install
```

### **3️⃣ Run the Server**
```sh
node app.js
```
or, for live reloading:
```sh
nodemon app.js
```

### **4️⃣ Open the Web Interface**
```
http://localhost:3000
```
or access it from another device via:
```
http://YOUR_IP:3000
```

## 🎯 How It Works

### **Fault Logging**
1. Click a **fault category** (e.g., Pole, Crossarm, Conductor).
2. Choose a **specific fault type** from the pop-up modal.
3. The fault is logged automatically in the CSV file.

### **Setting Observer & Depot**
1. Click **"Set Observer"** to enter observer name.
2. Click **"Set Depot"** to enter depot name.
3. The values are stored and used for logs.

### **Downloading Logs**
1. Click **"Download CSV"** to download fault reports.
2. The CSV file is automatically named with the date & flight number.

### **Server Shutdown**
- Click **"Shutdown Server"** to stop logging operations.

## 📜 API Endpoints
| Method | Endpoint            | Description |
|--------|---------------------|-------------|
| `POST` | `/log`              | Log a new fault record |
| `GET`  | `/current-flight`   | Get the latest flight number |
| `POST` | `/new-flight`       | Create a new flight log |
| `GET`  | `/check-file`       | Check if a flight log exists |
| `POST` | `/shutdown`         | Gracefully shut down the server |
| `GET`  | `/health`           | Check server status |

## 🏗️ Project Structure
```
fault-logger/
│── public/          # Front-end assets (JS, CSS, HTML)
│── logs/            # CSV log storage
│── docs/            # Docsify documentation
│── index.html       # Web interface
│── script.js        # JavaScript logic
│── style.css        # UI styling
│── app.js           # Express server
│── package.json     # Dependencies and scripts
│── README.md        # Project overview
```

## 🖼️ Screenshots
![Fault Logger UI](../assets/logger.png)

## 📜 License
This project is licensed under the MIT License.

## 🔗 Related Links
- 🔗 [GitHub Repository](https://github.com/your-username/logger-app)

