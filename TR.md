# p5.js Türkçe Cheat Sheet

## Yaşam Döngüsü Fonksiyonları

**preload() {}:**
Dışarıdan yüklenmesi gereken kaynakların tanımlandığı fonksiyon. Tüm kaynakların yüklenmesi tamamlanmadan diğer fonksiyonların çalışmasına geçilmez.
```JavaScript
function preload() {
    model = loadModel('teapot.obj');
    img = loadImage('cat.jpg');
}
```

**setup() {}:**
İlk tanımlamaların yapılmasını sağlar.
```JavaScript
function setup() {
    createCanvas(640, 480);
}
```

**draw() {}:**
Oyun döngüsünde olacak olayları ve çizimleri tanımlamayı sağlar.
```JavaScript
function draw() {
    x++;
    rect(x, 100, 50, 50);
}
```

## Çizim Fonksiyonları

**createCanvas():** Çizim yapılacak alanı tanımlar.
```JavaScript
createCanvas(genişlik, yükseklik)
createCanvas(genişlik, yükseklik, WEBGL)
```

**line():** Çizgi çizer.
```JavaScript
line(x1, y1, x2, y2)
```

**rect():** Dikdörtgen çizer.
```JavaScript
rect(x, y, genişlik, yükseklik)
```

**circle():** Daire çizer.
```JavaScript
circle(x, y, çap)
```

**ellipse():** Elips çizer.
```JavaScript
ellipse(x, y, çap)
ellipse(x, y, genişlik, yükseklik)
```

**text():** Metin gösterir.
```JavaScript
text('Metin', x, y[, dikeyMetinSınırı, yatayMetinSınırı])
```

**rectMode():** Tanımlanacak dikdörtgenin konum seçeneklerini belirler.
```JavaScript
rectMode(CORNER) // Sol üst köşeyi başlangıç noktası seçer ve uzunluk değerleri başlangıç koordinatına eklenir

rectMode(CORNERS) // Sol üst köşeyi başlangıç noktası seçer ve uzunluk parametreleri çizimin bitiş koordinatları olarak seçilir

rectMode(CENTER) // Seçilen konum parametreleri dikdörtgenin orta noktası olur ve dikdörtgenin genişliği uzunluk parametreleri olarak alınır

rectMode(RADIUS) // Seçilen konum parametreleri dikdörtgenin orta noktası olur ve uzunluk parametreleri dikdörtgenin genişliğinin yarısını belirler
```

**ellipseMode():** Elips ve daire için, ``rectMode()`` ile aynı şekilde çalışır.
```JavaScript
rectMode(CORNER | CORNERS | CENTER | RADIUS)
```

**fill():** Şeklin içini dolduracak rengi belirler. Şekil fonksiyonlarından önce kullanılır.
```JavaScript
fill(255); // Siyah-beyaz tonlar
fill(255, 255, 255); // RGB
fill([255, 255, 255]); // RGB dizi
fill(255, 255, 255, 255); // RGBA
fill([255, 255, 255, 255]); // RGBA dizi
fill('white'); // HTML renk kodu ismi
```

**stroke():** Şeklin dışına çizilecek çizginin rengini belirler. ``fill()`` ile aynı şekilde kullanılır.
```JavaScript
stroke(255, 255, 255); // RGB
```

**noFill():** Çizimin boyanmamasını sağlar.

**noStroke():** Çizime sınır çizgilerinin çizilmemesini sağlar.

**frameRate():** Saniyede kaç defa çizim yapılacağını belirler.
```JavaScript
frameRate(25);
```

## Genel Fonksiyonlar

**random():** İki değer arasında float formatında rastgele bir sayı döndürür.
```JavaScript
rastgeleSayi = random(2, 5)
```

**int():** Aldığı girdiyi integer formatına dönüştürür.
```JavaScript
tamSayi = int(2.6)
```

**float():** Aldığı girdiyi float formatına dönüştürür.
```JavaScript
ondalikliSayi = float(4)
```

**str():** Aldığı girdiyi string formatına dönüştürür.
```JavaScript
metin = str(8)
```

**abs():** Mutlak değer döndürür.
```JavaScript
sayi = abs(-3)
```

**sin():** Sinüs fonksiyonu.

**cos():** Kosinüs fonksiyonu.

**tan():** Tanjant fonksiyonu.

**degrees():** Radyan değerini dereceye dönüştürür.

**radians():** Derece değerini radyana dönüştürür.

**angleMode():** Açı olarak parametre alan fonksiyonların açıyı yorumlama şeklini belirler.
```JavaScript
angleMode(DEGREES | RADIANS)
```

**createVector():** Vektör oluşturur.
```JavaScript
angleMode(x, y[, z])
```

## Değişkenler
**frameCount:** Çizim başladığından beri kaç kere çizildiğinin sayısı

**width:** Çizim alanı genişliği

**height:** Çizim alanı yüksekliği

**windowWidth:** Sayfa genişliği

**windowHeight:** Sayfa yüksekliği

**displayWidth:** Tüm ekranın genişliği

**displayHeight:** Tüm ekranın yüksekliği

**mouseX:** Mouse'un yatay koordinatı

**mouseY:** Mouse'un dikey koordinatı

**pmouseX:** Mouse'un bir önceki çizimdeki yatay koordinatı

**pmouseY:** Mouse'un bir önceki çizimdeki dikey koordinatı

**key:** Klavyede basılan son tuşun değeri

