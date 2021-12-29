# **Corso DENTRO il MUSEO**  
__*Esperienze di AR con AR.js*__

### IL TEMPLATE
Il Template fa riferimento al file __esercizioDiM.html__ che si trova nella *CARTELLA PRINCIPALE* del corso e che a sua volta richiede la presenza di tre *CARTELLE SECONDARIE* così denominate <br>
__styles__ contenente i file di formattazione degli stili della pagina .html<br>
__patterns__ contiene i file per i markers siano essi target o immagini<br>
__media__ contiene i file per l'esperienza AR, quindi per i 3D (.obj, .mtl etc.) o i video (.mp4)<br>
All'interno di *script* viene richiamata la libreria di riferimento di AR.js denominata aframe, che si trova nel web e che viene richiamata attraverso un indirizzo url specifico 
```
<!DOCTYPE html>
<html>
<script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
<!-- we import arjs version without NFT but with marker + location based support -->
<script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
```
Nella sezione *head* troviamo il riferimento al foglio di stile *styles.css* che si trova nella cartella __styles__ della cartella principale. Il file .css stabilisce lo stile del documento per ogni singolo elemento della pagina, quindi font, margini etc..
In questo caso il font per lo stile del documento viene richiamato tra quelli disponibili in GoogleFonts attraverso una APIs specifica per lo stile *"Poppins"*
```
<head>
    <link rel="stylesheet" href="styles/styles.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Poppins">
</head>
```
Nella sezione *a-marker* troviamo il codice che permette di associare il marker all'esperienza 3D. In questo caso poichè il file .html si trova nella cartella principale (dentro-il-museo.github.io) il percorso url della pagina sarà il seguente: https://dentro-il-museo.github.io/esercizioDiM.html
per quanto riguarda le classi richiamate "pattern" (riga 4) e obj-model (riga 8) il codice richiama dei file che si trovano nelle cartelle secondarie __patterns__ e __media__ per inserire il percorso corretto si andrà quindi a inserire il percorso url utilizzando uno __/__ che precede il __nome della cartella secondaria__ e successivamente uno __/__ che precede il __nome del file__ compreso della sua estensione in questo modo _/patterns-media/nome file_
```
<body>
    <button class="button">Info</button>
    <a-scene vr-mode-ui="enabled: false" embedded arjs>
        <a-marker type="pattern" url="/patterns/pattern-marker.patt">
            <a-entity
            position="0 0 0"
            scale="4 4 4"
            obj-model="obj: url(/media/dama.obj);mtl: url(/media/dama.mtl);"
            animation="property: rotation; dur: 6000; to: 0 360 0; loop: true; easing: linear;"
            > </a-entity>
        </a-marker>
        <a-entity camera></a-entity>
    </a-scene>
</body>
</html>
```
### COME INDIRIZZARE IL PROGETTO .HTML ALLA PROPRIA DIRECTORY DI GRUPPO
All'interno della directory principale sono state create 17 cartelle secondarie recanti il nome del gruppo e all'interno delle cartelle denominate GR_xx (con xx= numero del gruppo) sono state create altrettante sottocartelle __styles__ __patterns__ __media__ per ricreare l'esempio. In questo caso quindi all'interno del template per richiamare i file corretti andrà inserito nel campo url anche il percorso della cartella secondaria che fa riferimento al gruppo GR_xx e delle sottocartelle create per contenere i file di progetto. Vedi esempio:
```
        <a-marker type="pattern" url="/GR_xx/patterns/pattern-marker.patt">
            <a-entity
            position="0 0 0"
            scale="4 4 4"
            obj-model="obj: url(/GR_xx/media/dama.obj);mtl: url(/GR_xx/media/dama.mtl);"
            animation="property: rotation; dur: 6000; to: 0 360 0; loop: true; easing: linear;"
            > </a-entity>
        </a-marker>
```
### LISTA PAGINE PER ESPERIENZE 3D
Per semplificare il test delle vostre esperienze abbiamo elencato le pagine web per l'esperienza di ogni singolo gruppo.<br>
Tenere presente che ovviamente il file nella cartella gruppo dovrà avere l'estensione .html<br>
<br>
https://dentro-il-museo.github.io/GR_01/GR_01.html <br>
https://dentro-il-museo.github.io/GR_02/GR_02.html <br>
https://dentro-il-museo.github.io/GR_03/GR_03.html <br>
https://dentro-il-museo.github.io/GR_04/GR_04.html <br>
https://dentro-il-museo.github.io/GR_05/GR_05.html <br>
https://dentro-il-museo.github.io/GR_06/GR_06.html <br>
https://dentro-il-museo.github.io/GR_07/GR_07.html <br>
https://dentro-il-museo.github.io/GR_08/GR_08.html <br>
https://dentro-il-museo.github.io/GR_09/GR_09.html <br>
https://dentro-il-museo.github.io/GR_10/GR_10.html <br>
https://dentro-il-museo.github.io/GR_11/GR_11.html <br>
https://dentro-il-museo.github.io/GR_12/GR_12.html <br>
https://dentro-il-museo.github.io/GR_13/GR_13.html <br>
https://dentro-il-museo.github.io/GR_14/GR_14.html <br>
https://dentro-il-museo.github.io/GR_15/GR_15.html <br>
https://dentro-il-museo.github.io/GR_16/GR_16.html <br>
https://dentro-il-museo.github.io/GR_17/GR_17.html <br>
