# Grokking Deep Learning - Code Reproduction & Theoretical Deep-Dive

Repositori ini berisi reproduksi kode lengkap dan penjelasan teoretis mendalam (*theoretical deep-dive*) dalam Bahasa Indonesia dari buku **"Grokking Deep Learning"** karya **Andrew W. Trask** (Manning Publications, 2019). Disusun untuk memenuhi Tugas Individu Mata Kuliah Deep Learning.

---

## Daftar Isi & Ringkasan Bab (Chapter Summary)

### Chapter 1: Introducing Deep Learning: Why You Should Learn It
* **`Chapter_01_Introducing_Deep_Learning.ipynb`**
* Membahas motivasi mempelajari *deep learning* sebagai alat otomatisasi kecerdasan secara bertahap, dampak ekonominya, serta filosofi pembelajaran *"from scratch"* menggunakan Python dan `NumPy` tanpa menyembunyikan cara kerja algoritma di balik *framework* tingkat tinggi.

### Chapter 2: Fundamental Concepts: How Do Machines Learn?
* **`Chapter_02_Fundamental_Concepts.ipynb`**
* Menguraikan hubungan antara AI, *Machine Learning*, dan *Deep Learning*, perbedaan *Supervised Learning* (mentransformasikan dataset yang diketahui menjadi dataset target) dengan *Unsupervised Learning* (mengelompokkan data ke dalam klaster), perbedaan model *Parametric* (jumlah parameter tetap, belajar via *trial-and-error*) dengan *Nonparametric* (berbasis penghitungan/frekuensi), serta paradigma tiga langkah: **Predict, Compare, Learn**.

### Chapter 3: Introduction to Neural Prediction: Forward Propagation
* **`Chapter_03_Forward_Propagation.ipynb`**
* Membahas langkah **Predict** (*forward propagation*) mulai dari jaringan 1 input & 1 bobot, jaringan multi-input menggunakan *weighted sum* (*dot product*), intuisi kemiripan vektor (logika AND, OR, NOT), jaringan multi-output (*elementwise multiplication*), jaringan multi-input & multi-output (*vector-matrix multiplication*), jaringan bertumpuk (*stacked neural networks* dengan *hidden layer*), hingga aturan dimensi matriks di `NumPy`.

### Chapter 4: Introduction to Neural Learning: Gradient Descent
* **`Chapter_04_Gradient_Descent.ipynb`**
* Membahas langkah **Compare** dan **Learn**: alasan mengkuadratkan kesalahan (*Mean Squared Error*), perbandingan *Hot and Cold Learning* dengan *Gradient Descent*, cara kerja turunan (*derivative*) dalam menghitung arah dan besaran pembaruan bobot (`weight_delta = delta * input`), tiga properti penting (*stopping*, *negative reversal*, *scaling*), fenomena *divergence* (*overshooting*), dan pengendalian laju pembelajaran menggunakan parameter `alpha` ($\alpha$).

### Chapter 5: Learning Multiple Weights at a Time: Generalizing Gradient Descent
* **`Chapter_05_Generalizing_Gradient_Descent.ipynb`**
* Memperluas *gradient descent* pada jaringan multi-input, eksperimen membekukan satu bobot (*freezing one weight*) untuk memahami konsep permukaan kesalahan berdimensi tinggi (*error plane*), *gradient descent* pada jaringan multi-output dan jaringan matriks penuh menggunakan *outer product*, serta visualisasi bobot sebagai cetakan gambar pada klasifikasi digit tulisan tangan.

### Chapter 6: Building Your First Deep Neural Network: Introduction to Backpropagation
* **`Chapter_06_Backpropagation.ipynb`**
* Memperkenalkan masalah lampu lalu lintas (*The Streetlight Problem*), representasi matriks data *lossless*, perbedaan *Full*, *Batch*, dan *Stochastic Gradient Descent*, konsep tekanan naik/turun (*up and down pressure*), bahaya *overfitting* dan *conflicting pressure*, alasan mengapa tumpukan lapisan linear memerlukan fungsi non-linear (`ReLU` untuk menciptakan *conditional/sometimes correlation*), serta algoritma **Backpropagation** untuk membangun jaringan saraf dalam (*3-layer deep neural network*) pertama.

### Chapter 7: How to Picture Neural Networks: In Your Head and on Paper
* **`Chapter_07_How_to_Picture_Neural_Networks.ipynb`**
* Menyederhanakan cara memvisualisasikan jaringan saraf melalui tiga tingkat abstraksi (*Correlation Summarization*, *Local Correlation*, dan *Global Correlation*), representasi balok LEGO (vektor lapisan dan matriks bobot), penentuan dimensi matriks secara otomatis, serta notasi aljabar ringkas $l_2 = \text{relu}(l_0 W_0) W_1$.

### Chapter 8: Learning Signal and Ignoring Noise: Introduction to Regularization and Batching
* **`Chapter_08_Regularization_and_Batching.ipynb`**
* Menganalisis masalah *overfitting* pada jaringan 3 lapis di dataset digit tulisan tangan (analogi cetakan garpu tanah liat), perbedaan memorisasi vs generalisasi, teknik regularisasi **Early Stopping**, mekanisme dan alasan bekerjanya **Dropout** (membuat jaringan besar berperilaku seperti ansambel jaringan kecil), serta percepatan dan stabilisasi pelatihan dengan **Mini-Batch Gradient Descent**.

### Chapter 9: Modeling Probabilities and Nonlinearities: Activation Functions
* **`Chapter_09_Activation_Functions.ipynb`**
* Membahas sifat matematis fungsi aktivasi, perbandingan fungsi aktivasi lapisan tersembunyi (`sigmoid`, `tanh`, dan `ReLU`) beserta rumus turunannya, penggunaan fungsi **Softmax** pada lapisan keluaran untuk memodelkan distribusi probabilitas multikelas, serta peningkatan akurasi jaringan klasifikasi digit menggunakan kombinasi `tanh` dan `softmax`.

### Chapter 10: Neural Learning About Edges and Corners: Intro to Convolutional Neural Networks
* **`Chapter_10_Convolutional_Neural_Networks.ipynb`**
* Memperkenalkan struktur spasial **Convolutional Neural Networks (CNN)**, konsep berbagi bobot (*weight sharing*) melalui jendela filter/kernel lokal untuk mendeteksi fitur tepi dan sudut secara invarian terhadap pergeseran, serta implementasi lapisan konvolusional dari nol dalam `NumPy`.

### Chapter 11: Neural Networks That Understand Language: $\text{king} - \text{man} + \text{woman} == ?$
* **`Chapter_11_Word_Embeddings_and_NLP.ipynb`**
* Membahas dasar-dasar *Natural Language Processing* (NLP), efisiensi lapisan **Word Embedding** (mengganti perkalian matriks *one-hot* raksasa dengan penjumlahan baris bobot), klasifikasi sentimen ulasan film IMDB, pencarian kemiripan semantik kata, pelatihan konteks *fill-in-the-blank*, serta aritmatika analogi vektor kata ($\text{king} - \text{man} + \text{woman} \approx \text{queen}$).

### Chapter 12: Neural Networks That Write Like Shakespeare: Recurrent Layers for Variable-Length Data
* **`Chapter_12_Recurrent_Neural_Networks.ipynb`**
* Mengatasi keterbatasan *Bag-of-Words* yang mengabaikan urutan kata dengan memperkenalkan **Recurrent Neural Networks (RNN)**, matriks transisi identitas vs matriks rekuren yang dipelajari, *forward propagation* untuk kalimat dengan panjang arbitrer, serta algoritma **Backpropagation Through Time (BPTT)**.

### Chapter 13: Introducing Automatic Optimization: Let's Build a Deep Learning Framework
* **`Chapter_13_Deep_Learning_Framework_Autograd.ipynb`**
* Membangun kerangka kerja *deep learning* berorientasi objek dari nol: kelas `Tensor` dengan pelacakan graf komputasi otomatis (**Autograd**), penghitungan referensi untuk *multiuse tensors*, pengoptimal `SGD`, serta abstraksi lapisan modular (`Layer`, `Linear`, `Sequential`, `Tanh`, `Sigmoid`, `Embedding`, `MSELoss`, `CrossEntropyLoss`, dan `RNNCell`).

### Chapter 14: Learning to Write Like Shakespeare: Long Short-Term Memory
* **`Chapter_14_Long_Short_Term_Memory_LSTM.ipynb`**
* Membahas pemodelan bahasa tingkat karakter (*character language modeling*), efisiensi **Truncated BPTT**, fenomena **Vanishing and Exploding Gradients** pada RNN standar, serta arsitektur sel **Long Short-Term Memory (LSTM)** beserta intuisi keempat gerbangnya (*Forget Gate*, *Input Gate*, *Candidate Gate*, dan *Output Gate*).

### Chapter 15: Deep Learning on Unseen Data: Introducing Federated Learning
* **`Chapter_15_Federated_Learning.ipynb`**
* Mengupas privasi data dalam *deep learning*, pelatihan terdesentralisasi dengan **Federated Learning** pada deteksi spam, celah kebocoran privasi pada gradien bobot, proteksi menggunakan **Secure Aggregation**, serta komputasi di atas data terenkripsi dengan **Homomorphic Encryption** (sistem kriptografi Paillier).

### Chapter 16: Where to Go From Here: A Brief Guide
* **`Chapter_16_Where_to_Go_From_Here.ipynb`**
* Panduan langkah lanjutan setelah menguasai fondasi internal *deep learning*, termasuk tabel pemetaan langsung dari kerangka kerja `Tensor` yang dibangun di Bab 13 menuju sintaks **PyTorch** modern.

---
