# h13_Hello_world-


## Ympäristö

Hyper-V kotikoneella (Host):

- CPU: i5-9600K
- RAM: 16Gb
- HDD: 120Gb
- Win 11 Pro x64

Virtuaalikoneen speksit:

- 2 x CPU
- 4 Gb RAM
- 50 Gb HDD
- Generation 2 (Hyper-V pyytää määrittelemään)


## Aloitus 
Tämän kerran tehtävänä oli asentaa kolme eri koodausympäristöä ja luoda niillä Hello World ohjelmisto. Aloitin työt käynnistämällä Debianin virtuaalikoneen 8.3.2023 klo 15:30. Käytin tätä tehtävää varten opettajamme Tero Karvisen artikkelia aiheesta "Hello World Python3, Bash, C, C++, Go, Lua, Ruby, Java – Programming Languages on Ubuntu 18.04", aloitin selaamalla läpi eri vaihtoehdot ja valitsin seuraavat kielet: Python 3, C++ & Ruby. Ennen eri koodikielten asentamista perustin niitä varten oman kansion, johon loin harjoituksien aikana eri kielillä tehdyt ohjelmat. Loin kansion nimeltä "Koodia" ```mattis``` käyttäjän juureen komennolla ```mkdir Koodia```, sekä päivitin repositoriot komennolla ```sudo apt-get update```.


## Python 3
Python ympäristö oli jo entuudestaan koneellani, mutta ajattelin ensin tarkistaa siitä päivitykset komennolla ```sudo apt-get install python3```.
Päivitettävää ei ollut: </br>
![Kuva1](https://user-images.githubusercontent.com/122887740/223729317-280a4b6f-37e7-4071-b735-ff4a273cde06.png)</br>


Oli siis aika siirtyä luomaan Hello World ohjelmisto. Aloitin luomalla tiedoston ```helloworld.py``` Micron avulla ja syötin sinne seuraavan pätkän tekstiä: </br>
```
print(Hello World")
```
Lopulta tallensin tiedoston, ja nyt oli aika ajaa ensimmäistä kertaa kyseinen tiedosto komennolla ```python3 helloworld.py```: </br>
![Kuva2](https://user-images.githubusercontent.com/122887740/223729345-df0c8875-58d2-4872-b777-c25b7b0b1bf8.png)


Ohjelma näytti toimivan oikein. Eli tässä tuli tehtyä Python kielellä toimiva ohjelma, joka printtaa ainoastaan sanat ```Hello World```.


Nyt oli aika siirtyä seuraavan kielen pariin.


## C++
Klo 15:45 </br>
Seuraavana vuorossa oli C++ kielen ympäristö, sitä ei kuitenkaan löytynyt entuudestaan koneelta, vaan se tuli asentaa. Lunttasin hiukan Naman Kukrejan artikkelista "How to install the C++ compiler on Ubuntu", millä komennolla C++ ympäristö asennetaan. Aloitin asennuksen siis komennolla ```sudo apt-get install g++```:</br>
![Kuva3](https://user-images.githubusercontent.com/122887740/223730383-8869cae0-0409-4617-a704-868d0066c723.png)</br>


Asennuksen yhteydessä selvisikin, että koneella on jo C++ compiler, olisikohan kyseessä Debianiin sisään leivotusta komponentista? Joka tapauksessa seuraavaksi oli aika siirtyä luomaan uusi ohjelma C++:lla. Tällä kertaa loin Microlla tiedoston nimeltä ```helloworld.cc``` ja syöttämällä sinne määritteet: </br>
```
#include <iostream>
int main()
{
 std::cout << "Hello World\n";
}
```

Tallennuksen jälkeen tiedosto tuli vielä koota (compile) ja se tehtiin komennolla: ```g++ helloworld.cc -o helloworldcc```, jossa g++ toimii compilerina, helloworld.cc lähdetiedostona, -o parametri osoittaa outputin ja helloworldcc on kohdetiedoston nimi. </br>

![Kuva4](https://user-images.githubusercontent.com/122887740/223731713-74c19c86-f2a6-4e96-b6ca-0dbb435f8e6c.png) </br>
Koonti sujui näemmä ongelmitta. Testaus vielä uupui: </br>

![Kuva5](https://user-images.githubusercontent.com/122887740/223732390-7ef80a06-cf16-4d72-ade8-9dad0d9fbfc6.png)


Tulos oli lupaava, koska ohjelma teki juuri sen mitä sen pitikin, eli tulostaa sanat Hello World.


## Ruby
Klo 16:01 </br>
Lopuksi oli luvassa asentaa ja testata Ruby kielen ympäristö koneelle sekä luoda sillä toimiva ohjelma. Aloitin jälleen harjoitteen tarkistamalla asentamalla itse koodikielen koneelle. Tällä erää apuna oli Rubyn oma dokumentaatio "Installing Ruby" ja sieltä löysin oikean komennon ja se oli: ```sudo apt-get install ruby full``` </br>

![Kuva6](https://user-images.githubusercontent.com/122887740/223733492-5484c787-df50-447c-8a0e-4fc03d18db00.png) </br>

Asennus onnistui mutkitta ja nyt olikin aika siirtyä luomaan ohjelma itse kielellä. Käytin jälleen Microa luomaan tiedoston nimeltä ```helloworld.rb``` ja syöttämällä sinne seuraavat määritteet: </br>
```
print ("Hello Tero\n")
```


Tallennuksen jälkeen oli aika siirtyä vielä testiin komennolla ```ruby helloworld.rb```: </br>
![Kuva7](https://user-images.githubusercontent.com/122887740/223734230-536ec0ea-491a-4c64-9131-4c95bba397ea.png)</br>


Sehän näytti pelittävän niin kuin pitääkin.


## Vapaaehtoinen: greetme.
Klo 16:16 </br>
Valitsin tehtävään Ruby kielen ja aloitin tehtävän luomalla uuden tiedoston nimeltä ```greetme.rb```, sekä syötin sinne seuraavat arvot: </br>
```
print ("Hello" + " " + ENV['USER'] +"\n")
```


- "Hello" = selkokielistä tekstiä
- plusmerkki (+) = aiemman tiedon lisäksi lisättävä
- " " = välilyönti selkokielellä
- ENV['USER'] = tulostaa kirjautuneen käyttäjän nimen
- "\n" = toimii rivinvaihtona


Löysin parametrin ```ENV['USER']``` Ruby Forumilta otsikolla "Get current user logged-in to local computer".


Seuraavaksi oli luvassa testi: </br>
![Kuva8](https://user-images.githubusercontent.com/122887740/223736449-ccef9802-b542-4386-861b-d9ba40f50371.png)</br>

Sehän toimi oikein! En ole kyllä varma haettiinko tätä tarkalleen tehtävänannossa. Mieleeni nimittäin tuli toinen ohjelma, joka kysyisi käyttäjältä nimeä, johon se vastaisi sitten käyttäen syötettyä nimeä Hello "syötetty nimi".



## Lopetus
Tämä harjoitus opetti alkeita Python3, C++ sekä Rubyn maailmaan, harjoitteisiin meni tällä erää noin 1h.

## Lähteet:
Karvinen Tero, 2023 - Linux Palvelimet 2023 alkukevät (https://terokarvinen.com/2023/linux-palvelimet-2023-alkukevat/)

Karvinen Tero, 2018 - Hello World Python3, Bash, C, C++, Go, Lua, Ruby, Java – Programming Languages on Ubuntu 18.04 (https://terokarvinen.com/2018/hello-python3-
bash-c-c-go-lua-ruby-java-programming-languages-on-ubuntu-18-04/)

Naman Kukreja, 25.2.2023 - How to install the C++ compiler on Ubuntu(https://www.codingninjas.com/codestudio/library/how-to-install-the-c-compiler-on-ubuntu)

Ruby - Installing Ruby (https://www.ruby-lang.org/en/documentation/installation/)

Ruby Forum, 7.5.2008 - Get current user logged-in to local computer (https://www.ruby-forum.com/t/get-current-user-logged-in-to-local-computer/136885)
