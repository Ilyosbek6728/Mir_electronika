# Mir Electronika — Netlify'ga joylash (server bilmasdan)

Bu papka tayyor sayt: do'kon + admin panel + Gemini AI (Robo AI).
Ma'lumotlar (mahsulotlar, narx, karta, promokod, adminlar) Netlify'ning o'z xotirasida saqlanadi,
shuning uchun hamma admin va hamma xaridor bir xil ma'lumotni ko'radi.

## 1. Gemini kalitini oling (bepul)
1. https://aistudio.google.com/apikey ga kiring (Google hisobi bilan).
2. "Create API key" ni bosing va kalitni nusxalab qo'ying. Uni hech kimga bermang.

## 2. GitHub'ga yuklang
1. https://github.com da hisob oching (bepul).
2. Yuqoridagi "+" -> "New repository". Nomi: mir-electronika. "Create repository".
3. "uploading an existing file" havolasini bosing.
4. Zipni ochib, ICHIDAGI hamma narsani (public va netlify papkalari, netlify.toml,
   package.json) oynaga sudrab tashlang. Papkalar o'z holicha qolishi kerak.
5. "Commit changes" ni bosing.

## 3. Netlify'da saytni yarating
1. https://app.netlify.com da "Sign up with GitHub" orqali kiring.
2. "Add new site" -> "Import an existing project" -> GitHub -> mir-electronika.
3. Hech narsani o'zgartirmay "Deploy" ni bosing.

## 4. Maxfiy sozlamalar
Netlify: Site configuration -> Environment variables -> Add variable:

| Nomi | Qiymati |
|------|---------|
| ADMIN_PASSWORD | admin panelga kirish uchun o'zingiz o'ylab topgan parol |
| GEMINI_API_KEY | 1-qadamdagi Gemini kaliti |
| SECRET | uzun tasodifiy matn (masalan 30 ta harf va raqam) |
| GEMINI_MODEL | (ixtiyoriy) model nomi. AI ishlamasa, AI Studio'dagi model nomini yozing |

Keyin: Deploys -> Trigger deploy -> Deploy site (o'zgarishlar kuchga kirishi uchun).

## 5. Kirish
Sayt: https://NOM.netlify.app
Admin: https://NOM.netlify.app/#admin
Birinchi kirish: login `admin`, parol = ADMIN_PASSWORD.
Keyin "Adminlar" bo'limida boshqa adminlarni qo'shing.

## Muhim
- Karta raqami va telefonni "Sozlamalar" bo'limida tekshirib chiqing (boshlang'ich ma'lumotda hozirgi qiymatlar bor).
- Bepul tarif limitlari o'zgarishi mumkin: Netlify va Google'ning joriy shartlarini tekshirib turing.
- Gemini bepul tarifida yozilgan matnlar Google tomonidan ishlatilishi mumkin: AI'ga shaxsiy ma'lumot yozmang.
- AI ishlamasa ham Robo AI katalog bo'yicha oddiy rejimda javob beradi.
