# Javascript

---

kod sonları **( ; )** ile belirtilir, stringler alert veya console.log **( ``,''," )( option+, )** ile belirtilir

Javascript de **{ }** kullanılır.

## Diziler

```jsx
var names = ['Escan','sena','ada','yiğit'];
var years = [2017,1970,1990,1998];

var result = `Benim adım ${names[0]} ve yaşım ${(2020- years[0])}`);
console.log(result); // Benim adım çınar ve yaşım 3
```

### dizi & metodlar.

```jsx
//push()
var cars = ['mazda','opel','toyota'];
cars.push('bmw');  // push metodu değer atamamıza yarıyor.

//unshift()
var cars = ['mazda','opel','toyota'];
cars.unshift('bmw');  // bu metod kodun başına değeri atar

//splice()
var cars = ['mazda','opel','toyota'];
cars.splice(1, 0, 'bmw', 'mercedes'); //splice() metodunun ilk parametresi ekleme yapılacak olan konum, ikinci parametre ise kaç elemanın silinmesidir.Örneğimizde 1.indeks den itibaren hiç bir elemanı silme ve 'bmw', 'mercedes' elemanlarını ekle demiş oluyoruz.

//concat()
var cars1 = ['mazda','opel','toyota'];
var cars2 = ['mercedes','bmw'];

var cars = cars1.concat(cars2); // Bu metod iki diziyi birleştirir ve çıktı 'mazda','opel','toyota','mercedes','bmw' olur

//slice()
var cars = ['mazda','opel','toyota','bmw'];
var yenidizi = cars.slice(2);
console.log(yenidizi);    // bu metod seçtiğin sayıya göre baştan diziden eleman çıkarır.
```

## İF/else/else if Koşulu

```jsx
var a = 1;

var b = 2;

if(a < b){   // Javascript de if koşulu bu şekilde açılır

alert(`a b den küçüktür`);

}

else if (a == b){  // Javascript de else if mantığı bu şekilde 

alert(`a b ye eşittir`);

}

else{   //Javascript de bu kod hiç bir koşul tutmuyorsa işe yarar

alert(`a b den büyüktür`);

}
```

## Javascript  Döngüler

### For döngüsü

```jsx
for (bölüm 1; bölüm 2; bölüm 3) {
  // tekrarlanacak kod bloğu
}

//Örnek

for (var a = 0; a<=10; a++ ){ 
alert(a);
}
```

### For/in döngüsü

```jsx
for (keyin nesne) {
   // çalıştırılacak kod blokları.
}

var user = { username:"Escan", name:"Escan Dönmez", age:25 };
var x;
for (x in user) {
  alert(user[x]);
}
```

### ForEach döngüsü

```jsx
const sayilar = [1, 2, 3];

sayilar.forEach(myFunction);

function myFunction(sayi) {
  alert(sayi);
}

```

### For/of döngüsü

```jsx
for (element of iterable) {
    // kod bloğu
}

//Örnek

const ogrenciler = ['Ali', 'Ahmet', 'Yasemin'];

for ( let ogrenci of ogrenciler ) {
    alert(ogrenci);
}
```

### While döngüsü

```jsx
while (koşul) {
  // çalıştırılacak kodlar.
}

//Örnek

let i = 1;

while (i <= 5) {
    alert(i);
    i += 1;
}
```

## Switch

```jsx
switch(ifade) {
case x:
    // kod bloğu
break;
case y:
    // kod bloğu
break;
default:
    // kod bloğu
}

//Örnek

var kategori = 'beyaz eşya';

switch(kategori){
  case 'telefon':
      console.log('telefon kategorisi');
      break;

  case 'bilgisayar':
      console.log('bilgisayar kategorisi');
      break;   

  default:
     console.log('yanlış kategori');
}
```

## Javascript Fonksiyonlar

```jsx
function fonksiyonAdi(parametre1, parametre2) {
  // fonksiyon kodları
}

//Örnek

function uyari(mesaj) {
  alert(mesaj);
  uyari(mesaj);
}
uyari("Merhaba JavaScript");
```

## Javascript kullanıcıya girdi sormak

Javascript kullanıcıya girdi sormak **prompt** kodu ile yapılır

```jsx
**var person = prompt("Please enter your name");**
alert(person);
```

## Operatörler:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/22a4fcf3-8693-498f-aee0-a08985f9778a/Screen_Shot_2021-06-02_at_22.23.12.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/22a4fcf3-8693-498f-aee0-a08985f9778a/Screen_Shot_2021-06-02_at_22.23.12.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e4d383fe-68b8-4c72-bcee-b6070d8cf792/Screen_Shot_2021-06-02_at_22.23.55.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e4d383fe-68b8-4c72-bcee-b6070d8cf792/Screen_Shot_2021-06-02_at_22.23.55.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5851a69f-8624-4cd4-9b27-a92166aad824/Screen_Shot_2021-06-02_at_22.24.14.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5851a69f-8624-4cd4-9b27-a92166aad824/Screen_Shot_2021-06-02_at_22.24.14.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/60e18d6c-c8d8-4637-8962-fee49c3b1e43/Screen_Shot_2021-06-02_at_22.25.30.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/60e18d6c-c8d8-4637-8962-fee49c3b1e43/Screen_Shot_2021-06-02_at_22.25.30.png)

# Python

---

Kod sonları **( : )** ile yapılır stringler **( "" )** ve **('')** ile belirtilir

Pythonda **{ }** kullanılmaz. Pythonda boşluk önem arz eder

## Fonksiyonlar

```python
def hello():
    print("Merhaba")
hello() #hello yazıldığında merhaba yazacak
```

### Fonksiyona parametre gönderme

```python
defhello(name):
print("Merhaba "+ name)

hello("Escan") # Merhaba Escan
```

## if/elif/else koşulu

```jsx
//Örnek

a = 1

b = 2

if a < b :           // Python da koşul girerken ( ) kullanılmaz.

print("a küçüktür")

elif b == a :        // Python da (else if) mantısı elif ile çalışır

print("a b ile eşittir")

else:               // Değilse anlamına gelir

print("a b den büyüktür")
```

## Python Döngüler

### For döngüsü

```python
sayilar = [1,2,3,4,5]
for sayiin sayilar:
   print(sayi)
```

### While döngüsü

```python
i = 1
while i < 5:
  print(i)
  i += 1
```

## Python kullanıcıya girdi sormak

Pythonda kullanıcıya girdi sormak için **input** kullanılır

```jsx
**isim = input('isminiz: ')** //şeklinde kullanılır
```

## Operatörler:

<img width="706" alt="Screen Shot 2021-06-02 at 23 55 54" src="https://user-images.githubusercontent.com/84273839/120550879-14065180-c3fe-11eb-9f5e-63a5f48e00fb.png">

<img width="706" alt="Screen Shot 2021-06-02 at 23 56 16" src="https://user-images.githubusercontent.com/84273839/120550920-21234080-c3fe-11eb-81bb-b5169a93e48c.png">

<img width="706" alt="Screen Shot 2021-06-02 at 23 56 53" src="https://user-images.githubusercontent.com/84273839/120550983-36986a80-c3fe-11eb-9490-6800b1b6e929.png">

<img width="706" alt="Screen Shot 2021-06-02 at 23 57 19" src="https://user-images.githubusercontent.com/84273839/120551044-46b04a00-c3fe-11eb-84dd-f62ec273efd5.png">
