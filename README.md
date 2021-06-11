# Emularea sunetelor produse de corzile unor instrumente muzicale
Modelarea unui/unor instrumente muzicale:corzi de vioara/chitara si/sau notele unui pian, bazate pe algoritmul Karplus-Strong.

## Instalare
Download la patcher-ele de Max din folder-ul Prototipuri si eventual folder-ul cu proiectul final
Download la folder-ul Proiect Karplus-Strong Final ce contine proiectul integrat in Ableton Live 10 si patcher-ele Max in format .amxd

## Utilizare
Deschiderea proiectului Max Karplus-Strong project.als , si setarea parametrilor doriti, pentru a obtine un anumite tipuri de sunete: corzi de chitara/vioara de exemplu.

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
   

(12.06)  Modificari finale/imbunatatiri/ajustari: 
        -Creearea unei interfete user friendly in Presentation Mode.
        -Integrarea algoritmului in Ableton Live 10 cu ajutorul a 2 track-uri de tip MIDI pe care sunt atasate cate un Max MIDI Effect. Fiecare effect preia un anumit tip de  
        Instrument MIDI specific pentru Live 10 in care am compus un anumit track MIDI, iar cele 2 MIDI Effects trimit numarul notei MIDI si Velocity-ul in kslider-ul din
        programul principal(In cazul track-ului cu rosu) si in kslider-ul pentru Karplus-Guitar(In cazul track-ului verde).
        Astfel, notele MIDI generate in Live 10 sunt generate si de kslider-ele specifice celor doua tipuri de algoritm Karplus-Strong.
        -Switch-ul ON/OFF pentru notele si vitezele MIDI primite din Live 10 se face cu ajutorul butoanelor/mesajelor 1 si 2 respective in interfata grafica pentru fiecare 
        algoritm in parte, dar pentru a fi oprit in totalitate, trebuie dat mute pe pe track-ul respectiv in Live 10.
        -Range-ul pentru mesajele tip OSC a fost schimbat ca sa nu se suprapuna prea mult pentru senzorul de lumina: 50-55; 100-110; 300-320
        -Adaugarea a 4 switch-uri pentru controlul ON/OFF al mesajelor tip OSC din oschook v2, si mai ales controlul timpului in care sunt primite mesajele din obiectele
        de tip speedlim.
        

## Link-uri 
https://www.youtube.com/watch?v=5RYy8Cvgkqk

https://www.youtube.com/watch?v=Cc1-Rq0nSVo&t=182s

https://www.youtube.com/watch?v=Yb8JuFHJxQQ   

https://www.youtube.com/watch?v=ieLUTwfkkU4 	(part 1) 

https://www.youtube.com/watch?v=Z_aLgR3n05A	(part 2)

https://www.youtube.com/watch?v=eiewFZ8OVow  (part 1) 

https://www.youtube.com/watch?v=REigfEsfNxw	(part 2) 

https://www.youtube.com/watch?v=zCx_7lum-DU

https://www.youtube.com/watch?v=gLEHeA2NX8Q&ab_channel=TheProducer%27sKitchen 	CONTROL CU MIDI

https://docs.cycling74.com/max5/vignettes/core/live_midieffects.html		CONTROL CU MIDI

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

