# Storyteller — Interview Companion
 
A single-file, client-side job search command center: track applications, analyze job descriptions against your resume, build a bank of interview stories, and generate cover letters — all in one HTML page with no backend required.
 
> 求職全流程管理工具：追蹤職位申請、比對履歷與職缺、建立面試故事庫、產生求職信 — 單一 HTML 檔案，無需後端伺服器。
 
---
 
## Table of Contents / 目錄
 
- [English](#english)
- [中文](#中文)
---
 
## English
 
### Overview
 
Storyteller is a self-contained interview preparation and job search tracker. Open the HTML file in any browser and it works immediately — every user's data is kept in their own browser's local storage, scoped to the email they sign in with. There is no server, no database, and no account system beyond typing an email address to open a private workspace.
 
### Features
 
**Multi-user private workspaces**
Sign in with any email address. Each email gets its own isolated workspace stored in the browser (no password, no server — this is meant for personal/local use, not shared authentication).
 
**Dashboard**
- Summary stats: total applications, average resume fit score, stories marked "Ready," resume upload status.
- A "Getting Started" guide with five simple steps matching the recommended workflow: upload resume → track applications → build your interview question bank → analyze job descriptions → prepare your cover letter.
- Job pipeline overview: counts of applications at each stage (Applied, Phone, On-site, Offer, Rejected).
- Recent applications timeline with fit score and current stage.
**Resume**
- Upload a resume as `.txt`, `.pdf`, or Word `.docx` (parsed in-browser using PDF.js and Mammoth.js — nothing is uploaded to a server), or paste resume text directly.
- A toast notification confirms successful upload (or shows an error if parsing fails).
- Uploading or saving a new resume automatically recalculates the fit score for every tracked job.
- Shows the last-updated timestamp.
**Job Tracker**
- Add a position with company, title, applied date, job posting URL, full job description, and a "dream company" flag.
- Automatic fit score: a keyword-matching engine compares your resume against each job description across categories like data analytics, operations, project management, communication, tools, and business skills.
- Stage tracking with one-click buttons: Applied, Phone, On-site, Offer, Rejected — all shown in a single row per job card.
- Rejection tracking: when a job is marked Rejected, a date is recorded automatically, and you can add rejection notes/reason (e.g., "went with an internal candidate") via the edit form.
- Click any job card to open a detail view: fit score, matched skills, missing skills to develop, full list of JD-derived keywords, AI-suggested likely interview questions, the rejection record (if applicable), and the full job description.
- Edit any position in place from the detail view — nothing is duplicated, the same entry is updated.
- Download a generated cover letter (from your saved template) directly from each job card.
- Summary stats: total applications, dream companies, average fit score, in-progress count, rejected count — laid out in a single row.
**Interview Question Bank** (formerly "Stories")
- Build a library of behavioral interview stories using the STAR format (Situation, Action, Result).
- Categorize each story (Behavioral, Data-Driven, Process Improvement) and track your confidence level (Drafting, Developing, Ready).
- A practice counter lets you log how many times you've rehearsed each story.
**JD Analysis**
- Paste any job description (without adding it to your tracker) to instantly see your resume fit score, matched and missing skills, the full list of extracted JD keywords, and likely interview questions — useful for a quick check before deciding whether to apply.
**Cover Letter**
- Save one reusable template using `[COMPANY]` and `[POSITION]` placeholders.
- Select any tracked job to generate a preview, copy it to the clipboard, or download it as a `.txt` file.
**Bilingual interface (English / 中文)**
- Full UI translation — every label, button, section heading, form field, and even the AI-generated interview questions are available in both English and Traditional Chinese.
- The app always starts in English; switch languages anytime with the toggle in the top bar, and the active language stays in sync with what's on screen.
**Other niceties**
- Dark mode toggle.
- Fully responsive layout with a mobile hamburger menu for the sidebar navigation.
- Every modal (add/edit job, job details, add story) can be closed by clicking outside of it, not just with a Close button.
### Getting Started
 
1. Download `storyteller.html` and open it in any modern browser (Chrome, Edge, Firefox, Safari).
2. Sign in with any email address to create your private workspace.
3. Follow the suggested flow: upload your resume, start tracking applications, build your interview story bank, analyze job descriptions as needed, and set up your cover letter template.
### Tech Stack
 
- Plain HTML, CSS, and vanilla JavaScript — no build step, no framework.
- [Tailwind CSS](https://tailwindcss.com/) (CDN) for base styling utilities.
- [PDF.js](https://mozilla.github.io/pdf.js/) for in-browser PDF text extraction.
- [Mammoth.js](https://github.com/mwilliamson/mammoth.js) for in-browser `.docx` text extraction.
- Browser `localStorage` for all data persistence — nothing leaves your machine.
### Privacy
 
All data (resume text, job applications, stories, cover letter template) is stored only in your browser's local storage, keyed to the email you sign in with. Nothing is transmitted to any server. Clearing your browser data or switching browsers/devices will not carry your data over.
 
### License
 
Add your preferred license here (e.g., MIT).
 
---
 
## 中文
 
### 簡介
 
Storyteller 是一個一體成型、完全在瀏覽器端運作的求職準備與職位追蹤工具。只要用任何瀏覽器打開這個 HTML 檔案就能直接使用，每位使用者的資料都會依照登入時輸入的電子郵件，儲存在該瀏覽器自己的本機儲存空間中。沒有伺服器、沒有資料庫，也沒有真正的帳號系統 —— 輸入電子郵件只是為了建立一個屬於你自己的私密工作區。
 
### 功能介紹
 
**多使用者私密工作區**
用任何電子郵件登入即可。每個電子郵件都會擁有自己獨立、儲存在瀏覽器裡的工作區（沒有密碼、沒有伺服器 —— 這是設計給個人本機使用，而非多人共用登入系統）。
 
**儀表板**
- 總覽統計：總申請數、平均履歷匹配度、已標記為「已準備好」的故事數量、履歷上傳狀態。
- 「新手指南」步驟卡片，依照建議流程列出五個步驟：上傳履歷 → 追蹤職位申請 → 建立面試題庫 → 分析職位描述 → 準備求職信。
- 職位進度總覽：各階段（已申請、電話面試、現場面試、已獲聘、已拒絕）的申請數量。
- 最近申請時間軸，顯示匹配分數與目前進度階段。
**履歷**
- 可上傳 `.txt`、`.pdf` 或 Word `.docx` 格式的履歷（全部在瀏覽器內用 PDF.js 與 Mammoth.js 解析，不會上傳到任何伺服器），或直接貼上履歷文字。
- 上傳成功會跳出提示通知（若解析失敗則顯示錯誤提示）。
- 上傳或儲存新履歷後，會自動重新計算所有已追蹤職位的匹配分數。
- 顯示履歷最後更新時間。
**職位追蹤**
- 新增職位時可填寫公司、職稱、申請日期、職缺連結、完整職位描述，並可標記為「理想公司」。
- 自動匹配分數：透過關鍵字比對引擎，將你的履歷與各職位描述在數據分析、營運、專案管理、溝通協作、工具、商業分析等類別上進行比對。
- 一鍵切換進度階段：已申請、電話面試、現場面試、已獲聘、已拒絕 —— 全部整齊排列在每張職位卡片的同一排。
- 拒絕紀錄追蹤：當職位被標記為「已拒絕」時，系統會自動記錄日期，你也可以在編輯視窗中補充拒絕原因或備註（例如「公司選擇了內部候選人」）。
- 點擊任一職位卡片可開啟詳情視窗：匹配分數、你已具備的技能、需要加強的技能、完整的職缺關鍵字列表、AI 推薦的可能面試問題、拒絕紀錄（若有），以及完整職位描述。
- 可直接在詳情視窗中點擊編輯，修改後會更新同一筆資料，不會產生重複紀錄。
- 可直接從職位卡片下載（依你儲存的範本）產生的求職信。
- 總覽統計：總申請數、理想公司數、平均匹配分數、進行中數量、已拒絕數量 —— 全部排列在同一排。
**面試題庫**（原「故事庫」）
- 以 STAR 架構（情境、行動、結果）建立行為面試故事庫。
- 為每個故事分類（行為問題、數據導向、流程改善），並標記熟練程度（草稿中、準備中、已準備好）。
- 練習次數計數器，記錄你演練過每個故事幾次。
**JD 分析**
- 貼上任何職位描述（不會加入職位追蹤清單），即可立即看到履歷匹配分數、已具備與缺少的技能、完整的職缺關鍵字列表，以及可能的面試問題 —— 適合在決定是否申請前快速檢查。
**求職信**
- 儲存一份可重複使用的範本，使用 `[COMPANY]` 與 `[POSITION]` 作為佔位符。
- 選擇任一已追蹤的職位即可產生預覽、複製到剪貼簿，或下載為 `.txt` 檔案。
**中英雙語介面**
- 完整介面翻譯 —— 所有標籤、按鈕、區塊標題、表單欄位，甚至連 AI 產生的面試問題都有中英文版本。
- 每次開啟都預設為英文，可隨時透過畫面上方的語言切換按鈕切換，切換後的語言狀態會與畫面內容保持同步。
**其他細節**
- 深色模式切換。
- 完全響應式版面設計，手機上會出現漢堡選單以開關側邊導覽列。
- 每個彈出視窗（新增／編輯職位、職位詳情、新增故事）都可以直接點擊視窗外的區域關閉，不一定要按下方的關閉按鈕。
### 使用方式
 
1. 下載 `storyteller.html`，並用任何現代瀏覽器（Chrome、Edge、Firefox、Safari）打開它。
2. 用任何電子郵件登入，即可建立屬於你的私密工作區。
3. 依照建議流程操作：上傳履歷、開始追蹤職位申請、建立面試題庫、視需要分析職位描述，並設定你的求職信範本。
### 技術架構
 
- 純 HTML、CSS 與原生 JavaScript —— 無需建置流程，也不依賴任何前端框架。
- [Tailwind CSS](https://tailwindcss.com/)（CDN 版本）提供基礎樣式工具。
- [PDF.js](https://mozilla.github.io/pdf.js/) 用於瀏覽器端解析 PDF 文字。
- [Mammoth.js](https://github.com/mwilliamson/mammoth.js) 用於瀏覽器端解析 `.docx` 文字。
- 所有資料皆儲存於瀏覽器的 `localStorage` —— 不會傳送到任何伺服器。
### 隱私說明
 
所有資料（履歷文字、職位申請紀錄、故事、求職信範本）僅儲存在你瀏覽器的本機儲存空間中，並依登入時使用的電子郵件做區隔。資料不會傳送到任何伺服器。清除瀏覽器資料，或更換瀏覽器／裝置，都不會保留原本的資料。
