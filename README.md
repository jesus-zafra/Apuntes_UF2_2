# Apunts M5: UF2-2 - Optimització i Documentació
![jpg portada-optimitzacio](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_2/main/GoodCodePractice.jpg)
***
# Optimització
Optimitzar una aplicació consisteix en millorar el rendiment d'aquest, ja sigui en termes de velocitat d'execució dels seus diferents mètodes, fer que faci el mateix utilitzant menys recursos del sistema (això inclou que ocupi menys mida al suport físic on està instal·lada) entre qualsevol altre factor que impliqui una millora de rendiment.  

A més, quan optimitzem un codi font s'han de tenir en compte també no només aspectes purament funcionals en quant a la millora del rendiment, sinó que també tindrem en compte factors com la llegibilitat per exemple. 

Les millores d'una optimització no només afecten al codi, podem fer millores que afectin l'**estructura de les dades**, la **lògica dels processos**, o que afectin directament a les parts de les seves **interfícies**.
***
# Pudor del codi
![jpg code-smell](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_2/main/code-smell.jpeg)  

 La *"pudor del codi"*, o code smell en anglès es un concepte de programació que fa referència a tot aquell codi que si bé és correcte, a la llarga ens pot donar molts problemes endarrerint el desenvolupament de projecte.  
  
Alguns dels típics casos on el codi fan pudor i s'ha d'optimitzar:  
- **Mètodes o atributs amb noms no significatius**  
  És més sencill de seguir un codi on es veu clarament cada cosa a que fa referència. Especialment quant pasa molt de temps i s'ha de revisar el codi, i quant es treballa en equip.
- **Varis mètodes fent la mateixa tasca**  
  Hem d'evitar la repetició de codi, o fer la mateixa tasca amb codi semblant. Quan això succeeix es millor escriure un mètode genèric i que s'invoqui segons diferents necessitats amb diferents arguments.  
- **Mètodes amb més paràmetres dels necessaris**  
  Es molt important que cada mètode faci una tasca molt concreta. Si un mètode necessita molts arguments per funcionar sol ser síntoma de que potser no estem modularitzant correctament la tasca que aquest ha de resoldre.
- **Codi innecesari**  
  El codi que fa cap aportació a la funcionalitat s'ha d'eliminar. Només fa que despistar-nos i fer més confús l'enteniment de l'algoritme que usa, a més de emportar-se temps de processament i capacitat de recursos.
- **Ús de nombres o valors màgics en expresions**  
  Usar constants directament en lloc d'utilitzar un nom de constant. S'ha d'evitar utilitzar aquests "números màgics" de tal manera que sigui fàcil d'entendre d'on venen els càlculs a les diferents expressions del codi.  
***  

# Anàlisi del Codi  
Un codi es pot analitzar de forma estàtica o dinàmica:  
- **Anàlisi estàtic**
  - Es fan sense executar el codi.  
  - S'utilitzant analitzadors estàtics anomenats linters, o també utilitzant llocs web (p. ex. validadors HTML, XML, etc.). 
  - Alguns analitzadors estàtics de codi: lint (C), sonar (Java), JSLint, ESLint(Javascript).  
- **Anàlisi dinàmic**  
  - Es fan executant el codi.  
  - Majorment s'utilitzen programes coneguts com depuradors (debuggers en anglès).  
***

# Refactorització   
Refactoritzar un codi consisteix en alterar la seva estructura sense que això modifiqui el seu comportament.
Es pot refactoritzar de diverses maneres:
- Reanomenant variables  
- Eliminant codi que mai serà executat  
- Eliminant codi redundant  
- Eliminant codi mort o inútil.  
etc.  

Fent aquestes refactoritzacions aconseguirem optimitzar el codi fent-lo més mantenible i/o augmentant el seu rendiment.  

# Documentació  
Una part important en el procés de desenvolupament és la documentació. Cal deixar documentat tot allò que pensem que algú altre o nosaltres mateixos al cap del temps puguessim tenir dificultats per entendre-ho.
  Es pot documentar amb diferents formats: **HTML** (p.ex. *javadoc*), **Markdown** (p.ex.GitHub), **reStructuredText** (p.ex. *Readthedocs*), *asciiDoc*...  
Hi ha tres tipus de documentació:  
1. **Documentació del codi**  
  Consisteix en documentar els mètodes i atributs de les nostres classes explicant què són, les seves funcions, formes d'ús, etc. 
2. **Documentació tècnica**  
  És tota aquella documentació que va dirigida a usuaris especialitzats per d'usar l'aplicació.
3. **Documentació de l'usuari**  
  És la informació que rebrà l'usuari normal que usarà el programa, on s'explica tot el que ha se conèixer per aprofitar totes les funcionalitats.

# Control de versions
![jpg eines-control-versions](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_2/main/git-sites.png)
Una aplicació, conforme va avançant el temps, a través de diferents revisions pot arrivar a no ser compatible amb alguns dels seus estats anteriors, el que es coneix com a versió. Per això és molt important que portem un control de quina versió de l'aplicació estem desenvolupant, deixant ben clar quines parts es comporten diferent, que noves coses es poden fer ara, etc.  
  
Hi ha una sèrie de sistemes per ajudar-nos a portar un control de les versions dels nostres programes.  
  
Els més coneguts: *CVS*, *Subversion*, *Mercurial*, *Git* (un dels més populars actualment).  

  


  
