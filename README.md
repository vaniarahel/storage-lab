Eksperimen 1: Persistence Test
- Cookies: masih ada 
- LocalStorage: masih ada 
- SessionStorage: hilang

Eksperimen 2: Tab isolation
- nilai counter di tab yang baru saat baru di buka tabnya tetap 0
- nilai counter di tab yang lama tetap 5
kesimpulannya sessionStorage adalah tab-isolated

Eskperimen 3: Storage Size Comparison
- Cookies: ~4KB
- LocalStorage: ~5 - 10MB
- SessionStorage: ~5 - 10MB

Eksperimen 4: Decision Quiz
- skenario 1: User Theme Preference
    jawaban: LocalStorage, karena itu cocok untuk preferensi yang harus presist dan tidak perlu dikirim ke server
- skenario 2: Muti-step Form (Wizard)
    jawaban: SessionStorage, karena itu cocok untuk data form sementara yang harus hilang saat tab ditutup
- skenario 3: Session Authentication Token
    jawaban: Cookies (HttpOnly), karena tiu adalah satu-satunya yang bisa melindungi token dari XSS dan dikirim ke server
- skenario 4: Shopping Cart (tanpa login)
    jawaban: LocalStorage, karena cocok untuk shopping cart yang persist tanpa perlu ke server