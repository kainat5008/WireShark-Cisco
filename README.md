
# Network Traffic Analysis using Wireshark

**Name:** Kainat Khalid  
**Section:** CS-A  
**Roll Number:** i22-2242  

---

## 📘 Overview

This lab focused on analyzing and understanding computer network behavior through practical exercises using **Wireshark**—a powerful network protocol analyzer. The primary objectives included:

- Observing HTTP packet-level data exchange
- Analyzing IP addresses and port information
- Customizing Wireshark filters for better packet visualization
- Identifying communication between a host machine and a remote server

---

## 🔍 Lab Breakdown

### ✅ Task 1 – Server File Handling

- **Objective**: Work with a file located on a server.
- **Environment**: Local host machine connected to a networked server.
- **Verification**: Confirmed visibility and accessibility of the file.

### ✅ Task 2 – Wireshark Traffic Analysis

#### 🔸 Wireshark Setup:
- Installed and launched Wireshark to monitor real-time traffic.
- Applied **custom filters** to isolate HTTP traffic.
- Modified **foreground and background colors** for better visibility and differentiation of filtered packets.

#### 🔸 Observations:

| Detail                 | Value               |
|------------------------|---------------------|
| **Source IP**          | `172.16.136.103`    |
| **Destination IP**     | `216.58.209.131`    |
| **Source Port**        | `80`                |
| **Destination Port**   | `80`                |
| **Protocol**           | `HTTP`              |

This indicates an HTTP request initiated by the host machine to a remote server (likely a web server such as Google or similar).

#### 🔸 Key Takeaways:
- HTTP communication occurs over port 80 (default).
- The source IP `172.16.x.x` suggests a **private IP range**, indicating NAT translation is likely being used for external communication.
- Destination IP `216.58.209.131` maps to a **public-facing server**, showcasing a typical client-server request in action.
- **Wireshark** filters such as `http` and IP-based filters like `ip.addr==216.58.209.131` are critical for narrowing down useful data.
- Color customization in Wireshark enhances packet tracking efficiency, especially in high-traffic logs.

---

## 🧠 Skills Practiced

- Packet inspection using Wireshark
- Network addressing (public vs private IP)
- Identifying port roles in client-server communication
- HTTP traffic analysis
- Filter and display configuration in Wireshark

---

## 🔧 Tools Used

- 🧪 **Wireshark** (Network packet analyzer)
- 🖥️ Local PC with IP `172.16.136.103`
- 🌐 Remote HTTP server at `216.58.209.131`
