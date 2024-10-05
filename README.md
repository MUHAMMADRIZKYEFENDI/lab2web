# lab2web
# 1. Membuat dokumen HTML
```
<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>CSS Dasar</title> 
</head> 
<body> 
    <header> 
        <h1>CSS Internal dan <i>Inline CSS</i></h1> 
    </header> 
    <nav> 
        <a href="lab2_css_dasar.html">CSS Dasar</a> 
        <a href="lab2_css_eksternal.html">CSS Eksternal</a> 
        <a href="lab1_tag_dasar.html">HTML Dasar</a> 
    </nav> 
    <!-- CSS ID Selector --> 
    <div id="intro"> 
        <h1>Hello World</h1> 
        <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman 
Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat 
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML 
dan CSS.</p> 
        <!-- CSS Class Selector --> 
        <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a> 
    </div> 
</body> 
</html>
```
Screenshot 
![Screenshot (222)](https://github.com/user-attachments/assets/b831f521-2d81-425e-a2c3-022e86d8aed6)


# 2. Mendeklarasikan CSS Internal 
```
<head> 
    <title>CSS Dasar</title> 
    <style> 
        body { 
            font-family:'Open Sans', sans-serif; 
        } 
        header { 
            min-height: 80px; 
            border-bottom:1px solid #77CCEF; 
        } 
        h1 { 
            font-size: 24px; 
            color: #0F189F; 
            text-align: center; 
            padding: 20px 10px; 
        } 
        h1 i { 
            color:#6d6a6b; 
        } 
    </style> 
</head>
```
Screenshot 

![Screenshot (223)](https://github.com/user-attachments/assets/d940eeb9-e8ce-45b4-b057-3fa0f2e947bc)


# 3. Menambahkan Inline CSS 
```
<p style="text-align: center; color: #ccd8e4;">
```
Screenshot 
 

![Screenshot (219)](https://github.com/user-attachments/assets/432c4d5e-17e7-431d-a66f-065808344339)

# 4. Membuat CSS Eksternal 
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut. 
```
nav { 
    background: #20A759; 
    color:#fff; 
    padding: 10px; 
} 
nav a { 
    color: #fff; 
    text-decoration: none; 
    padding:10px 20px; 
} 
nav .active,  
nav a:hover { 
    background: #0B6B3A; 
}
```
Kemudian tambahkan tag <link> untuk merujuk file css yang sudah dibuat pada bagian <head>
```
<head> 
    <!-- menyisipkan css eksternal --> 
    <link rel="stylesheet" href="style_eksternal.css" type="text/css"> 
</head>
```
Screenshot 

![Screenshot (220)](https://github.com/user-attachments/assets/20126e81-7262-4b7e-8cb2-f01a4995b70e)

  
# 5. Menambahkan CSS Selector
```
/* ID Selector */ 
#intro { 
    background: #418fb1; 
    border: 1px solid #099249; 
    min-height: 100px; 
    padding: 10px; 
} 
#intro h1 { 
    text-align: left; 
    border: 0; 
    color: #fff; 
} 
 
/* Class Selector */ 
.button { 
    padding: 15px 20px; 
    background: #bebcbd; 
    color: #fff; 
    display: inline-block; 
    margin: 10px; 
    text-decoration: none; 
} 
.btn-primary { 
    background: #E42A42; 
}
```
Screenshot 
  ![Screenshot (221)](https://github.com/user-attachments/assets/9c905afb-3c73-4282-be9a-a10367c6f4d6)
  # Hasil Eksperimen
1. **Perbedaan Selector Elemen (`h1 {...}`) vs. Selector ID (`#intro h1 {...}`):**
   - Selector elemen menerapkan gaya ke semua elemen `<h1>`, sedangkan selector ID hanya akan mempengaruhi elemen `<h1>` di dalam elemen dengan ID `#intro`.

2. **Urutan Prioritas CSS Internal, Eksternal, dan Inline:**
   - Jika ketiga jenis CSS ini diterapkan pada elemen yang sama, **inline CSS** memiliki prioritas tertinggi, diikuti **CSS eksternal**, dan terakhir **CSS internal**. Misalnya:

```html
<h1 style="color: red;">Judul ini akan berwarna merah karena CSS inline.</h1>
```

3. **Prioritas Selector ID dan Class:**
   - Selector ID memiliki prioritas lebih tinggi dibandingkan selector class, karena ID lebih spesifik.

```html
<p id="paragraf-1" class="text-paragraf">Gaya teks akan mengikuti selector ID.</p>
```

## Kesimpulan
Praktikum ini memberikan pengalaman dalam menggunakan berbagai metode deklarasi CSS dan menunjukkan bagaimana aturan CSS diterapkan dengan berbagai selector dan urutan prioritasnya.

---
