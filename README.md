# D121231078_PemogramanWeb

# Portfolio Website - Christianto Trisatria Lapu

**NIM:** D121231078<br>
**Nama:** Christianto Trisatria Lapu<br>
**Program Studi:** Teknik Informatika<br>
**Universitas:** Universitas Hasanuddin

## Deskripsi Website

Website ini adalah portfolio pribadi yang menampilkan biodata dan informasi profesional Christianto Trisatria Lapu. Website menggunakan layout flex horizontal dengan desain modern minimalis yang didominasi warna biru dan hitam. Panel kiri berisi informasi detail dalam format grid card, sedangkan panel kanan menampilkan foto profil dengan efek border yang menarik.

## Fitur Website

- **Layout Responsif**: Menyesuaikan dengan berbagai ukuran layar (desktop, tablet, mobile)
- **Gradient Background**: Menggunakan gradien linear untuk elemen visual yang menarik
- **Animasi Hover**: Efek interaktif pada card dan elemen tertentu
- **Dark Theme**: Skema warna gelap dengan aksen biru yang modern
- **Typography Hierarchy**: Struktur font yang jelas dan mudah dibaca
- **Animated Background**: Efek bintang berkedip untuk background yang dinamis

## Struktur HTML

### HTML Tags yang Digunakan

#### 1. Document Structure
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Data Diri</title>
    <link rel="stylesheet" href="style.css">
</head>
```

**Penjelasan:**
- `<!DOCTYPE html>`: Deklarasi dokumen HTML5
- `<html lang="id">`: Tag root dengan bahasa Indonesia
- `<meta charset="UTF-8">`: Pengkodean karakter Unicode
- `<meta name="viewport">`: Konfigurasi responsive design untuk mobile
- `<title>`: Judul halaman "Data Diri" yang muncul di tab browser
- `<link rel="stylesheet">`: Menghubungkan file CSS eksternal (style.css)

#### 2. Body Structure
```html
<body>
    <div class="container">
        <div class="profile-left">
            <!-- Konten informasi -->
        </div>
        <div class="profile-right">
            <!-- Foto profil -->
        </div>
    </div>
</body>
```

**Penjelasan:**
- `<body>`: Kontainer utama konten halaman
- `<div class="container">`: Container utama dengan flexbox layout
- `<div class="profile-left">`: Panel kiri untuk informasi detail
- `<div class="profile-right">`: Panel kanan untuk foto profil

#### 3. Profile Information Section
```html
<div class="profile-info">
    <h2 class="greeting">Hello, My Name!</h2>
    <h1 class="profile-name">CHRISTIANTO TRISATRIA LAPU</h1>
    <p class="profile-title">
        Mahasiswa • Teknik Informatika • Universitas Hasanuddin
    </p>
    <p class="profile-description">
        Saya sedang menempuh pendidikan di Universitas Hasanuddin...
    </p>
</div>
```

**Penjelasan:**
- `<div class="profile-info">`: Container untuk informasi utama profil
- `<h2 class="greeting">`: Heading level 2 untuk sapaan
- `<h1 class="profile-name">`: Heading utama untuk nama (typography hierarchy)
- `<p class="profile-title">`: Paragraf untuk status dan institusi
- `<p class="profile-description">`: Deskripsi singkat tentang diri

#### 4. Profile Details Grid
```html
<div class="profile-details">
    <div class="info-item">
        <div class="info-icon">
            <svg viewBox="0 0 24 24">
                <path d="M12 2C13.1 2 14 2.9..."/>
            </svg>
        </div>
        <div class="info-content">
            <div class="info-label">NIM</div>
            <div class="info-value">D121231078</div>
        </div>
    </div>
</div>
```

**Penjelasan:**
- `<div class="profile-details">`: Container grid untuk kartu informasi
- `<div class="info-item">`: Kartu individual untuk setiap informasi
- `<div class="info-icon">`: Container untuk ikon SVG
- `<svg viewBox="0 0 24 24">`: SVG icon dengan viewBox untuk scalability
- `<div class="info-content">`: Container untuk konten teks
- `<div class="info-label">`: Label untuk jenis informasi
- `<div class="info-value">`: Nilai/data informasi

#### 5. SVG Icons Implementation
```html
<svg viewBox="0 0 24 24">
    <path d="M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22..."/>
</svg>
```

**Penjelasan:**
- `viewBox="0 0 24 24"`: Mendefinisikan koordinat dan dimensi SVG
- `<path d="...">`: Path data untuk menggambar bentuk ikon
- SVG digunakan untuk ikon yang scalable dan crisp di semua ukuran layar

#### 6. Hobby Tags
```html
<div class="hobby-tags">
    <span class="hobby-tag">Main Musik</span>
    <span class="hobby-tag">Gaming</span>
    <span class="hobby-tag">Editing Video</span>
    <span class="hobby-tag">Photography</span>
</div>
```

**Penjelasan:**
- `<div class="hobby-tags">`: Container untuk tag hobi
- `<span class="hobby-tag">`: Individual tag untuk setiap hobi
- Menggunakan flexbox untuk layout yang responsif

#### 7. Photo Section
```html
<div class="profile-right">
    <div class="photo-container">
        <div class="profile-photo">
            <img src="image/foto1.jpeg" alt="photo-container" />
            <div class="photo-placeholder" style="display: flex">
                <svg viewBox="0 0 24 24">...</svg>
                <span>Foto</span>
            </div>
        </div>
    </div>
</div>
```

**Penjelasan:**
- `<div class="photo-container">`: Container untuk positioning foto
- `<div class="profile-photo">`: Frame foto dengan styling khusus
- `<img src="image/foto1.jpeg">`: Gambar profil dengan path relatif
- `<div class="photo-placeholder">`: Placeholder ketika foto tidak ada
- Inline style `display: flex` untuk override default styling

## CSS Styling

### 1. Global Reset & Base Styles
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    background: #0a0a0a;
    color: white;
    min-height: 100vh;
    overflow-x: hidden;
    position: relative;
}
```

**Fungsi:**
- Universal selector (*) untuk reset default browser styling
- `box-sizing: border-box` untuk predictable sizing behavior
- Font stack dengan fallback fonts untuk compatibility
- `line-height: 1.6` untuk readability yang optimal
- Dark background (#0a0a0a) untuk modern dark theme
- `overflow-x: hidden` untuk mencegah horizontal scroll
- `position: relative` untuk positioning context

### 2. Main Container Layout
```css
.container {
    display: flex;
    min-height: 100vh;
    align-items: center;
    max-width: 1400px;
    margin: 0 auto;
    padding: 60px 40px;
    gap: 80px;
}
```

**Fungsi:**
- Flexbox untuk horizontal layout
- `min-height: 100vh` untuk full viewport height
- `align-items: center` untuk vertical centering
- `max-width: 1400px` untuk optimal reading width
- `margin: 0 auto` untuk horizontal centering
- `gap: 80px` untuk spacing antar panel

### 3. Left Panel Styling
```css
.profile-left {
    flex: 1;
    max-width: 1000px;
}
```

**Fungsi:**
- `flex: 1` untuk mengambil space yang tersisa
- `max-width: 1000px` untuk membatasi lebar maksimum content

### 4. Typography Hierarchy
```css
.greeting {
    color: #4a9eff;
    font-size: 24px;
    font-weight: 400;
    margin-bottom: 0px;
}

.profile-name {
    font-size: 48px;
    font-weight: 700;
    color: white;
    margin-bottom: 1px;
    letter-spacing: -0.5px;
}

.profile-title {
    color: #4a9eff;
    font-size: 18px;
    font-weight: 500;
    margin-bottom: 0px;
}
```

**Fungsi:**
- Hierarchy dengan ukuran font yang berbeda (48px > 24px > 18px)
- Color coding: putih untuk nama, biru (#4a9eff) untuk accent
- `letter-spacing: -0.5px` untuk tightening pada heading besar
- `font-weight` bervariasi untuk contrast visual

### 5. Grid Layout untuk Details
```css
.profile-details {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
    margin-top: 30px;
}
```

**Fungsi:**
- CSS Grid dengan responsive columns
- `auto-fit` untuk automatic column adjustment
- `minmax(280px, 1fr)` untuk minimum width 280px
- `gap: 20px` untuk consistent spacing

### 6. Info Cards Design
```css
.info-item {
    display: flex;
    align-items: center;
    background: rgba(255, 255, 255, 0.05);
    padding: 20px;
    border-radius: 15px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    transition: all 0.3s ease;
}

.info-item:hover {
    background: rgba(255, 255, 255, 0.08);
    transform: translateY(-2px);
}
```

**Fungsi:**
- Flexbox untuk horizontal alignment
- Semi-transparent background untuk subtle effect
- `border-radius: 15px` untuk modern rounded corners
- Subtle border dengan low opacity
- Hover effects dengan `transform` dan background change
- `transition: all 0.3s ease` untuk smooth animations

### 7. Icon Styling
```css
.info-icon {
    width: 45px;
    height: 45px;
    border-radius: 12px;
    background: linear-gradient(135deg, #4a9eff, #6366f1);
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 15px;
    flex-shrink: 0;
}

.info-icon svg {
    width: 22px;
    height: 22px;
    fill: white;
}
```

**Fungsi:**
- Fixed size (45x45px) untuk consistency
- `linear-gradient(135deg, #4a9eff, #6366f1)` untuk attractive gradient
- Flexbox centering untuk SVG icons
- `flex-shrink: 0` untuk prevent shrinking
- SVG styling dengan `fill: white`

### 8. Content Typography
```css
.info-label {
    font-size: 13px;
    color: #888;
    font-weight: 500;
    margin-bottom: 4px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.info-value {
    font-size: 16px;
    color: white;
    font-weight: 600;
}
```

**Fungsi:**
- Size contrast (13px label vs 16px value)
- Color hierarchy (#888 muted vs white prominent)
- `text-transform: uppercase` untuk labels
- `letter-spacing: 0.5px` untuk improved readability pada uppercase

### 9. Hobby Tags
```css
.hobby-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 5px;
}

.hobby-tag {
    background: linear-gradient(135deg, #4a9eff, #6366f1);
    color: white;
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 13px;
    font-weight: 500;
}
```

**Fungsi:**
- Flexbox dengan wrap untuk multiple lines
- Gradient background matching icon colors
- `border-radius: 20px` untuk pill-shaped tags
- Compact padding untuk badge appearance

### 10. Photo Container
```css
.profile-photo {
    width: 350px;
    height: 450px;
    border-radius: 25px;
    position: relative;
    overflow: hidden;
    background: linear-gradient(135deg, #2a2a2a, #1a1a1a);
    border: 3px solid rgba(74, 158, 255, 0.3);
    box-shadow: 0 25px 60px rgba(0, 0, 0, 0.5), 
                0 0 0 1px rgba(74, 158, 255, 0.1),
                inset 0 1px 0 rgba(255, 255, 255, 0.1);
}

.profile-photo img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 22px;
}
```

**Fungsi:**
- Fixed dimensions (350x450px) untuk portrait aspect ratio
- Multiple `box-shadow` untuk depth dan border effects
- `object-fit: cover` untuk maintain aspect ratio
- `border-radius` yang sedikit lebih kecil pada img untuk perfect fit
- Gradient border dengan semi-transparent blue accent

### 11. Background Animation
```css
@keyframes twinkle {
    0%, 100% {
        opacity: 0;
    }
    50% {
        opacity: 1;
    }
}

.star {
    position: absolute;
    width: 2px;
    height: 2px;
    background: rgba(74, 158, 255, 0.8);
    border-radius: 50%;
    animation: twinkle 2s infinite;
}
```

**Fungsi:**
- CSS animation untuk twinkling effect
- `position: absolute` untuk free positioning
- Small size (2x2px) untuk subtle effect
- `border-radius: 50%` untuk perfect circles
- Different animation durations untuk variety

### 12. Responsive Design

#### Desktop Large (1024px)
```css
@media (max-width: 1024px) {
    .container {
        gap: 60px;
        padding: 40px 30px;
    }
    .profile-right {
        flex: 0 0 300px;
    }
    .profile-photo {
        width: 280px;
        height: 380px;
    }
}
```

#### Tablet (768px)
```css
@media (max-width: 768px) {
    .container {
        flex-direction: column;
        gap: 40px;
        padding: 30px 20px;
        text-align: center;
    }
    .profile-left {
        order: 2;
    }
    .profile-right {
        order: 1;
    }
}
```

**Fungsi Responsive:**
- Progressive enhancement dari desktop ke mobile
- `flex-direction: column` untuk vertical stacking di mobile
- CSS `order` untuk mengubah urutan tampilan (foto dulu, konten kedua)
- `text-align: center` untuk mobile-friendly alignment
- Proportional scaling untuk foto dan spacing

## Advanced CSS Techniques

### 1. CSS Grid Auto-fit
```css
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
```
- Otomatis adjust jumlah kolom berdasarkan available space
- Minimum width 280px untuk optimal card size

### 2. Multiple Box Shadows
```css
box-shadow: 
    0 25px 60px rgba(0, 0, 0, 0.5),
    0 0 0 1px rgba(74, 158, 255, 0.1),
    inset 0 1px 0 rgba(255, 255, 255, 0.1);
```
- Layered shadows untuk realistic depth
- Inset shadow untuk subtle inner highlight

### 3. CSS Transforms untuk Interaktivitas
```css
transform: translateY(-2px);
```
- Subtle lift effect pada hover
- Hardware-accelerated untuk smooth performance

### 4. Gradient Implementation
```css
background: linear-gradient(135deg, #4a9eff, #6366f1);
```
- Diagonal gradient (135deg) untuk dynamic appearance
- Color scheme consistency across elements

## Kesimpulan

Website ini mendemonstrasikan penggunaan teknik modern CSS dan HTML:

- **Semantic HTML**: Struktur yang meaningful dan accessible
- **Flexbox & Grid**: Layout system yang powerful dan responsive  
- **CSS Animations**: Subtle animations untuk enhanced UX
- **Responsive Design**: Mobile-first approach dengan progressive enhancement
- **SVG Icons**: Scalable vector graphics untuk crisp icons
- **Typography Hierarchy**: Clear information architecture
- **Color Psychology**: Dark theme dengan blue accents untuk professional appearance
- **Performance Optimization**: Hardware-accelerated transforms dan efficient selectors

