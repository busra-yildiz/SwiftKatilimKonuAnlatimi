# SwiftKatilimKonuAnlatimi
Swift programlama dilinde "katılım" (inheritance) kavramı, bir sınıfın başka bir sınıftan özelliklerini ve işlevselliğini 
miras almasını ifade eder. Yani, bir sınıfın mevcut bir sınıfın tüm özelliklerini (değişkenler ve metodlar) ve davranışlarını 
devralmasına olanak tanır. Miras alınan sınıf "üst sınıf" veya "üst sınıf" olarak adlandırılırken, yeni sınıf "alt sınıf" veya "alt sınıf" 
olarak adlandırılır. İşte Swift'te katılımın nasıl çalıştığını anlatan bir örnek:

class GeometrikSekil {
    var ad: String
    
    init(ad: String) {
        self.ad = ad
    }
    
    func alanHesapla() -> Double {
        return 0.0
    }
}

class Dikdortgen: GeometrikSekil {
    var uzunluk: Double
    var genislik: Double
    
    init(uzunluk: Double, genislik: Double) {
        self.uzunluk = uzunluk
        self.genislik = genislik
        super.init(ad: "Dikdörtgen")
    }
    
    override func alanHesapla() -> Double {
        return uzunluk * genislik
    }
}


Bu örnekte, GeometrikSekil adlı bir üst sınıf tanımlanmıştır. Bu sınıf, herhangi bir geometrik şeklin temel özelliklerini içerir ve 
alanHesapla adlı bir metod bulunur. Daha sonra, Dikdortgen adlı bir alt sınıf tanımlanmıştır. 
Bu sınıf, GeometrikSekil sınıfından miras alır ve ayrıca uzunluk ve genişlik özelliklerine sahiptir. Dikdortgen sınıfı, 
alanHesapla metodunu üst sınıftan devralır ve kendi uyarlamasını sağlar.

Bu şekilde katılım, kodun yeniden kullanılabilirliğini artırır ve sınıfları daha düzenli ve mantıklı bir şekilde organize etmenize yardımcı olur. 
İhtiyaca göre yeni özellikler eklemek veya mevcut davranışları değiştirmek için miras alınan sınıfları genişletebilirsiniz. Swift'te katılım,
güçlü bir nesne yönelimli programlama kavramıdır ve çok sayıda tasarım deseni için temel bir taşıyıcıdır.



