Jawaban Refleksi:

1. Mengapa power() dipanggil di dalam term()?,

Karena operator pangkat (^) memiliki prioritas lebih tinggi dibandingkan operator perkalian (_) dan pembagian (/).
Dengan menempatkan power() di dalam term(), maka proses parsing akan mengikuti aturan precedence:
^ > _ / > + -

2. Apa yang terjadi jika variabel tidak ada di symbol_table?

Akan terjadi error pada fase analisis semantik, yaitu:
"Semantic Error: Undefined variable"

Hal ini karena compiler memeriksa apakah variabel sudah didefinisikan sebelumnya.

3. Mengapa a ^ 2 muncul lebih dulu di TAC?

Karena TAC mengikuti struktur Abstract Syntax Tree (AST), di mana operasi dengan prioritas lebih tinggi akan dieksekusi lebih dulu.

Sehingga:
t1 = a ^ 2
t2 = b \* c
t3 = t1 + t2
