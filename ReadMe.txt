-----INDEX.HTML-----

<HEAD>  # Tutto cio' che c'è in <head> serve a fornire al browser le informazioni di questa pagina
   come il titolo, tipo di codifica, stylesheet e scripts. Tutto cio' aiuta il browser a 
   renderizzare la pagina correttamente.
    - Il link nella riga 6 ci permette di usare il framework "bootstrap" per la nostra pagina.
    - Nella riga 7 c'è un tag di script che carica una libreria di bootstrap. Ci permette
      di usare delle classi e delle componenti di bootstrap nel nostro codice html.
      - Nelle righe 9 e 10 ci serviamo delle google apis per poter utilizzare determinati font
        i quali non sono scaricati sulla nostra macchina, da poter utilizzare poi nel nostro 
        documento HTML;

<BODY> # In <body> vi è principalmente un div (class="container"), il qualw contiene altri due div.
          Il primo ha due elementi, uno con tag h1 e l'altro con il tag p (display sulla pagina di alcune scritte).
          Vi sono poi dei <label> contenenti i due "input type="text" dove verrano poi inserite le stringhe
          da posizionare sull'immagine.
          Infine si ha un bottone, pilotato da uno script, il quale una volta premuto genererà l'immagine
          con i due input di testo.

----STYLE.CSS-----
# Qui troviamo svariati stili applicati ai vari class/id/tags; essi rendono la pagina HTML più 
  fluida e pulita, impostando vari tipi di colori e vari tipi di font.


----SCRIPT.JS----

# La funzione principale dello script è "window.onload", la quale "si attiva" nell'esatto momento in cui
  il browser carica l'oggetto in causa.
  Le variabili dichiarate con "var" sono poi inizializzate principalmente con due metodi.
  - Abbiamo il metodo "document.getElementById()" che prende un parametro : una stringa che rappresenta
  l'id di un attributo di un elemento HTML. In questo caso (es : riga 2, riga 3), stiamo passando
  come argomenti gli id "addMemeForm" e "memeList".

  - Abbiamo poi il metodo "createElement()", la quale non fa altro che creare un elemento, in questo 
  caso (es : riga 12) crea un bottone.

  Ci sono poi altri metodi come classList, che viene usato per aggiunge, rimuovere o controllare
  la presenza di una classe su un'elemento. (Es riga : 14) Aggiunge la classe "remove" all'elemento
  "removeBtn".

  - Il metodo appendChild(), aggiunge alla fine di un'elemento un'altro elemento.
  (es riga : 28) in questo caso il metodo in questione sta aggiungengo "imgDiv" a "newMeme".

  - Il metodo reset(), resetta il form.

  - La funzione a riga 65, si mette in ascolto per un "click event" sull'elemento memeList. Se il
    target del "click event" è un bottone, questo rimuove il "parent node" di quel bottone.
    Lo scopo di questa funzione è quello di permettere all'utente di rimuovere un meme 
    generato cliccando sul bottone associato.
