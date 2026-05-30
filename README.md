# 🎮 Game Info Finder: Asynchronous RAWG API Integration Engine

HTML5, CSS3 va Vanilla JavaScript (ES6+ Asynchronous Architecture) yordamida yaratilgan, dunyodagi eng yirik RAWG video o'yinlar ma'lumotlar bazasi bilan real vaqt rejimida aloqa o'rnatuvchi dynamic qidiruv platformasi. Loyiha tashqi API-lar bilan ishlash, HTTP so'rovlarini boshqarish va asinxron ma'lumotlar oqimini DOM-ga dinamik integratsiya qilish usullarini namoyish etadi.

---

## 📝 Loyiha haqida

Ushbu veb-ilova foydalanuvchi kiritgan o'yin nomi asosida global serverga so'rov yuboradi. Qaytgan ma'lumotlar ichidan o'yinning aniq nomi, rasmiy chiqarilgan sanasi, geymerlar hamjamiyatidagi reyting ko'rsatkichi, tegishli janrlari hamda o'yinga tegishli yuqori sifatli fon rasmini (background image) topib, foydalanuvchi ekranida chiroyli vizual kartochka (`.game-card`) ko'rinishida guruhlaydi.

---

## 📐 Asinxron Ma'lumotlar Arxitekturasi (Fetch API Workflow)

Tizim API so'rovlarini xavfsiz va xatolarsiz qayta ishlash uchun `try...catch` himoya bloki va asinxron `Promises` zanjiriga tayanadi:

1. **Kiritish nazorati:** Input bo'sh bo'lsa, brauzer so'rov yubormasdan `alert()` chiqaradi va resurslarni tejaydi.
2. **Asinxron HTTP So'rov (`Fetch API`):**
   ```javascript
   const response = await fetch(`https://api.rawg.io/api/games?key=${apiKey}&search=${gameName}`);
