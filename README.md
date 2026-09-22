# LanShare v5.4.1

LanShare is a lightweight Windows desktop application for LAN file sharing, serving as an alternative to traditional SMB folder sharing. It comes with built-in WebDAV network drive, group permission management, file audit logs and web-based file preview, and supports direct browsing of WebDAV directories via web browsers. Packaged as a single EXE file, it works offline within the internal network only, ideal for workshop drawings and enterprise team document distribution.

## ✨ Feature List
- Web interface (Port 8080): File browsing, upload, download, deletion, and online preview for images/PDF/TXT files
- WebDAV Service (Port 8081)
  - Map network drives on Windows; directly double-click to edit Word/Excel files and save changes back to the server with Ctrl+S
  - Web browsers can directly access the WebDAV directory page
- Isolated user & group permissions: Different groups can only access assigned directories to achieve departmental file isolation
- Audit logs: Records all file operations and supports log export
- Graphical account management interface; account credentials stored locally
- Single EXE package, ready to run out of the box, no Python environment required

## 📡 Port Description
|Port|Function|
| ---- | ---- |
|8080|Web file management panel|
|8081|WebDAV network drive service with browser directory browsing support|

## 🚀 Quick Start
1. Launch LanShare and set the root shared directory
2. Allow `8080` and `8081` through the Windows Firewall
3. Create groups, add new users and bind corresponding group permissions
4. Start the service
   - Web access: `http://local-IP:8080`
   - WebDAV mapping: `http://local-IP:8081`

## ⚠️ WebDAV Client Notes
Before mapping WebDAV on Windows PCs:
1. Enable the `WebClient` service
2. Set registry value `BasicAuthLevel = 2` to enable basic authentication

## 📌 Version Notes v5.4.1
Updates based on the full v5.4 release:
- Enabled the WsgiDavDirBrowser middleware. Accessing port 8081 via web browser no longer returns 403; WebDAV directories can be browsed directly
- WebDAV file read/write, group permission and web interface features remain unchanged from v5.4

## 📄 License
MIT License
