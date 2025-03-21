# Honeypot Project

## Overview
The **Honeypot-Project** is a cybersecurity initiative designed to detect unauthorized access attempts and analyze malicious activities. It integrates **Heralding, Graylog, OpenSearch, Filebeat (Logstash), and Python scripts** to create an automated system for monitoring and alerting.

## Features
- **Heralding**: Captures login attempts and records authentication data.
- **Graylog**: Centralized log management and visualization.
- **OpenSearch**: Stores and indexes log data for analysis.
- **Filebeat (Logstash)**: Collects, processes, and forwards log data.
- **Python Email Alert System**: Sends real-time email notifications for detected threats.

## Installation & Setup
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/lakhan2083/Honeypot-Project.git
cd Honeypot-Project
```

### 2️⃣ Set Up Heralding (Virtual Environment)
```bash
cd heralding
python3 -m venv my_venv
source my_venv/bin/activate
pip install -r requirements.txt
```

### 3️⃣ Configure Graylog & OpenSearch
- Ensure Graylog and OpenSearch are properly configured.
- Use Graylog for log analysis.
- Configure OpenSearch for data indexing.

### 4️⃣ Start Filebeat
```bash
sudo systemctl start filebeat
```

### 5️⃣ Run the Python Alert Script
```bash
python3 alert_script.py
```

## Usage
- Logs can be accessed in **Graylog**.
- Login attempts are stored in `/home/kali/heralding/log_auth.csv`.
- Session logs are stored in `/home/kali/heralding/log_session.csv`.
- OpenSearch indexes log data for further analysis.

## Contributing
1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b new-feature`)
3. **Commit changes** (`git commit -m "Added new feature"`)
4. **Push to GitHub** (`git push origin new-feature`)
5. **Create a Pull Request**

## License
This project is **open-source** under the MIT License.

## Contact
For queries, reach out via [GitHub Issues](https://github.com/lakhan2083/Honeypot-Project/issues).
