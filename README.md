# Association Rules

*Association Rules* merupakan hubungan antara kombinasi beberapa item (barang, orang, penduduk ataupun yang diwakili oleh kata benda) yang sering muncul bersamaan. Pada *Association Rules* terdapat 3 satuan umum yang digunakan yakni:
1. __Support__  
    indikasi seberapa sering itemset muncul di dataset. 
2. __Confidence__  
    indikasi seberapa sering aturan itu terbukti benar. 
3. __Lift__  
    adalah  suatu  ukuran  untuk  mengetahui  kekuatan  aturan  asosisasi  (*association  rule*) yang  telah  terbentuk.

# Apriori Algorithm
*Apriori Algorithm* menggunakan frequent itemsets untuk menghasilkan aturan asosiasi, dan dirancang untuk bekerja pada database yang berisi transaksi.
Secara umum, algoritma Apriori memiliki langkah-langkah sebagai berikut:  
1. Menentukan minimum support.
2. Iterasi 1 : hitung item-item dari support(transaksi yang memuat seluruh item) dengan men-scan database untuk 1-itemset, setelah 1-itemset didapatkan, dari 1-itemset apakah diatas minimum support, apabila telah memenuhi minimum support, 1-itemset tersebut akan menjadi pola frequent tinggi.
3. Iterasi 2 : untuk mendapatkan 2-itemset, harus dilakukan kombinasi dari k-itemset sebelumnya, kemudian scan database lagi untuk hitung item-item yang memuat support. itemset yang memenuhi minimum support akan dipilih sebagai pola frequent tinggi dari kandidat.
4. Tetapkan nilai k-itemset dari support yang telah memenuhi minimum support dari k-itemset.
5. Lakukan proses untuk iterasi selanjutnya hingga tidak ada lagi k-itemset yang memenuhi minimum support.  

# Frequent Pattern Growth Algorithm (FP-Growth)  
Algoritma ini merupakan perbaikan dari metode Apriori. Berbeda dengan algoritma Apriori dimana kita menghasilkan kandidat frequent-itemset disetiap iterasi, FP-Growth bekerja dengan menggunakan FP-Tree.  
Adapun langkah-langkah yang diperlukan dalam algoritma FP-Growth adalah sebagai berikut:  
1. Deduksi item yang sering dipesan. Untuk item dengan frekuensi yang sama, urutannya diberikan menurut urutan abjad.  
2. Bangun pohon FP berdasarkan transaksi yang tersedia  
3. Dari FP-Tree yang ada, buat FP-conditional tree untuk setiap item (atau itemset).
4. Tentukan pola *frequent pattern*

> untuk kode dan penjelasannya silahkan ke [Machine Learning.ipynb](https://github.com/takdim/Association_Rules/blob/main/Machine_Learning.ipynb)
