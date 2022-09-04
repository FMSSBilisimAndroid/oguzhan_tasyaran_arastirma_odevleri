# Lazy Loading vs Eager Loading

## Lazy Loading

Lazy Loading, sayfadaki ögenin ihtiyaç duyulmadığı,kullanılmadığı takdirde çağrılmaması prensibi ile çalışır.Nesneye yeniden ihtiyaç duyulana kadar
bekletilmesi için kullanılır.Bu yöntemde veriler sorguya bağlı olarak çekilir ve veri setinin içindeki tüm dataları yüklemek yerine kullanılacağı an tekrar sorgu atar.

## Eager Loading

Lazy Loading’in tam tersi yönde çalışır. Kullanacağımız nesneleri, nesnenin ihtiyaç anından çok önce yaratır ve bekletir. Eager loading Linq 
sorgusu çalıştırıldığında verilerin tamamını yükler ve hafızaya alır.

## Avantaj/Dezavantajları

Her iki uygulamanında çeşitli avantajları ve dezavantajları bulunmaktadır. Tercih durumu uygulamanın büyüklüğü ve ihtiyaçlarına göre yapılmaktadır. Basit bir veritabanı 
ilişkili kullanıcı ve kullanıcı detay uygulamasını baz alırsak ;
- Lazy loading ile birbiriyle ilişkili olan entityler ihtiyaç oldukça çekilir. Bu da performans açısından yarar sağlayabilir. Ancak Eager Loding'e göre veritabanına çok daha fazla kez bağlanır ve sorgu atar bunun da program için bir maliyeti vardır. 
- Eager loading ise tek sorguda gerekli bilgileri elde eder.

İki uygulamanın arasındaki çalışma hızını değerlendirecek olursak Lazy tekrar tekrar veritabanına bağlanacağı için kayıt sayısı arttıkça Eager Loding'e göre performansında düşüş olacaktır.

