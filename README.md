# Overview : A/B Testing Analysis for Digital Marketing

# Latar Belakang
Proyek ini merupakan analisis A/B Testing untuk mengevaluasi efektivitas iklan digital terhadap perilaku pengguna dalam melakukan pembelian produk. Dataset mencakup sekitar 588 ribu pengguna dengan informasi mengenai:
- user id : id pengguna secara unik
- test group : jika "ads" maka user tersebut melihat iklan, jika "psa" maka user melihat pengumuman layanan masyarakat
- converted : "True" jika user membeli produk, "False" jika tidak
- total ads : jumlah iklan yang dilihat oleh user
- most ads days : hari dimana user tersebut melihat jumlah iklan terbanyak
- most ads hour : jam dalam sehari dimana user melihat jumlah iklan terbanyak

# Konten
Analisis ini mencakup beberapa tahap :

1. Data Cleaning
    - Menangani outlier pada variabel total ads yang menunjukkan nilai ekstrim (hingga 2065 iklan) dibandingkan median (13) dan mean (24.82).
    - Menghapus anomali untuk meningkatkan kualitas data.

2. Objective
    - Mengetahui apakah penayangan iklan digital efektif meningkatkan conversion rate dibandingkan PSA.
    - Mengevaluasi dampak jumlah iklan dan waktu paparan iklan terhadap konversi.

3. Success Metrics
    - Conversion Rate → seberapa besar pengguna melakukan pembelian setelah melihat iklan.
    - Guardrail Metrics → memastikan jumlah paparan iklan dan pola jam/hari tidak memberikan dampak negatif yang signifikan.

4. Hypothesis Testing
    - H0: Tidak ada perbedaan signifikan tingkat konversi antara grup ads dan psa.
    - H1: Grup ads memiliki tingkat konversi yang lebih tinggi dibandingkan grup psa.

# Temuan Penting
1. Conversion Rate (CVR):
    - Grup ads: 1.34%
    - Grup psa: 1.06%
      
    → Peningkatan signifikan dengan p-value = 0.0002 < 0.05.

2. Paparan Iklan (Total Ads):
    - Rata-rata ads group: 24.82 iklan
    - Rata-rata psa group: 24.76 iklan
      
    → Selisih kecil, namun uji statistik (p-value = 0.0000) menunjukkan sistem menayangkan iklan berbeda antar grup.

# Rekomendasi yang bisa ditindaklanjuti
1. Optimalkan kampanye digital karena terbukti lebih efektif meningkatkan conversion rate dibandingkan psa
2. Pantau tren paparan iklan untuk memastikan tidak terjadi overeksposure yang bisa mengganggu pengalaman pengguna
3. Evaluasi variasi konten iklan (dari segi UI atau UX) untuk mendorong kenaikan konversi lebih tinggi
