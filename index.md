# Điện Máy Huy Yến Hướng dẫn cài chặn quảng cáo cho TV sansung !

Dưới đây là phần tóm tắt cách làm, và phần chi tiết cách làm. 

### Tóm Tắt cách làm:
* **Tải và cài file giả lập** https://f-droid.org/F-Droid.apk
* **Cài Termux** https://f-droid.org/en/packages/com.termux/
* 
*  Dán vào Termux lần lượt như sau:
* pkg update && pkg upgrade
* ------------------------------------------------
* pkg install nodejs
* -----------------------------------------------
* pkg install git
* --------------------------------------------------
* git clone https://github.com/reisxd/TizenBrewInstaller.git
* ---------------------------------------------------
* cd TizenBrewInstaller/client/ui
* -----------------------------------------------
* npm install --force
* npm run build
* -----------------------------------------------
* cd ../services/tizenbrew-installer-service
* --------------------------------------------------
* npm install
* ------------------------------------------------
* node index.js


* copy phần ( http://localhost:x000 )      và dán vào trình duyệt









### hướng dẫn chi tiết:
### Tổng quan cách làm (để bạn dễ hình dung)

* Điện thoại Android đóng vai trò như máy tính
* Dùng ứng dụng Termux để chạy lệnh
* Cài TizenBrew Installer → từ đó cài TizenTube lên TV Samsung (Tizen OS)
* TV và điện thoại phải chung Wi-Fi
*
*
*
* PHẦN 1: Chuẩn bị trước
* 1️⃣ Trên TV Samsung
* Vào Cài đặt (Settings)
* Chọn Hỗ trợ (Support) → Giới thiệu TV
* Bấm 7 lần vào mục Model hoặc Software Version để bật Developer Mode
* Bật Developer Mode
* Nhập IP của điện thoại Android
* Khởi động lại TV
*
*
* 👉 Bước này để TV cho phép cài app ngoài (rất quan trọng)
*

* 2️⃣ Trên điện thoại Android
* Bạn cần cài:
* 🔹 Termux
* KHÔNG cài Termux trên CH Play
* Tải từ F-Droid (bản chính thức, chạy ổn)
* Sau khi cài, mở Termux lên
* PHẦN 2: Cài công cụ cần thiết trong Termux
*
*
* 3️⃣ Cập nhật Termux
* Gõ từng dòng, nhấn Enter:
* pkg update && pkg upgrade
*
*

* 4️⃣ Cài Node.js
* pkg install nodejs
* 👉 Node.js dùng để chạy TizenBrew Installer

*
* 5️⃣ Cài Git
* pkg install git
* 👉 Git dùng để tải mã nguồn TizenBrew Installer


* PHẦN 3: Tải và build TizenBrew Installer

* 6️⃣ Tải TizenBrew Installer
* git clone https://github.com/reisxd/TizenBrewInstaller.git
* Chờ tải xong.
*
*

*7️⃣ Vào thư mục giao diện (UI)
* cd TizenBrewInstaller/client/ui
*
*
*8️⃣ Cài thư viện và build giao diện
* npm install --force
* npm run build
*⏳ Bước này hơi lâu (2–5 phút), đợi chạy xong không báo lỗi
*
*

*9️⃣ Vào thư mục service
* cd ../services/tizenbrew-installer-service
*
*

*🔟 Cài thư viện cho service
* npm install
*
*

* PHẦN 4: Chạy TizenBrew Installer
*1️⃣1️⃣ Chạy service
* npm start
* Nếu thành công, bạn sẽ thấy thông báo server đang chạy (ví dụ cổng 3000).
*

*1️⃣2️⃣ Mở trình duyệt trên điện thoại
* Truy cập:
* http://localhost:3000
* 👉 Giao diện TizenBrew Installer sẽ hiện ra
*
*

*PHẦN 5: Cài TizenTube lên TV
*1️⃣3️⃣ Kết nối với TV
* Trong giao diện TizenBrew:
* Nhập IP của TV Samsung
* Kết nối (TV & điện thoại cùng Wi-Fi)
*1️⃣4️⃣ Cài TizenTube
* Chọn TizenTube
* Nhấn Install
* Chờ hoàn tất
* 👉 Sau khi xong, TizenTube sẽ xuất hiện trên TV như app bình thường
*
*

* LƯU Ý QUAN TRỌNG

* ❗ Mỗi lần tắt nguồn TV hoàn toàn, app cài ngoài có thể bị mất → cần cài lại
* ✔️ Nên để TV ở chế độ Standby, không rút điện
* 📺 Một số TV Samsung đời cũ có thể không hỗ trợ đầy đủ
