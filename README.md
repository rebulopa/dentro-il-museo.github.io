# **Corso DENTRO il MUSEO**  
__*Esperienze di AR con AR.js*__

### IL TEMPLATE
Il Template fa riferimento al file che si trova nella DIRECTORY PRINCIPALE del corso e che a sua volta richiede la presenza di tre directory secondarie così denominate <br>
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
Nella sezione *head* troviamo il riferimento al foglio di stile *styles.css* che si trova nella cartella __styles__ della directory principale. Il file .css stabilire lo stile del documento per ogni singolo elemento della pagina, quindi font, margini etc..
In questo caso il font per lo stile del documento viene richiamato tra quelli disponibili in GoogleFonts attraverso una APIs specifica per lo stile *"Poppins"*
```
<head>
    <link rel="stylesheet" href="styles/styles.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Poppins">
</head>
```

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
### COME CREARE LA PROPRIA DIRECTORY

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

### COME MODIFICARE IL TEMPLATE

### INSERIRE FILE VIDEO


### LISTA PAGINE PER ESPERIENZE 3D
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
