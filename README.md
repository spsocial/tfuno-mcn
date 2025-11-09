# MCN TikTok Landing Page

Landing Page แบบ One-Page สำหรับการสมัคร MCN TikTok พร้อมข้อเสนอสิทธิพิเศษ 4 ข้อ และแนะนำโค้ช 2 ท่าน

## 🎨 Theme

- **สีหลัก**: Black & White (TikTok Style)
- **Accent Colors**: Cyan (#00f2ea) และ Pink (#ff0050)
- **Design**: Modern, Minimalist พร้อม Animations
- **Font**: Sarabun (Google Fonts)

## 📁 โครงสร้างโปรเจค

```
mcn-tiktok-landing/
├── index.html                              (หน้าเว็บหลัก)
├── images/                                 (โฟลเดอร์รูปภาพ)
│   ├── coach-film.jpg                      (รูป Coach FILM - ต้องใส่เอง)
│   └── coach-2.jpg                         (รูป Coach 2 - ต้องใส่เอง)
├── CLAUDE_CODE_INSTRUCTIONS.md             (คำสั่งสำหรับ Claude Code)
└── README.md                               (ไฟล์นี้)
```

## 🚀 วิธีใช้งาน

### วิธีที่ 1: ใช้ไฟล์ HTML โดยตรง

1. ดาวน์โหลดไฟล์ `mcn-tiktok-landing-tiktok-theme.html`
2. สร้างโฟลเดอร์ `images/` ในที่เดียวกับไฟล์ HTML
3. ใส่รูปโค้ช 2 รูป:
   - `images/coach-film.jpg` (รูป Coach FILM)
   - `images/coach-2.jpg` (รูป Coach ท่านที่ 2)
4. เปิดไฟล์ HTML ด้วย Browser เพื่อดูตัวอย่าง

### วิธีที่ 2: ใช้ Claude Code (แนะนำ)

1. เปิด Terminal/Command Prompt
2. สร้างโฟลเดอร์ใหม่:
   ```bash
   mkdir mcn-tiktok-landing
   cd mcn-tiktok-landing
   ```

3. วางไฟล์ `CLAUDE_CODE_INSTRUCTIONS.md` ในโฟลเดอร์

4. เรียก Claude Code:
   ```bash
   claude-code
   ```

5. พิมพ์คำสั่ง:
   ```
   สร้างหน้า Landing Page ตาม specification ในไฟล์ CLAUDE_CODE_INSTRUCTIONS.md
   ```

6. Claude Code จะสร้างไฟล์และโครงสร้างให้อัตโนมัติ

## ✏️ สิ่งที่ต้องปรับแต่งหลังสร้าง

### 1. รูปโค้ช (จำเป็น)

วางรูปใน `images/` folder:
- **ขนาดแนะนำ**: 400x400px หรือ 600x600px (สี่เหลี่ยมจัตุรัส)
- **Format**: JPG หรือ WebP
- **คุณภาพ**: 85-90%

```
images/
├── coach-film.jpg    <- รูป Coach FILM
└── coach-2.jpg       <- รูป Coach ท่านที่ 2
```

### 2. ข้อมูลโค้ชท่านที่ 2 (จำเป็น)

เปิดไฟล์ HTML และแก้บรรทัดที่ 576:
```html
<h3 class="coach-name">Coach [ใส่ชื่อ]</h3>
```
เป็น:
```html
<h3 class="coach-name">Coach [ชื่อจริง]</h3>
```

### 3. Link สมัคร (จำเป็น)

แก้ไขบรรทัดที่ 619:
```html
<a href="#" class="cta-button" onclick="handleCTA(event)">
```
เป็น:
```html
<a href="https://forms.google.com/YOUR_FORM_ID" class="cta-button">
```

หรือแก้ที่ JavaScript function `handleCTA()` บรรทัดที่ 665:
```javascript
window.location.href = 'https://YOUR_SIGNUP_URL';
```

### 4. ข้อมูลติดต่อ (แนะนำ)

แก้ไขบรรทัดที่ 628:
```html
<p>ติดต่อเรา: <a href="#">[ใส่ข้อมูลติดต่อของคุณ]</a></p>
```
เป็น:
```html
<p>ติดต่อเรา: 
    <a href="https://line.me/ti/p/YOUR_LINE_ID">Line: @yourline</a> | 
    <a href="tel:0812345678">Tel: 081-234-5678</a>
</p>
```

## 🎯 Features

### ✨ Animations
- Fade in on scroll
- Smooth scroll behavior
- Parallax effect บน Hero section
- Hover effects บน Cards และ Buttons
- Scroll indicator animation

### 📱 Responsive Design
- **Desktop**: Grid layout แบบเต็ม
- **Tablet**: 2 columns
- **Mobile**: Single column stack

### 🎨 Visual Effects
- TikTok-style gradient backgrounds
- Card hover effects พร้อม shadow
- Button shine effect
- Smooth transitions

## 🌐 การ Deploy

### GitHub Pages (ฟรี)

1. สร้าง Repository ใหม่บน GitHub
2. Upload ไฟล์ทั้งหมด
3. ไปที่ Settings > Pages
4. เลือก branch: main และ folder: / (root)
5. Save และรอสักครู่ จะได้ URL: `https://username.github.io/repo-name`

### Netlify (ฟรี)

1. ไปที่ [netlify.com](https://netlify.com)
2. Drag & Drop โฟลเดอร์ทั้งหมด
3. จะได้ URL ทันที: `https://random-name.netlify.app`
4. (Optional) เปลี่ยน Domain name ได้ฟรี

### Vercel (ฟรี)

1. Install Vercel CLI: `npm i -g vercel`
2. ใน Terminal: `cd mcn-tiktok-landing`
3. รันคำสั่ง: `vercel`
4. ตอบคำถาม และจะได้ URL ทันที

### Firebase Hosting (แนะนำ - เนื่องจากคุณใช้อยู่แล้ว)

1. Install Firebase CLI:
   ```bash
   npm install -g firebase-tools
   ```

2. Login:
   ```bash
   firebase login
   ```

3. Init project:
   ```bash
   firebase init hosting
   ```
   - เลือก "Use an existing project" หรือสร้างใหม่
   - Public directory: `.` (current folder)
   - Single-page app: No
   - Auto builds: No

4. Deploy:
   ```bash
   firebase deploy
   ```

5. จะได้ URL: `https://your-project.web.app`

## 📊 การปรับแต่งเพิ่มเติม

### เปลี่ยนสี Theme

แก้ CSS Variables ในส่วน `:root`:
```css
:root {
    --color-black: #000000;
    --color-cyan: #00f2ea;    /* เปลี่ยนสี Accent */
    --color-pink: #ff0050;    /* เปลี่ยนสี Accent */
}
```

### เพิ่ม Google Analytics

ใส่โค้ดก่อน `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### เพิ่ม Facebook Pixel

ใส่โค้ดก่อน `</head>`:
```html
<!-- Facebook Pixel Code -->
<script>
!function(f,b,e,v,n,t,s)
{if(f.fbq)return;n=f.fbq=function(){n.callMethod?
n.callMethod.apply(n,arguments):n.queue.push(arguments)};
if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
n.queue=[];t=b.createElement(e);t.async=!0;
t.src=v;s=b.getElementsByTagName(e)[0];
s.parentNode.insertBefore(t,s)}(window, document,'script',
'https://connect.facebook.net/en_US/fbevents.js');
fbq('init', 'YOUR_PIXEL_ID');
fbq('track', 'PageView');
</script>
```

## 🛠️ Troubleshooting

### รูปไม่แสดง
- ✅ ตรวจสอบว่ารูปอยู่ใน `images/` folder
- ✅ ตรวจสอบชื่อไฟล์ตรงกับใน HTML หรือไม่ (case-sensitive)
- ✅ ตรวจสอบ path: `./images/coach-film.jpg` (มีจุดด้านหน้า)

### Font ไม่โหลด
- ✅ ตรวจสอบการเชื่อมต่ออินเทอร์เน็ต (Font จาก Google Fonts)
- ✅ ถ้าใช้ offline ให้ดาวน์โหลด font มาใส่ในโปรเจค

### Animation ไม่ทำงาน
- ✅ เปิดใน Browser ที่รองรับ (Chrome, Firefox, Safari, Edge)
- ✅ ตรวจสอบ JavaScript ไม่มี error (เปิด Console: F12)

## 📞 ติดต่อ & สนับสนุน

- **Prompt D Academy**: [ใส่ช่องทางติดต่อ]
- **Line**: [ใส่ Line ID]
- **Facebook**: [ใส่ Facebook Page]

---

**สร้างโดย**: Prompt D Academy  
**เวอร์ชัน**: 1.0  
**อัพเดทล่าสุด**: November 2025  
**License**: สามารถใช้งานและปรับแต่งได้อย่างอิสระ
