# All Python Notes

---

# 1.Kısım ➕

---

## General Information :

**Information of : `Shift + Tab`  &  Type of x : `type(x)`** 

**`help(benimAdim.upper)` : info about func.**

---

## String :

**String to integer : `x = int(String)`**

**String input : `input(”İsim Giriniz ”)`** 

**Split : `name.split()`** 

**Sep+maxsplit :** `**name.split(sep=" " , maxsplit=2)`** 

**Slicing : `[ : 10 ]`** 

**Step Size : two by two : `name[: : 2]`** 

**all to upper : `name.upper()`**  

**all to lower : `name.lower()`**

**to check all is lower or upper : `name.islower()`**  

**first letters are upper  : `name.title()`**

**only first letter is upper : `name.capitalize()`**

**how many letters : `len( k )`**

**replace one to another : `s.replace(”eski”,”yeni”)`**

**to find substring location index in string :** 

**`s = "KALEM"
 s.find("LE")`  —> 2**

### **Split( ) , String to List :**

**`s = "merhaba nasılsın ?"
 s.split(" ")` —> ['merhaba', 'nasılsın', '?']** 

### Join( ) , List to String :

`**l = ['limon', 'portakal', 'elma']
 ",".join(l)` —> “limon,portakal,elma”**

### to drop the spaces :

**only drop from left : `str.lstrip()`**

**only drop from rigt : `str.rstrip()`**

**drop both : `str.strip()`**

---

**Bir str, int veya list içinde var mı yok mu kontrolü için`in`**

```python
**if “kalem” in mystr :
   print(”varmış”)
else:
   print(”yokmuş”)
###
if “top” in myDic.keys(): Dict için** 
```

---

**For loop örnek** : **Koordinat listesi , for döngüsü ile x , y elemanlarını veya sadece x yazdırma :**

```python
**koorlist = [(2,5) , (6,9) , (3,8)]
for (x,y) in koorlist:
	print((x,y)) 
	print(x)**
```

**Dict içindeki verileri sıralamak, for ile x, y elemanlarını yazdırmak & x yazdırmak için :**

```python
**myDick = {”muz”:150 , “kiraz”:200}
for (anahtar,deger) in myDict:
print((anahtar,deger)) 
print(anahtar)**
```

---

### **Continue, Break, Pass : Döngüler anahtar kelimeler :**

**Döngüyü durdur, bitir : `break`**

**Döngüyü sonlandırmak yerine o kısmı geçerek döngünün en üstüne geri atlar : `continue`**

**Döngünün içine henüz bir şey yapmaycaksak işlem yapılamacak hata alınmasın daha karar vermedim diyorsan pass geçebiliyon : `pass`** 

---

### **While döngüsü : Sozsuz tekrar eden döngüler**

**Örnek : x için ‘0 dan 10 ‘a kadar döngüde yazdıracak +1 ekleyip devam edecek. :**

```python
**x=0
while x < 10 :
   print(x)
   x=x+1** 
```

---

### **If-else mantığında `Assert`kullanımı :**

**Varsıyım yapar bir koşulu, yanlış ise hata mesajını veya belirttiğimiz mesajı verir. Uzun süreçli projelerde hataları hızlıca ayıklayabilmek için kullanımı pratik olabilir.** 

```python
**def fonksiyon(liste):
	for i in liste:
		try:
			assert i <= 3 #İddianın-doğru-olduğu-aralık
			print(i)
		except AssertionError:
			print("{} sayısı 3'den büyük".format(i))
liste = [1, 2, 3, 4, 5, 6]
fonksiyon(liste)**
```

---

### Format : —>

```python
**num = [4, 5, 6]
p ="Nums:{0}{1}{2}".format(num[0],num[1],num[2])  
## print: Nums: 4 5 6
#Format içinde sayı yerine str de kullanılabilir 
a = "{x}, {y}".format(x=5, y=12)**
```

---

**Kapsam : scope : Komutları kapsamlara göre sıralar. 
Local, Enclosing, Global, Built-In : İçten >> Dışa doğru** :

```python
**benimAdım = “hoca”
#Global
def benimFonksiyonum():
      benimAdım = “ali”
      #Enclosing
      def icFonksiyon():
				benimAdım = “fatih”
	      #local
	      print(benimAdım)
		 icFonksiyon()**
```

**Daha sonra `benimFonksiyonum()` çağırırsak içindeki `print(benimAdım)` ı en içten tek tek kontrol ederek öncelikte onu yazdırır.** 

---

- **Useful Functions : Özel Fonksiyonlar**
    
    ![Untitled](All%20Python%202e705/Untitled.png)
    

---

### Python Hata Mesajları, İstisnalar, Exceptions, Yaygın istisnalar:

**ImportError: içe aktarma başarısız;**

**IndexError: bir liste, aralık dışı bir sayıyla endekslenir;**

**NameError: bilinmeyen bir değişken kullanılıyor;**

**SyntaxError: kod düzgün bir şekilde ayrıştırılamıyor;**

**TypeError: uygun olmayan türden bir değerde bir işlev çağrılır;**

**ValueError: Doğru türde bir değerde, ancak uygun olmayan bir değerde bir işlev çağrılır.**

**Python'un ZeroDivisionError ve OSError gibi birkaç yerleşik istisnası daha vardır. 
Üçüncü taraf kitaplıkları da genellikle kendi istisnalarını tanımlar.**

- Exceptions : (**english**)
    
    Different exceptions are raised for different reasons. Common exceptions:
    **ImportError:** an import fails;
    **IndexError:** a list is indexed with an out-of-range number;
    **NameError:** an unknown variable is used;
    **SyntaxError:** the code can't be parsed properly;
    **TypeError:** a function is called on a value of an inappropriate type;
    **ValueError:** a function is called on a value of the correct type, but with an inappropriate value.
    Python has several other built-in exceptions, such as **ZeroDivisionError and OSError**. 
    Third-party libraries also often define their own exceptions.
    

---

### Hataları Ele Alma : try: except:

```python
**while true
   try:
  .....
   except: 
  ...... print(”işlemi doğru yapınız..”)** 
```

**Burada while döngüsü içindeki işlemleri sonsuz döngüde devam ettir. İstenilen değerler verilmiş ise hata yok ise kontrol et, “try” içinde dene; eğer hata var ise “except” içindeki mesajı veya işlemi yazdır.**

---

### Hataları İşleme : Exception Handling

- **Exception Handling : Hataları işleme :**
    
    **To handle exceptions, and to call code when an exception occurs,
    you can use a try/except statement.**
    
    **The try block contains code that might throw an exception.**
    
    **If that exception occurs, the code in the try block stops being executed, and the code in the except block is run.**
    
    **If no error occurs, the code in the except block doesn't run.**
    
    ![Untitled](All%20Python%202e705/Untitled%201.png)
    
    ---
    
    ### Hangi hata olursa olsun kodu çalıştırmak için, `finally:` —>
    
    ![Untitled](All%20Python%202e705/Untitled%202.png)
    
    ---
    
    ### Raising Exception :  `raise Error` : hatayı özel olarak belirtebilirsin :
    
    ![Untitled](All%20Python%202e705/Untitled%203.png)
    
    ### try , except ‘den sonra `raise` tek yazılırsa hatayı sistem otomatik yazar.
    
    ---
    

---

### Sorted( [.. for .. in ..] ,reverse=T/F ) Sorted ascending or descending

<aside>
💡 n = int(input())   # integer input like 394617
s = sorted ( [i for i in str(n) ], reverse=True)   ## int to str list and descending sorted
int("".join(s))   ### finally convert str list back to int

</aside>

- **Links +**
    - [https://docs.python.org/3/howto/sorting.html](https://docs.python.org/3/howto/sorting.html)
    - [https://www.w3schools.com/python/ref_func_sorted.asp](https://www.w3schools.com/python/ref_func_sorted.asp)
    - [https://www.programiz.com/python-programming/methods/built-in/sorted](https://www.programiz.com/python-programming/methods/built-in/sorted)
    - [https://www.geeksforgeeks.org/sorted-function-python/](https://www.geeksforgeeks.org/sorted-function-python/)
    - [https://www.afternerd.com/blog/python-sort-list/#:~:text=If you want to sort,They both accept it](https://www.afternerd.com/blog/python-sort-list/#:~:text=If%20you%20want%20to%20sort,They%20both%20accept%20it)!
    

---

- **Is list, isinsatance ?**
    - [https://github.com/cihanayindi/Patika.dev-Python101-FinalProject/blob/main/Tasks/main.py](https://github.com/cihanayindi/Patika.dev-Python101-FinalProject/blob/main/Tasks/main.py)
    - [https://github.com/BarisCemSahin/Patika.dev-Python-101-Final-Project/blob/main/Tasks](https://github.com/BarisCemSahin/Patika.dev-Python-101-Final-Project/blob/main/Tasks)
    - [https://github.com/alixuzun/Bitime-projesi/blob/main/python-proje](https://github.com/alixuzun/Bitime-projesi/blob/main/python-proje)
    - [https://github.com/mehmetumutmutlu/patika/blob/main/1-python-temel.ipynb](https://github.com/mehmetumutmutlu/patika/blob/main/1-python-temel.ipynb)
    - [https://www.getgnu.org/gnulinux/gnulinux-ipuclari/20-examples-for-flattening-lists-in-python.html](https://www.getgnu.org/gnulinux/gnulinux-ipuclari/20-examples-for-flattening-lists-in-python.html)

# 2.Kısım ➕

---

## **Python All String Methods** 🔗 **[here!](https://www.programiz.com/python-programming/methods/string#:~:text=A)**

## **math Modülü (yazbel.com)** 🔗 [here!](https://python-istihza.yazbel.com/standart_moduller/math.html)

## math Kütüphanesi (medium.com) 🔗 [here!](https://medium.com/software-development-turkey/python-math-k%C3%BCt%C3%BCphanesi%CC%87-ve-kullanimi-60ab7f19924b)

## Python math functions 🔗 [here!](https://docs.python.org/3/library/math.html)

### **Özel Metodlar : “special methods in Python”**

---

## Ma1th Operations :

**Exponential : x^2 : `x ** 2`** 

**Quotient : `print( 20 // 3 )` : as 6** 

**Remainder : `10 % 3` : as 1**

---

## List :

**String & list : immutability & mutable !!** 

**A list : `mylist = [0, 2, 5]`**  

**Empty list : `bosList = list( )` veya `boslist = []`**

**to drop last value : `mylist.pop ()`** 

**to delete value : `mylist.remove(40)`**

**to change index 0 as 8 : `mylist[0] = 8`**  

**to reverse list : `mylist.reverse ()`** 

**A nestedList : `nestedList = [2,“top”, [5, “at”] ]`**

**to add into list : `mylist.append(50)`**

**to add into specific index : `list.insert(5,”is”)`**  

**number of value, how many : `mylist.count (20)`**  

**sum of all value in int list : `sum(listem)`**

**to find averafe of int list : `sum(listem) / len(listem)`**

**to identfy max num of list : `max(bakılanlist, key=len)`**

---

## Dictionary

**{ “Key” : Value } : `mydt = {”elma” : 100, “kiraz” : 200}`**

**print(“Key”) —> Value : `print(mydt["elma"])` —> 100**

**.get(”elma”) —> Value : `mydt.get("elma")` —> 100**

**using .get(”..”) parameter, if the value isn’t in dict, 
the program writes : `None` or your message :
`print(ages.get("ali"))` —> `None`
`print(ages.get(680 ,"not in dictionary"))`  —> ...**

**to show keys or values : `dict.values( )`&`dict.keys( )`** 

**Empty dict : `bosDict = dict( )`  & `bosDict = { }`**

**to add into dict : `bosDic[”key”]=123`**

**to show items in dict as `(’muz’, 150)` : `myDick.items()`**

---

## Set

**Set : `myset = {“a”,“s”}` `num_set = {1,2,3,4,5}
word_set = set(["spam","egg","sausage"])`**

**Empty set : `bosSet = set( )`**

**to add into set : `bosset.add(50)` not `append` !!** 

**to convert from list to set : `listemSet = set (listem)`**

**Set in listeden farkı içerisinde tekrar eden elemanları sadece 1 defa gösterir. !!! 
Üyelik kontrolü, testi ve tekrarlanan girişleri elemek için kullanılabilir. Set ile kontrol etmek daha hızlıdır. !!**

**Set için index mantığı yoktur. Bu yüzden eleman değişimi de yapılamaz. !!!**

**print(first | second)  —> both set values
print(first & second)  —> common values  
print(first - second)  —> only first values
print(second - first)  —> only second values
print(first ^ second)  —> non-common values**

**Parantez içinde set ile yazılan stringin her bir harfi karakter olarak set kümesine kaydedilir.** 

**`s = set("deneme")`  —> {'d', 'e', 'm', 'n'}**

---

## Tuple

**Tuple : normal parantez veya parantez olmadan oluşturulabilir : Index mantığı vardır, ama Listedeki gibi ELEMAN DEĞİŞTİRME Tuple da yoktur !!!**  

`**myTuple = (1, 2, 5, “s”)`
`mytup = "one" , "two" , "three”`**

**Tuples listelerden hızlıdır. Ama index değiştirilemez!**

**Tuple Unpacking ile tuple içindeki öğeleri değişkenlere atayabiliriz:**

**`numbers = (1,2,3,4,5)
a, *b, c = numbers   
## *b olunca sağından sonraki değere kadar hepsini al.
print(a,b,c)` —> 1 [2, 3, 4] 5**

---

## Functions ..

```python
def yenifonksiyon() :
	print(”yeni fonksiyon oluştu.”)   
def toplama(num1, num2):
	return num1+num2   
```

**Functional Programming : Higher-Order Functions :**

**Bir diğer fonksiyonu argüman olarak almak veya sonuç olarak döndürmek.**

```python
**def apply_twice(func, arg):
	return func(func(arg))

def add_five(x):
	return x+5

print(apply_twice(add_five,10))**
```

**İç içe Fonksiyonlarda argümanın uygulanacağı fonksiyon için lambda kalıbı kullanılabilir :**

```python
**def my_func(f, arg):
	return f(arg)

my_func( lambda x: 2*x*x, 5)**
```

---

### Recursion : Kendi kendini tekrarlayan fonksiyonlar, Adım adım çözmek için :

```python
**def factorial(x):
   if x==1:
      return 1
   else:
      return x * factorial(x-1)
factorial(5)**
```

---

**Args : argümanlar : değişken sayısını args ile kullanıcıya bırakmış oluruz, istediğimiz kadar girdi alabiliriz :**

```python
**def yeniToplam(*args):
   return sum(args)

yeniToplam(10,20,30..)**
```

**Kvargs, keywordargümanlar : args ile aynı mantık 
ama ** kullanılır dict çevirir :** 

```python
**def yeniFonksiyon(**kvargs):
   return(kvargs)
yeniFonksiyon(muz=100, elma=200)**
```

---

**map func. apply list to any sums** 

`**list(map(bolmeİslemi, yeniListem))**` 

**filter func. same as map and also filter :**

`**list( filter( kontrolFonksiyon, stringList ))`** 

**map String için başka bir örnek : 
listedeki stringlerde “a” var mı kontrol eder :**

```python
**stringListesi= ["atıl","hoca","fatih","ali" ]
def kontrolFonksiyonu(string):
	return "a" in string
list(map(kontrolFonksiyonu,stringListesi))**
```

**Anonymous : Lambda fonksiyonu : Teksatırda hızlıca matematiksel işlemler yapabilmek için :** 

```python
**carpma = lambda numara : numara*3
carpma(10) ## --> 10*3 : 30** 
```

**map fonksiyonu ile birinci kısımdaki fonksiyona ikinci kısımdaki sayıları uygulamak :** 

```python
**listem=[2,5,8]
list(map(lambda numara : numara*5 , listem))**
```

---

### Sınıf : Class : instance & attribute : Özellik

```python
**class ArabaMarkalari():
def __init__(self,ismi,yasi):
print("class oluşturuldu.")
## Self’den sonra 1.kısım attribute yani özelliği temsil eder.2.kısım ise değişkeni temsil eder. 
self.ismi = ismi
self.yasi = yasi**
```

**Metodlar : sınıf içerisinde istediğimiz kadar metod oluşturabiliriz :** 

**Mesela yeniMetod ile yeni eklentiler yapabilir, burada “self” yardımıyla bir önceki metodtan değişkenleri kullanabiliyoruz. Self olmazsa kod çöker :**

```python
**def yeniMetod(self):
print(f"yerli ve milli araba: {self.ismi}")**
```

**Metodta belirlediğimiz değişkene sabit bir değer de atayabilir, daha sonra çağrılırken değer girmezsek bu değeri yazdırabiliriz :**

```python
**class Kus():
   def __init__(self,yas=3):
   self.yas = yas**
```

---

### **inheritance : kalıtım almak, miras almak. : bir sınıfın özelliklerini miras almak. Örneğin bir ana küme var, bir de sonradan oluşturulan bir küme var.**

```python
**class Hayvan():
def init(self):
    print("hayvanlar alemi oluştu")
def yetenek1(self):
    print("1.yetenek yüklendi")
## Superclass   &&  ## Subclass
Yeni bir kedi sınıfı oluşturulur ama hayvan sınıfından kalıtım alınır —>
class kedi(Hayvan):
            def init(self):
                print("kedi sınıfı oluştu")
                Hayvan.yetenek1(self)**
```

**override : ayrıca kedi sınıfında üstüne yazma da yaptırabiliriz, 
yani hayvan sınıfındaki aynı özelliği burada özelleştirebiliriz.** 

**polymorphism : farklı sınıflardaki aynı isimdeki metodların farklı amaçlara hizmet etmesi, işlevi görmesi.** 

**Subclass ‘da Superclass ‘dan bir çağrı yapmak için `super()` kalıbı :** 

```python
**super().spam() calls the spam method of the superclass.**
```

---

# Tricky ➕ New

---

**Print without new line : `print(”Merhaba” , end="")`**

**Print without space :** 

`**print(*range(0,5))`  —>  0 1 2 3 4
`print(*range(0,5), sep="")` —> 012345
`print(*range(0,3), sep="+")` —>  0+1+2
`print("Ali","can", sep=" ")` —> Ali can**

**to control num of digits : 4.333333333  : such as float 2 digit :**

`**print('%.2f' % avrg)`  —> 4.33** 

### **Using map func. with `spit()` able to create int list :**

`**arr = map(int, input().split())
 print(list(arr))**`

## Special Methods

```python
**list(range(5))  ## 0 to 5 : [0, 1, 2, 3, 4]** 
```

```python
**list(range(2,10,3))  ## 2 to 10 with 3 by 3**
```

**enumerate : a shortcut to this code :**

```python
**index = 0
for numara in list(range(5,15)):
print( f “güncel numara: {numara} güncel index: {index}”)
index = index +1
## --> “güncel numara: 5 güncel index: 0 “ :** 
```

```python
**for eleman in enumerate(list(range(5,8))):
     print(eleman) 
## --> (0,5) (1,6) --> 0. index, no 5** 
```

**to show index and num with for loop :**

`**for (index, numara) in .... 
     print(index)**` 

**a random int and suffle to list :**

```python
**from random import randint 
randint(0,10)   #a random int between 0-10
from random import shuffle 
shuffle(listem)** 
```

**zip : concat to lists : like : (muz,100,salı) :**

```python
**yemeklist = [ ... ] \ 
kalorilist = [ ... ]  \ 
günlist = [ ... ] 
list( zip(yemeklist, kalorilist, günlist) )** 
```

---

### İleri seviye liste özelliği : `**[..for..in..]`**

```python
**bosliste = [ ] 
birstring = “fatihhoca”
   for harf in birstring:
      bosliste.append(harf)
## shortcut to this cut is :
yenilis = [ eleman for eleman in birstring ] 
numlist = [ num*5 for num in list(range(0,5))]** 
```

---

**to control character as string, num, ..** 

```python
**k = input()
k.isalpha()
liste.isalnum() #num and char
list.isnumeric()  &  dene.isdigit() #num, digit**

```

---

### A list comprehension :

```python
**mylist = [ i*i for i in range(3) ]  # [0, 1, 4]

#Özelolarak for’un yanına if şartıda eklenebilr:
mylist = [ i*3 for i in range(9) if i%2==0 ]  
# —> [0, 6, 12, 18, 24]**
```

**Çok geniş aralıklı liste oluşturma MemoryError verebilir.** 

---

**for’dan `if - else` eklersek, anlamı şu olur : 
Eğer `if` durumu ise yazdır, `else` ise -1 yazdır. :** 

```python
**print( weird_squares = [e  if e % 2 == 0 else -1 for e in squares] )
## [-1, 4, -1, 16, -1, 36, -1, 64, -1, 100]**  
```

**Aynı durum için eğer for’dan sonra `if` şartı var ise baştaki `condition` kısımlarına bakılmaz. :**

```python
**ultra_weird_squares = [e if e % 2 == 0 else -1 for e in squares if is_even(e)]
## [4, 16, 36, 64, 100] <<< -1 ler yazdırılmaz yani , o kısım kontrol edilmediği için** 
```

### Nested List Comprehension :

```python
**[ [i for i in range(4)] for _ in range(6)]
### 
[[0, 1, 2, 3],
[0, 1, 2, 3],
[0, 1, 2, 3],
[0, 1, 2, 3],
[0, 1, 2, 3],
[0, 1, 2, 3]]**
```

---

**Shortcut with comprehension :**

```python
**my1 = [[10,12,16],[20,30],[18]]      my2 = []

for a in my1:
   print(a)
[10, 12, 16]
[20, 30]
[18]

for a in my1:
   print(a)
   for b in a:
      print(b)
      my2.append(b)
print(my2)
## [10, 12, 16, 20, 30, 18]   <<< m2
## shortcut this code
[ b for a in my1 for b in a]
## [10, 12, 16, 20, 30, 18]   <<<**
```

---

**Daha fazla argüman ile iç içe listeler de oluşturulabilir :**

```python
**mf=[[a,b]for a in range(0,3)for b in range(2,3)] ## —>[[0, 2], [1, 2], [2, 2]]**
```

**Belli sayıda input çağırmak için kısayol : DRY**

```python
x, y, z, n = (int(input()) for _ in range(4))
### Uzun hali —>
x, y, z, n = int(input()), int(input()), 
int(input()), int(input())
```

---

### **Özel metodlar :**

**Örneğin bir Meyve sınıfından tanımlanmış bir Elma objesini : Print edersek sadece onunla ilgili sistem bilgisi verilecektir.  Aynı şekilde “len(elma)” şeklinde çağırınca da hata verecektir. Bunun için class içinde özel fonksiyonu tanımlayabiliriz :** 

```python
**def __str__(self):
return f”{self.isim} meyvesi şu kadar kaloriye sahiptir: {self.kalori}”**
```

---

```python
**def __len__(self):
return self.kalori 
Şeklinde class içinde fonksiyonlar tanımlanabilir.** 
```

---

### **Magic Methods : Bazı özel, sihirli metodlar :**

```python
**class Vector2D:
def __init__(self, x, y):
self.x = x
self.y = y
def __add__(self, other):
return Vector2D(self.x + other.x, self.y + other.y)
first = Vector2D(5, 7)
second = Vector2D(3, 9)
result = first + second
print(result.x ,“and”, result.y)**
```

**Magic methods for common operators:** 

**...**

**Karşılaştırma için Magic Metod :** 

**...**

**Magic methods for making classes :**

...