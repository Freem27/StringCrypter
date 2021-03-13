# StringCrypter

## Библиотека для шифрования\расширофвания строк по ключу

## Использование:
добавить StringCrypter.dll в зависимости Вашего проекта

``` c#
using TDV.StringCrypter;

namespace poligon
{
    class Program
    {
        static void Main(string[] args)
        {
            string data = "строка для шифрования";
            string key = "cryptKey123";

            //шифрование строки
            string encryptedData = StringCrypter.Encrypt(data, key);    //encryptedData="WonfvTD6ZzF8dAPBIlK1N3S2w4EhsTx05uVlMxRjD9ANekc0scKF1sX2PaZo43pYELYHmrIfr7szvKI4z8cm0D7m0fEZPyC+uTbYsU7fXeRrjpeuQRJgcuZWONwbWDbkfaEAnlL5jOTB5itkT4iIBdpGe26ozJvPWU8DpL45Hko="
            //каждый вызов с такими же входными параметрами вернет новую зашифрованную строку:
            encryptedData = StringCrypter.Encrypt(data, key);           //encryptedData="1/SeNNBX2DpsENu+qazQ4bEnL3nU6OKUZ8Joqnug7fxTVKQkrsmpR3gcDqPS37MHMh3FABSAktKh8PUXaIwQa3W2EipeGIs3HwoFoFxLoTIzku8JHUUZ9UpcZ2XsSL1+XccRnwAI3lgntTDck9WKdBIOo50Q1ZYv+fFm+8n6yuc="
            encryptedData = StringCrypter.Encrypt(data, key);           //encryptedData="YkLjJNisaF3Bf88F1C/gDirjPCujyZi0u7D4pxuyknuAN3ZudPDFY6DAv8wcZucnOYbPLhtlhSe/gOdDKfqA+zioFevaXHxLwwwRaQiRoLtqJMFiXKFciT0rzdctmKRmWY1EdbXD9g5DHc00nrIe42xcW5Ioq3rv1HRXxbIFpU0="

            //расшифрование строки
            string decryptedData = StringCrypter.Decrypt(encryptedData, key);  //decryptedData="строка для шифрования"


        }
    }
}
```
