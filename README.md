# algoritma_analizi2
 
Program C++ dilinde yazılmış olup dört fonksiyon ve bir ana fonksiyondan oluşmaktadır.

İlk işlev, a tamsayı dizisini ve boyutunu girdi olarak alır ve diziyi -10 ile 10 arasında rastgele tamsayılarla doldurur. İkinci işlev function1, girdi olarak aynı tamsayı dizisini ve boyutunu alır ve diziyi kullanarak artan düzende sıralar. kabarcık sıralama algoritması. Üçüncü işlev function2, girdi olarak aynı tamsayı dizisi a'yı ve boyutunu alır, en yüksek ortalama değere sahip maksimum alt dizi toplamını bulur ve bu ortalama değeri döndürür. Dördüncü işlev function3, iki boyutlu bir tamsayı dizisi g'yi, boyut boyutunu alır ve başka bir iki boyutlu tamsayı dizisini d grafiğin köşeleri arasındaki en kısa yol mesafeleriyle doldurur. Ana işlev bu işlevleri çağırır ve sonuçları yazdırır.

Program önce rasgele tamsayılardan oluşan bir a tamsayı dizisi üretir, bunu işlev1'i kullanarak sıralar ve işlev2'yi kullanarak maksimum alt dizi toplamının ortalama değerini bulur. Ardından sıralanan diziyi ve ortalama değeri yazdırır. Bundan sonra, bir grafiği temsil eden iki boyutlu g dizisini yazdırır, fonksiyon3'ü kullanarak grafiğin köşeleri arasındaki en kısa yol mesafelerini bulur ve d dizisini yazdırır. Son olarak, grafikteki belirli bir tepe noktası için en kısa yol mesafelerini yazdırır. 



Bu program, farklı görevleri yerine getiren dört işlev içerir.

create() işlevi, bir tamsayı dizisini ve boyutunu parametre olarak alır ve diziyi -MAX_W ile MAX_W arasında rasgele tamsayılarla doldurur.

function1() bir tamsayı dizisini ve boyutunu parametre olarak alır ve kabarcık sıralama algoritmasını kullanarak diziyi artan düzende sıralar.

function2() bir tamsayı dizisini ve boyutunu parametre olarak alır ve maksimum altdizi toplamlarının ortalamasını döndürür. Başka bir deyişle, giriş dizisinin her bir alt dizisi için maksimum alt dizi toplamını bulur ve bunların ortalamasını döndürür.

function3() iki boyutlu tamsayı dizileri g ve d'yi ve bunların boyutlarını parametre olarak alır. g'nin 0 değerine sahip olduğu ve d'yi INF olarak ayarladığı hücreler dışında önce g'nin değerlerini d'ye kopyalar. Ardından, ağırlıklı bir grafikte herhangi iki köşe arasındaki en kısa mesafeyi bulmak için Floyd-Warshall algoritmasını uygular.

main() işlevinde, program önce verilen değerlerle bir 2B dizi g başlatır ve boş bir 2B dizi d oluşturur. Ardından rastgele bir a tamsayı dizisi oluşturur ve bunu function1() kullanarak sıralar. Orijinali yazdırır ve bir dizi sıralar.

Ardından, function2()'yi a'ya uygular ve sonucu yazdırır.

Bundan sonra g ve d dizileri ile function3()'ü çağırır ve elde edilen d dizisini yazdırır. Ardından function2()'den elde ettiği ağırlık ile grafiğin köşeleri arasındaki ortalama en kısa mesafeyi bulur ve yazdırır.

Son olarak programın çalışma süresini hesaplar ve yazdırır.
Floyd-Warshall algoritması, graf teorisiyle ilgili bir algoritmadır ve tüm çiftler arasındaki en kısa mesafeleri bulmak için kullanılır. Algoritmanın temel adımları şunlardır:

Başlangıçta, tüm çiftler arasındaki mesafeleri tutacak bir matris oluşturulur. Mesafelerin bilinmediği durumlar için sonsuz değerler atanır.
Graf üzerindeki her bir düğüm için, diğer düğümler üzerinden geçerek tüm çiftler arasındaki mesafeleri güncellemek için tüm kombinasyonları değerlendirir.
Her adımda, geçiş düğümü olarak seçilen düğümler üzerinden geçerek yeni bir en kısa yol olup olmadığı kontrol edilir. Eğer böyle bir yol varsa, matris güncellenir.
Sonuç olarak, matrisdeki her bir hücrede bulunan değerler, çiftler arasındaki en kısa mesafeleri temsil eder.
Floyd-Warshall algoritması, tüm düğümler arasındaki en kısa mesafeleri bulmak için kullanılabilir, ancak büyük veri kümeleri için hesaplama maliyeti yüksek olabilir.
