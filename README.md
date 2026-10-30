# स्वामी गोपाल तीर्थ बहुउद्देशीय संस्था - Two-Column Cash Book

**संस्था नाव:** स्वामी गोपाल तीर्थ बहुउद्देशीय संस्था, श्रीराम नगर भद्रावती  
**नोंदणी क्रमांक:** F-0016068(CDP)  
**प्रकल्प स्थान:** `C:\Users\student\.gemini\antigravity\scratch\sgtb-cashbook`

---

## 📁 प्रकल्पातील मुख्य फाईल्स (Project Structure)
```
sgtb-cashbook/
├── index.html                     # मुख्य वेब ॲप्लिकेशन (100% कार्यक्षम सिंगल-फाईल ॲप)
├── banner.jpg                     # फ्रंट पेजवरील तिन्ही गुरूंचा भव्य बॅनर फोटो
├── logo.jpg                       # संस्थेचा अधिकृत गोलाकार लोगो
├── README.md                      # प्रकल्प माहिती व तांत्रिक दस्तऐवजीकरण
└── backups/                       # फायरबेस डाटाबेसच्या सुरक्षित JSON बॅकअप फाईल्स
    └── CashBook_Backup_Latest.json
```

---

## 🚀 महत्त्वाचे फीचर्स (Key Features)

### १. दोन रकाने कॅश बुक (Two-Column Cash Book Engine):
- **रोख रकाना (Cash Column):** In (जमा) | Out (खर्च)
- **बँक रकाना (Bank Column):** In (जमा) | Out (खर्च)
- **एकूण शिल्लक (Running Balances):** रोख शिल्लक + बँक शिल्लक = संस्थेचा एकूण निधी

### २. पेमेंट मोड्स व कॉन्ट्रा व्यवहार (Payment Modes & Contra):
- **Bank:** Online / UPI / NEFT / RTGS / Cheque
- **Cash:** प्रत्यक्ष रोख व्यवहार
- **Contra (Cash to Bank):** रोख रक्कम बँकेत भरली (Cash Out ➡️ Bank In)
- **Contra (Bank to Cash):** खर्चासाठी बँकेतून रोख काढली (Bank Out ➡️ Cash In)
- **Contra (Bank to FD):** बँकेतून मुदत ठेव (FD) केली (Bank Out)
- **Contra (FD to Bank):** FD मोडून बँकेत जमा केली (Bank In)

### ३. पावती व व्हाउचर नंबरिंग सिस्टीम (Smart Voucher Auto-Sequence):
- **पावती (Receipt - PN):** देणगी पावती (उदा. `PN 01`, `PN 219`)
- **A/VSN:** आजीवन / वार्षिक सभासद नोंदणी (उदा. `A/VSN 01`, `A/VSN 10`)
- **व्हाउचर (Voucher - VN):** सामान्य खर्च व्हाउचर (उदा. `VN 01`, `VN 15`)
- **Internal Banking Transaction:** बँक हस्तांतरण (उदा. `VN 15 - IBT 11`)
- **other (इतर):** मॅन्युअल Cheque / UTR / Transaction No.

### ४. WhatsApp ऑटोमेशन (Instant Receipt Share):
- तक्त्यातील प्रत्येक पावतीसमोर हिरवा WhatsApp आयकॉन (`🟢💬`).
- दात्याचा फोन नंबर टाकून संस्थेच्या अधिकृत फॉरमॅटमध्ये पावती थेट WhatsApp वर पाठवता येते.

### ५. सुरक्षितता व भूमिका (Roles & Security):
- **Admin:** संपूर्ण ॲक्सेस (नोंद करणे, बदलणे, हटवणे, मासिक PDF, बॅकअप, विश्वस्त व्यवस्थापन).
- **Viewer (विश्वस्त):** केवळ पाहण्याचा ॲक्सेस (नोंदी पाहणे, शोधणे, WhatsApp पावती देणे). बदल किंवा डिलीट करू शकत नाही.

---

## 🔧 तांत्रिक कॉन्फिगरेशन (Technical Config)

### Firebase Credentials:
- **Project ID:** `swami-gopal-tirth`
- **Auth Domain:** `swami-gopal-tirth.firebaseapp.com`
- **Database:** Cloud Firestore (`transactions`, `viewers` collections)

### Google Drive Integration:
- **Google Apps Script Web App URL:**  
  `https://script.google.com/macros/s/AKfycbw8bYYwVOJ1ul5UF01oeEdhGfexUhqkb2ByBARoLRvRdAAJBiM7phRkZCeLWnmSxwKMtA/exec`
- **Bank Statement PDF Password:** `swam1905`

---

## 💻 वापर कसा करावा?
1. [`index.html`](file:///C:/Users/student/.gemini/antigravity/scratch/sgtb-cashbook/index.html) फाईलवर डबल-क्लिक करून उघडा.
2. डेस्कटॉपवरही [`sgtbsb.html`](file:///C:/Users/student/Desktop/sgtbsb.html) नावाने थेट शॉर्टकट उपलब्ध आहे.
