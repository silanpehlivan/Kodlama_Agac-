📈 Kodlama Ağacı (İkili Arama Ağacı Uygulaması)

Bu proje, C# dili kullanılarak geliştirilmiş basit bir ikili arama ağacı (Binary Search Tree - BST) uygulamasıdır. Kullanıcıların sayısal değerler ekleyebildiği ve bu değerleri sıralı bir şekilde görüntüleyebildiği konsol tabanlı bir yapıdır. Ağaç veri yapısının temel mantığını ve çalışma prensibini göstermeyi amaçlamaktadır.

---

🎯 Projenin Amacı

Bu projenin temel amacı, ikili arama ağacı veri yapısının C# ile nasıl oluşturulduğunu ve yönetildiğini göstermektir. Bu kapsamda:

- İkili arama ağacına eleman ekleme işlemi gösterilir  
- Sıralı gezinti (in-order traversal) mantığı uygulanır  
- Ağaç veri yapısının çalışma prensibi anlaşılır  
- Nesne yönelimli programlama pratiği geliştirilir  

---

📚 İkili Arama Ağacı Nedir?

İkili arama ağacı (Binary Search Tree - BST), her düğümün en fazla iki çocuk düğüme sahip olduğu ve belirli bir sıralama kuralına göre organize edilen bir veri yapısıdır.

### Temel Kurallar:

1. Sol alt ağaçtaki tüm değerler, düğüm değerinden küçüktür  
2. Sağ alt ağaçtaki tüm değerler, düğüm değerinden büyüktür  
3. Her düğüm en fazla iki çocuk düğüme sahiptir  

### Avantajları:

- Veri arama işlemleri hızlıdır (ortalama O(log n))  
- Veri sıralı şekilde tutulabilir  
- Dinamik veri yapısıdır (boyut esnek)  

---

⚙️ Teknik Detaylar

| Özellik | Açıklama |
|----------|----------|
| Dil | C# |
| Platform | .NET Framework |
| Paradigma | Nesne Yönelimli Programlama (OOP) |
| Uygulama Türü | Konsol Uygulaması |
| IDE | Visual Studio |

---

💻 Implementasyon Detayları

Projenin ana yapısı `AgacDugumu` ve `KodlamaAgaci` sınıfları üzerine kurulmuştur.

- `AgacDugumu`: Ağacın her bir düğümünü temsil eder  
- `KodlamaAgaci`: Ekleme ve sıralı gezinti işlemlerini yönetir  

---

### 📌 Ekleme (Insertion) Metodu

```csharp
public void Ekle(int deger)
{
    Kok = EkleRec(Kok, deger);
}

private AgacDugumu EkleRec(AgacDugumu kok, int deger)
{
    if (kok == null)
    {
        kok = new AgacDugumu(deger);
        return kok;
    }

    if (deger < kok.Deger)
    {
        kok.Sol = EkleRec(kok.Sol, deger);
    }
    else if (deger > kok.Deger)
    {
        kok.Sag = EkleRec(kok.Sag, deger);
    }

    return kok;
}
```

---

Main metodu içerisinde kullanıcıdan alınan değerler ağaca eklenir ve ardından sıralı gezinti ile ekrana yazdırılır.

---

🚀 Kurulum ve Çalıştırma

1. Projeyi indirip klasöre çıkarın  
2. `Kodlama_Agacı.sln` dosyasını Visual Studio ile açın  
3. Projeyi derleyin (Build Solution)  
4. Uygulamayı çalıştırın (F5 veya Start)  

---

📂 Proje Yapısı

```
Kodlama_Agaci-master/
├── App.config
├── Kodlama_Agacı.csproj
├── Kodlama_Agacı.sln
├── LICENSE
├── Program.cs
└── Properties/
    └── AssemblyInfo.cs
```

---

📜 Lisans

Bu proje MIT Lisansı kapsamında lisanslanmıştır. Detaylar LICENSE dosyasında yer almaktadır.

---

👩‍💻 Yazar

Şilan Pehlivan
