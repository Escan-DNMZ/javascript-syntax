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
## Window object

```jsx
//alert
alert(`Merhaba`);

//prompt
var i = prompt(`bir sayı  gir`);

//confirm
var cikis = confirm(`emin misiniz ?`)

//location
window.location.reload(); //bu kod sonrası site kendini sürekli f5 ler
```

## Scope

### Global Scope

```jsx
var name = `Escan`;
// her yerden ulaşılabilir

if(true){
console.log(name)
}
//----------//

for(name == `Escan`){
console.log(name)*5;
}
//----------//
function logName(){
console.log(name);
}
//Hepsinin çıktısı aynı olur  Escan
```

### Local Scope

```jsx
//Fonksiyonlar kendi scope larını oluşturur o değişken sadece fonksiyonda çalışır
function logName(){
var name = `ahmet`;
var age = `12`;
console.log(`function scope `,name,age); //bu kod konsola ismi ve yaşı yazar fakat
}

console.log(`function scope `,name,age); //fonksiyon çıktığı için bu kod çalışmaz

```
## Javascript-Dom

### Tekil element seçimi

```jsx
//document.getElementById()
let val;
val = document.getElementById('header'); //Bu kodla head id li etiketleri 👇
console.log(val); //val değişkeni ile konsola  yazdırdık

val = val.id; //diyerek val değişkenindeki (header ın id sini verir)
val = val.className; //diyerek val değişkenindeki (header ın class ını verir)
val.style.fontsize='45px'; //bu kodla header etiketli yerin fontunu değiştirdik
val.style.color='purple'; //bu kodla header etiketli yerin rengini değiştirdik

val = document.getElementById('header').innerHTML='my  to do app';// 👇
//Bu kodla header daki texti my to do app le değiştirebiliriz

//--------------------------------------------------------------------------//

//document.querySelector()

console.log(document.querySelector('#header')); //Şeklindede kullanılabilir

document.querySelector('li').style.color='red';//bulduğu 1.listeyi kırmızı yapar

document.querySelector('li:nt-child(2)').style.color='red';//2. li yi red yapar
```

### Çoklu element seçimi

```jsx
//document.getElementsByClassName()
let val;                              //class etiketi//ilk elemanı  alır 
val = document.getElementsByClassName('list-group-item')[0];
																			//class etiketi//3. elemanı alır
val = document.getElementsByClassName('list-group-item')[2];

val[1].style.color'blur'; //şeklindede kullanılır 2. elemanı mavi  yapar
val[1].fontSize'25px'; // 2. elemanı 25 px yapar
val[1].textContent='new item'; //2. elemanın yazısını new item  yapar

//Örnek
for(let i=0; i<val.length; i++){
console.log(val[i].style.color='red'); //bütün val ı kırmızı yaptı
}

//document.getElementsByTagName()

val=document.getElementsByTagName('li');//bütün li etiketlerini aldı

//document.querySelectorAll()

val = document.querySelectorAll('li');//burdada li yi verir fakat Nodelist olrak
//buda bize forEach gibi yapıları kullanmamıza  yarar

```
### Dom elementleri üzerinde oynama

```jsx
let val;                            //class
let list = document.querySelector('.list-group');
val = list;
val = list.childNodes; //Nodelist leri bize gösterir
val = list.childNodes[0]; //0 ıncı nodelist i getirir
val = childNodes[0].nodeType; //node un tipini gösterir 3 gibi
val = list.children[0]; //ilk  list-group etiketli li yi gösterir
val = list.children[2].textContent='new item';// textini new item yapar 3. list i
val = list.firstElementChild;//ilk eleman gelir
val = lastElementChild; //son elemanı alır

for(let i=0; i<list.children.length; i++){ //list-group un length i kadar 
if(list.childNodes[i].nodeType===1){
console.log(list.childNodes[i]);
}
}
```

### Element oluşturma

```jsx
//create element
const li = document.createElement('li'); //bir li etiketi oluşturduk
console.log(li)
//add class
li.className='list-group';
//add attribute
li.setAttribute('title','new item');
li.setAttribute('placeholder','sayı giriniz');
//text node
const text = document.createTextNode('new item');
li.appendChild(text); //new  item text bölümüne eklendi
//add link
const a = document.createElement('a');
a.setAttribute('href','#');
a.className='list-item';
```

### element silme

```jsx
const tasklist = document.querySelector('#task-list');
tasklist.remove(); //ul listesi silindi
//belli bir eleman silme
tasklist.childNodes[7].remove(); //8. elemanı sildik
//diğer yolr
tasklist.children[0].remove(); //1. elemanı sildi
//removing attribute
tasklist.children[0].removeAttribute('class');
//örnek
for(let i=0;i<tasklist.children.length;i++){
tasklist.children[i].removeAttribute('class');
}
```

## javascript - events

```jsx
const button = document.querySelector('#btnDeleteAll');
btn.addEventListener('click',function(){
console.log('button clicked');
});
//diğer kullanımı
btn.addEventListener('click',btnClick);

function  btnClick(){
console.log('clicked');
}
//link
btn.addEventListener('click',function(e){
console.log('clicked')
e.preventDefault(); //böylece linkin görevibi yapması yerine clicked yazdı
});

```

### mouse events

```jsx
const btn = document.querySelector('#btnDeleteAll')
const ul = document.querySelector('#task-list');
//click
btn.addEventListener('click',eventHandler);

function. eventHandler(event){
console.log(`event type: ${event.type} `);
}
//çıktı: event type: click

//double click
btn.addEventListener('dbclick',eventHandler);

function eventHandler(event){
	console.log(`event type: ${event.type}`);
}
//çıktı: event type: dbclick
```
### keybord event

```jsx
//keydown,keyup
const input = document.querySelector('#txtTaskName');

input.addEventListener('keydown',eventHandler);

function eventHandler(event){
console.log('event type:' + event.type)
}
//tuşa basdığın an keydown olur çekdiğin zaman keyup olur

//keypress
input.addEventListener('keypress',eventHandler);

function eventHandler(event){
console.log('event type:' + event.type);
}

//focus
input.addEventListener('focus',eventHandler);

function eventHandler(event){
console.log('event type:' + event.type);

event.target.style.backgroundColor='red'; //text tıkladığında arka planı red olur
}

//cut
input.addEventListener('cut',eventHandler);

function eventHandler(event){
console.log('event type:' + event.type);
}
//ctrl x yapıldığında bunu console loga yazar
```


## Javascript kullanıcıya girdi sormak

Javascript kullanıcıya girdi sormak **prompt** kodu ile yapılır

```jsx
var person = prompt("Please enter your name");
alert(person);
```

## Operatörler:

<img width="706" alt="Screen Shot 2021-06-03 at 00 30 32" src="https://user-images.githubusercontent.com/84273839/120554843-ebcd2180-c402-11eb-90fa-5233a7cec33a.png">


<img width="706" alt="Screen Shot 2021-06-03 at 00 30 14" src="https://user-images.githubusercontent.com/84273839/120554801-deb03280-c402-11eb-8370-6066278ebfc7.png">


<img width="706" alt="Screen Shot 2021-06-02 at 23 56 53" src="https://user-images.githubusercontent.com/84273839/120550983-36986a80-c3fe-11eb-9490-6800b1b6e929.png">

<img width="706" alt="Screen Shot 2021-06-02 at 23 57 19" src="https://user-images.githubusercontent.com/84273839/120551044-46b04a00-c3fe-11eb-84dd-f62ec273efd5.png">
