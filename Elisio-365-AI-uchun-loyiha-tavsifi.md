# Elisio 365 — mahsulot tavsifi va mustaqil tanqid uchun topshiriq

Quyidagi ta’rifni Elisio 365 haqida mustaqil tahlil beradigan AI’ga yuboring. Undan maqtov emas, asosli va amaliy tanqid so‘rang.

## Loyiha nima?

Elisio 365 — inson o‘z hayotini, kundalik fikrlarini, o‘rganganlarini, ishlarini va yutuqlarini saqlaydigan shaxsiy maydon. Har bir inson o‘zi uchun yopiq kundalik yurita oladi; xohlasa ayrim yozuvlari yoki portfolio qismlarini do‘stlari, oilasi yoki barcha bilan ulashadi. Boshqa odamlar ochiq ruxsat berilgan profil va yozuvlarni ko‘rishi, yoqtirishi va izoh qoldirishi mumkin.

Bu mahsulot ijtimoiy tarmoq tasmasini ko‘chirmasligi kerak. Asosiy markaz — alohida insonning shaxsiy portfolio va hayot arxivi: bugun nima qildi, nimalarni o‘rgandi, qanday fikrlari va loyihalari bor, qanday sertifikat hamda yutuqlarga erishdi. Foydalanuvchi vaqt o‘tishi bilan o‘z hikoyasini o‘zi quradi. Profil oddiy ish tarjimayi holi bilan chegaralanmaydi: dasturlash, Phantom Testlab, sayyor ovqat savdosi, kiberxavfsizlik, kitobxonlik, ilmiy g‘oyalar va shaxsiy o‘sish bir insonning turli tomonlari sifatida joylashishi mumkin.

Mahsulotning dastlabki foydalanuvchisi — kundalikni yuritmoqchi, o‘z ustida ishlamoqchi va qilgan ishlarini keyin ko‘rish yoki yaqinlariga ko‘rsatishni istaydigan inson. U telefon va Windows noutbukdan foydalanishi, ma’lumotlari esa hisobiga bog‘liq holda qurilmalar orasida saqlanishi kerak.

## Foydalanuvchi tajribasi

1. Foydalanuvchi telefon raqami yoki Google hisobidan biri bilan kiradi. Tizim foydalanuvchini tasdiqlagandan so‘ng undan ism, familiya, taxallus, noyob foydalanuvchi nomi va davlatini so‘raydi.
2. Foydalanuvchi 100 dan ortiq ma’noli portfolio ko‘rinishlaridan birini tanlaydi. Profil keyinchalik o‘zgartirilishi mumkin.
3. Har kuni matn, rasm, video yoki hujjat yuklab, “Kundalik”, “Loyiha”, “Sertifikat/yutuq”, “Ilmiy g‘oya” va “Kitobxonlik” kabi bo‘limlarda yozuv yaratadi va keyinchalik tahrirlaydi.
4. Har bir yozuv uchun kim ko‘rishini tanlaydi: faqat o‘zi, o‘zi tanlagan do‘stlar, o‘zi tanlagan oila a’zolari yoki barcha. Yangi kundalik yozuvi dastlab faqat o‘ziga ko‘rinadi. Profilni va ichidagi ayrim qismlarni turli darajada ulashish mumkin.
5. Odamlar foydalanuvchini `@username` orqali qidiradi, uning ochiq sahifasini ko‘radi, ochiq yozuvlarni yoqtiradi va izoh qoldiradi. Yozuv egasi o‘z izohlarini, foydalanuvchi esa o‘zi qoldirgan izohlarni boshqarishi kerak.

## Mahsulot qadri va yo‘nalish

- Reklama bo‘lmaydi.
- Qora fon, oq matn va turli davlat bayroqlari brendning ko‘rinishiga kiradi.
- Ko‘rinish shaxsiy, sokin, puxta va esda qoladigan bo‘lsin. Instagram yoki Telegram’ning post tasmasi va bezaklarini taqlid qilmasin.
- Do‘stlar, oila va omma uchun alohida ulashish foydalanuvchi nazoratida bo‘lsin. Yozuv, foto va video tasodifan ochilib qolmasin.
- Ma’lumotlarni uzoq muddat saqlash, hisobni turli qurilmada tiklash va egasiga eksport/delete imkonini berish mahsulotning asosiy talabi.
- Dastlab bepul va reklamasiz tajriba ko‘zda tutilgan. Kelajakdagi daromad modeli hali qaror qilinmagan; foydalanuvchini yashirin reklama yoki kutilmagan pullik devorga olib bormaslik kerak.

## Hozirgi prototipda bajarilgani

Quyidagilar mavjud prototipdagi implementatsiyani ifodalaydi; ularni yakuniy yoki ommавий reliz deb tushunmang.

- O‘zbekcha, moslashuvchan qora interfeys, portfolio bo‘limlari va davlat bayroqlari.
- D1’da profil va yozuvlarni saqlash; noyob username, ism, familiya, taxallus, davlat va bio.
- “O‘zim”, “Do‘stlar”, “Oila”, “Hamma” auditoriyalari. Do‘st/oila hozircha profil egasi boshqaradigan alohida ruxsat ro‘yxati; bu ikki tomonlama do‘stlik yoki taklifni qabul qilish oqimi emas.
- Kundalik, loyiha, sertifikat, ilmiy g‘oya va kitob yozuvlarini yaratish, tahrirlash, o‘chirish.
- R2’da JPEG, PNG, WebP, GIF, MP4, WebM va PDF saqlash. Hozirgi sinov limitlari: 32 MB/fayl, yozuvga oltitagacha fayl, foydalanuvchiga jami 500 MB.
- `@username` bilan qidiruv, ochiq profil, layk, izoh, izohni muallif yoki yozuv egasi o‘chirishi.
- 10 ta profil maketi va 12 ta rang aksenti kombinatsiyasidan iborat 120 tanlov. Bu 120 xil mustaqil, chuqur ishlangan dizayn degani emas.
- Mos brauzerda Android/Windows bosh ekraniga qo‘shish uchun web manifest/service worker. Hozir bu Play Market Android ilovasi yoki Windows MSIX paketi emas.
- Matn va metama’lumotlarni JSON ko‘rinishida chiqarish; eksport videolar va boshqa binary fayllarni o‘z ichiga olmaydi.
- Mahalliy prototipda ruxsat nazorati, yozuvga kirish, media URL’lari, layk, izoh, guruhdan chiqarish va CSRF manba tekshiruvi uchun integratsiya sinovlari o‘tgan.

## Hali bajarilmagan va qaror talab qiladigan qismlar

- Telefon/SMS yoki Google orqali hisob ochish ulanmagan. Prototipda faqat joylashtirish muhitining ChatGPT kirishi mavjud; bu kelajakdagi foydalanuvchilar uchun so‘ralgan login emas.
- Prototipni haqiqiy, umumiy foydalanuvchilarga ochishdan oldin autentifikatsiya provayderi va ruxsat siyosatini tanlash kerak.
- Android Google Play uchun AAB/APK, Windows uchun distributiv, signing, developer account yoki store submission tayyorlanmagan.
- Prototip joylashtirishda hozir faqat egasiga yopiq. `Hamma` yozuv degani sayt allaqachon ommaviy degani emas.
- Hisobni to‘liq o‘chirish, bloklash/shikoyat qilish, moderatsiya paneli, kontentni saqlash/o‘chirish siyosati, yuklangan fayllarni tekshirish va kuchliroq rate limiting ishlab chiqilmagan.
- Oila a’zolariga ruxsat qo‘shish/olib tashlash oqimi hozir username asosida va bir tomonlama. Bola yoki nozik ma’lumotlar uchun maxsus nazorat belgilari yo‘q.
- Video siqish/transkodlash, resumable upload, push xabarnoma, ingliz/rus kabi tillar va to‘liq offline yozuvlar yo‘q.
- Hajm bo‘yicha limitni bir vaqtdagi yuklashlar orasida qat’iy atomik saqlash, zaxira/restore, production load, real Android/Windows va accessibility testlari hali bajarilmagan.

## AI’dan so‘raladigan mustaqil tahlil

Sen ushbu mahsulot uchun mustaqil mahsulot tanqidchisi va tajribali UX, xavfsizlik hamda arxitektura maslahatchisisan. Maqsading Elisio 365’ni shunchaki zamonaviy ko‘rsatish emas; undan odam muntazam foydalanadigan, shaxsiy ma’lumotini ishonch bilan topshira oladigan, keyinchalik real do‘kon talablarigacha yetadigan mahsulot qilish.

Ta’rifni diqqat bilan tahlil qil va asosli fikringni bildir. G‘oyani maqtashga urinma. Noaniq, takrorlanuvchi, ziddiyatli, keragidan ortiq yoki xavfli joylarni ochiq ko‘rsat. “Yaxshi bo‘lardi” degan umumiy maslahat o‘rniga, nima uchun muammo ekanini va qanday konkret yechimni tanlaganingni tushuntir.

Javobing quyidagi tartibda bo‘lsin:

1. **Bir jumlalik hukm:** eng kuchli farqlovchi qiymat va hozirgi eng katta xavfni ayt.
2. **Aniq tanqid:** mahsulot g‘oyasi, birinchi foydalanish, kundalik odati, portfolio tuzilmasi, oila/do‘stlar ruxsati, maxfiylik, qidiruv, izohlar, media, kirish, qurilmalar, dizayn tanlovi va ilovalar do‘koni rejasida kamchiliklarni top. Har biri uchun og‘irligini `to‘siq`, `muhim` yoki `keyin` deb belgilab, sababini yoz.
3. **Xavfsizlik va ishonch auditi:** noto‘g‘ri sozlama orqali kundalik yoki media oshkor bo‘lishi, hisobni yo‘qotish, boshqalarning shaxsiy ma’lumotini joylash, nomaqbul izoh, akkauntni egallash, yosh bolalar/qarindoshlar ma’lumoti, backup va o‘chirish bo‘yicha tahdidlarni ko‘rib chiq. Qaysi tahdidni hozir hal qilish lozimligini ko‘rsat.
4. **Yaxshiroq mahsulot qarori:** qiymatni saqlagan holda qaysi oqim yoki funksiyani o‘zgartirishni taklif qilishingni va bu foydalanuvchiga qanday yengillik berishini misol bilan tushuntir. Shu jumladan do‘st va oila ro‘yxati o‘zaro tasdiqlanishi kerakmi, yoki egasining tanlovi yetarlimi — qaroringni asosla.
5. **Birinchi reliz:** ishga tushirish uchun zarur bo‘lgan eng kichik, lekin ishonchli imkoniyatlar to‘plamini belgila. Hozir olib tashlash mumkin bo‘lgan xususiyatlarni ko‘rsat. 120 dizayn va murakkab media xususiyatlariga nisbatan ustuvorlikni bahola.
6. **Bosqichma-bosqich reja:** eng muhim 5–10 ishni tartibla. Har biri uchun natija, qaramlik va tekshirish mezonini yoz. “Avval autentifikatsiya → so‘ng ma’lumot/ruxsat → so‘нг tajriba/dizayn → so‘ng beta/store” kabi даражani маҳсулотга мосла.
7. **Aniq savollar:** javob o‘zgarmasa arxitektura yoki UX noto‘g‘ri chiqadigan eng ko‘pi bilan 7 savolni ber. Javob bo‘lmasa qaysi xavfsiz taxminni ishlatishni ham yoz.

Hozirgi kodda tasdiqlanmagan imkoniyatlarni mavjud deb ko‘rsatma. Foydalanuvchiga hali ulanmagan login, ommaviy hosting yoki store publishing bor deb va’da berma. Har bir tavsiyani **zarur**, **foydali**, yoki **keyinroq** deb farqla. Faqat odatiy ijtimoiy tarmoq funksiyalarini qo‘shish uchun taklif berma; Elisio 365’ning kundalik + hayot portfolioga asoslangan farqini himoya qil. Javob aniq, tanqidiy va amalda bajariladigan bo‘lsin.
