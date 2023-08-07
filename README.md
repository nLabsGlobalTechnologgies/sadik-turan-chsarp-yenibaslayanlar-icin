#Veri Tipleri
#Byte: <br/>Bellek üzerinde 1 byte yer kaplar. 0’dan başlayarak 255 değerine kadar olan tam sayı aralığında değerler alabilir.<br/>
#Sbyte: <br/>Byte gibi bellek üzerinde kapladığı yer aynıdır. - 128 ile 127 arasında bulunan tam sayı değerlerini alabilir.<br/>
#Short: <br/>2 Byte boyutundadır. -32768 ile 32767 arasında bulunan tam sayı değerlerini alır.<br/>
#Ushort: <br/>Sbyte gibi pozitif değerleri alır. 0 ile 65535 arasında bulunan tam sayıları alır.<br/>
#Integer(int): <br/>Herkesin sıklıkla kullandığı veri tipidir.Bellek üzerinde 4 Byte yer kaplar. - 2³¹ ile 2³¹ -1 arasında bulunan tam sayıları alır.<br/>
#Uint: <br/>Integer veri tipinin pozitif değerler alan halidir. 0 ile 2×2³¹-1 arasındaki değerleri alır.<br/>
#Long: <br/>Bellek üzerinde 8 Byte yer kaplar.Integer veri tipinden daha uzun tam sayı değerlerini bünyesinde tutabilir. -2⁶³ ile 2⁶³-1 arasındaki değerler tanımlanabilir.<br/>
#Ulong: <br/>0 ile 2×2⁶³ arasındaki tam sayıları tutan veri tipidir.<br/>
Ondalıklı sayı türünde eleman tutan veri tipleri şu şekildedir;<br/>
#Float: <br/>Bellekte 4 Byte yer kaplar.Ondalık sayı türünde eleman tutan veri tipidir. - 3.4 * 10³⁸ ile 3.4 * 10³⁸ arasında bulunan değerleri alır.<br/>
#Double: <br/>Bellek üzerinde 8 Byte yer kaplar.Ondalık sayı türünde elemanlar alan veri tipidir. - 1.7 * 10³⁰⁸ ile 1.7 * 10³⁰⁸ arasındaki değerleri alır.<br/>
#Decmial: <br/>Ondalıklı elemanları tutan veri tipidir.Virgülden sonra 28 basamağa kadar destekleyen 128 bit uzunluğuna sahip kesirli bir sayımız var ise kullanacağımız veri tipidir.<br/>
Diğer C# Primitive veri tipleri şu şekildedir;<br/>
#Char: <br/>Tek karakter türünde değerler alır.Tanımlamaları oluştururken yalnızca bir rakam, işaret veya harf kullanabiliriz. Yapılan tanımlamalar diğer veri tiplerinin aksine tek tırnak arasında yapılmalıdır.<br/>
#Boolean: <br/>Diğer veri tiplerinin aksine sadece 2 adet değer alır.Bu değerler true veya false’dir.Bellek üzerinde bir bit yer kaplar. Mantıksal veri tipleri olarak da bilinir.<br/>

            //Degişkenler
            //byte sayi1 = 255;
            //short sayi2 = 500;
            //int sayi3 = 3000;
            //long sayi4 = 1000000;
            //float sayi5 = 2.5f;
            //double sayi6 = 12.5;
            //decimal sayi7 = 125.56m;
            //char character = 'A';
            //bool isOk = true;
            //string adsoyad = "Cuma KÖSE";
            //Console.WriteLine(sayi1);
            //Console.WriteLine(sayi2);
            //Console.WriteLine(sayi3);
            //Console.WriteLine(sayi4);
            //Console.WriteLine(sayi5);
            //Console.WriteLine(sayi6);
            //Console.WriteLine(sayi7);
            //Console.WriteLine(character);
            //Console.WriteLine(isOk);
            //Console.WriteLine(adsoyad);

            // Kilo bilgisi tutulacak bir degişken (byte, short, int, long)
            //byte kilo = 100;
            // Araç KM bilgisini tutacak bir degişken
            //int aracKm = 1000000;
            // Müşteri ID bilgisini tutacak bir degişken
            //long musteriId = 1000000000;
            // Bir ürünün satışta mı degilmi bilgisini tutacak bir degişken
            //bool satis = true;
            // Maaş bilgisini tutacak bir degişken
            //decimal maas = 3000.56m;
            // Ögrenci bilgisini tutacak bir degişken
            //string adSoyad = "Ali Kocabaş";
            // Şube kodunu tutacak bir degişken(Örnegin : A)
            //char subeKod = 'A';

            //Console.WriteLine(kilo);
            //Console.WriteLine(aracKm);
            //Console.WriteLine(musteriId);
            //Console.WriteLine(satis);
            //Console.WriteLine(maas);
            //Console.WriteLine(adSoyad);
            //Console.WriteLine(subeKod);


            //Type Conversion(Tür Dönüşümleri)
            // 1 Implicit type conversion (Bilinçsiz tür dönüşümleri)
            //burada önemli olan küçük veri büyük veriye sorunsuz dönüşebilir bir netlik belirtmeye yani örnek olarak (int)a gibi belirtmeye gerek yoktur
            //byte byteVeri = 255;
            //int intVeri = byteVeri;
            //Console.WriteLine(intVeri);

            // 2 Explicit type conversion (Bilinçli tür dönüşümleri)
            //burada önemli olan büyük veri küçük veriye dönüşürken veri kaybı olabilir bunu bilerek yapmamız gerekir aksi halde veri kaybına neden olacaktır
            //örnek olarak dönüştürecegimiz veriden fazla olursa kayıplar olacak
            //lakin burada tip belirtmemiz gerekir örnek olarak byte sayi2=(byte)sayi1; şeklinde hangi türe dönüştüreceksek belirtmemiz gerekmektedir
            Console.WriteLine("-------------------------------");
            short sayi1 = 2000;
            byte sayi2 = (byte)sayi1;
            Console.WriteLine(sayi2);
            // aşagıda ise veri sorunsuz aktarılır çünkü büyük veride saklı deger aslında küçük verinin kapasitesini aşmamaktadır. başarılı dönüşüm gerçekleşir
            int iVeri = 5;
            byte bVeri = (byte)iVeri;
            Console.WriteLine(bVeri);

            //Convert() ve Parse() (Uyumsuz tip Dönüşümü)
            // burada tip dönüşümü int.Parse yada Convert.ToInt16 yada Convert.ToInt23 veya Convert.ToInt64 olarak dönüştürürüz 16 yani short veriye 32 olunca ise int veriye 64 olunca ise long veriye dönüştürürüz
            Console.WriteLine("-----------------------------------");
            string stringVeri = "5";
            //int inVeri = int.Parse(stringVeri); // burada Parse işlemi gerçekleşir ama pek kullanımı tercih edilmez genelde Convert metodu uygulanır
            long    longaDonus = Convert.ToInt64(stringVeri);//Long dönüştürme işlemi
            int     inteDonus = Convert.ToInt32(stringVeri);//İnt dönüştürme işlemi
            short   shortaDonus = short.Parse(stringVeri);//Short dönüştürme işlemi
            byte    byteDonus = byte.Parse(stringVeri);//Byte dönüştürme işlemi

            Console.WriteLine(longaDonus);
            Console.WriteLine(inteDonus);
            Console.WriteLine(shortaDonus);
            Console.WriteLine(byteDonus);



            Console.ReadLine();
