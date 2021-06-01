# Emularea sunetelor produse de corzile unor instrumente muzicale
Modelarea unui/unor instrumente muzicale:corzi de vioara/chitara si/sau notele unui pian, bazate pe algoritmul Karplus-Strong.

## Instalare
Download la patcher-ele de Max din folder-ul Prototipuri si eventual folder-ul cu proiectul final

## Utilizare
Deschiderea patcher-ului, si setarea parametrilor doriti, pentru a obtine un anumite tipuri de sunete: corzi de chitara/vioara de exemplu.

## Istoric

(13.05) Experimentarea cu diferite exemple ale algoritmului Karplus-Strong gasite online, si ajustarea acestora pana la obtinerea unor rezultate(sunete) acceptabile si a unui punct de plecare adecvat.

(3.06) Compunerea automatizata/semi-automatizata a unor piese muzicale, si utilizarea algoritmului modificat pentru a produce o melodie simultan cu compunerea automatizata:
   -Ultima versiune a algoritmului este o combinatie intre Karplus_Strong_4, cel cu multichannel, si Karplus_Strong_3, cel care foloseste 3 corzi simultane ca un sub-patcher;
   -Controlul manual, de la tastatura al kslider-ului pentru Karplus_Strong_4 folosing obiectul key, dar reorganizand clapele (codul ASCII) in functie de tastatura;
   -Posibilitatea de schimbare a tipurilor de sunete din Karplus_Strong_4: noise~, pink~, tri~, saw~, cycle~, rect~, si combinatii intre ultimele 4 tipuri de sunete, astfel
   obtinand combinatii de sunete asemanatoare clapelor de pian.
   -Schimbarea anumitor valori din obiectul preset utilizand OSC din aplicatia oschook: mai exact, diferite valori pentru luminozitate;
   -Controlul/Compunerea diferitor tipuri de melodii in Karplus_Strong_3 folosind oschook: o combinatie intre parametrii de la accelerometru si a celor de la orientate, dar si
   schimbarea timpului in care sunt primite mesajele tip OSC pentru a obtine variatii de sunete controlate prin obiecte tip switch;
   -Modificarea track-urilor auxiliare pentru a putea fi utilizate simultan cu obiectul key modificat: ca un fel de "live performance";
   

(X.06)  Modificari finale/imbunatatiri/ajustari; 
        Creearea unei interfete user friendly in Presentation Mode.

## Link-uri
https://www.youtube.com/watch?v=5RYy8Cvgkqk

https://www.youtube.com/watch?v=Cc1-Rq0nSVo&t=182s

https://www.youtube.com/watch?v=Yb8JuFHJxQQ   

https://www.youtube.com/watch?v=ieLUTwfkkU4 	(part 1) 

https://www.youtube.com/watch?v=Z_aLgR3n05A	(part 2)

https://www.youtube.com/watch?v=eiewFZ8OVow  (part 1) 

https://www.youtube.com/watch?v=REigfEsfNxw	(part 2) 

https://www.youtube.com/watch?v=zCx_7lum-DU

# Dezvoltarea proiectului

Pentru început:

1. Creează-ți cont pe Github
2. Download și install [Github Desktop](https://desktop.github.com/)
3. Citește [acest ghid](https://charlesmartin.com.au/blog/2020/08/09/student-project-repository) și ține la îndemână [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet).

Apoi, procesul este următorul (inspirat de [aici](https://cs.anu.edu.au/courses/comp1720/deliverables/05-major-project/#submission-process)):

1. *fork* al acestui template către propriul tău cont de Github

![](assets/fork.gif)

_(dacă preferi cumva ca repo-ul să nu fie vizibil de către public, îl poți seta ca Private din Settings - "Change visibility". Atunci trebuie să mă adaugi drept colaborator, ca eu să am acces.)_

2. *clone* al repo-ului din Github Desktop pentru a-l downloada local

![](assets/clone.gif)

3. *commit* și *push* pe măsură ce lucrezi la proiect. Ultima versiune push-ată pe server înainte de deadline va conta pentru evaluare.

![](assets/commit.gif)

## Elemente obligatorii

1. Acest readme completat. Titlu, descriere, mod de utilizare, istoric, link-uri utile.

   Poți include și imagini și chiar [gif-uri animate](https://www.screentogif.com/), sau link-uri către materiale audio/video.
   
   Vezi [aici](https://charlesmartin.com.au/blog/2020/08/09/student-project-repository) mai multe sugestii.

2. [Declarația de originalitate](statement-of-originality.yml) completată. Tot ce nu este inclus acolo va fi considerat 100% contribuție proprie.

    *(formatul este adaptat de [aici](https://gitlab.cecs.anu.edu.au/comp1720/2018/comp1720-2018-major-project/-/blob/master/statement-of-originality.yml). Da, este un pic ironic să refolosim un doc [de altundeva](https://cs.anu.edu.au/courses/comp1720/resources/faq/#how-do-i-fill-out-my-statement-of-originality), dar menționăm sursa deci nu este plagiat!)*

3. Proiectul în sine. Tot codul trebuie să fie prezent, proiectul trebuie să poată rula conform instrucțiunilor din readme. Dacă e nevoie de asset-uri mari (sunete, video etc), [folosește Git LFS](https://git-lfs.github.com/) sau include link de download în instrucțiunile de instalare.

