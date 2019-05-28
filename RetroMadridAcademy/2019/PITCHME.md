---?image=../assets/image/ivan_televnyy.jpg

# AbadIA  

### La Inteligencia Artificial que juega (y resolverá) "La abadía del crimen" 

---

## Agenda

- Reinforcement Learning Intro

- The AbadIA project

---

## ¿alguien en RetroMadridAcademy NO conoce EL JUEGO?

+++
## El juego

- Programado en 1987 por **Paco Menéndez** con gráficos de **Juan Delcán**.
- Basado de forma no oficial en el libro de **Umberto Eco** **"El nombre de la rosa"**.
- Considerado por "Retro Gamer" uno de los 10 juegos perfecto para Spectrum 128.
- Clásico de culto en España.

+++

### Sello oficial

![Stamp](https://www.correos.es/ss/Satellite?blobcol=urldata&blobheadername1=Content-Disposition&blobheadervalue1=filena
me%3Dboc_TIC_Videojuegos_Abadia_Crimen_b1m31.jpg&blobkey=id&blobtable=MungoBlobs&blobwhere=1365530659478&ssbinary=true)

+++

### Museo

![Museum1](https://pbs.twimg.com/media/DO1d5JjW4AEnt_5.jpg)

![Museum2](https://www.fi.upm.es/GestorTablon/GTuploads/3215-4-DSC00326_FB.jpg)

---

## El desafío

---

## El desafío
### ¿cómo maneja la IA el juego?

+++

![Video](https://www.youtube.com/watch?v=HnA5WHxMIUo)

---

## El desafío
### ¿cómo recompenso a la IA cuando juega bien?

+++

### Falta enlace video jugando a Pong

+++

### Falta video jugando a la abadía y preguntando ¿es este movimiento bueno?


### La recompensa

---

## The Challenge 

- 10^80 Number of atoms in our universe (Hawking said there are more)
- 10^120 Number of chess legal moves
- 10^761 Number of GO legal moves
- 5^N+4 abadIA legal moves where N is the depth of the game. For N=10000, 5^10004

---

## Las soluciones

+++

### Vigasoco
- Reconstrucción en C++ para Win32 y DirectX de "La abadía del crimen" por Manuel Abadía
- Parte del desensamblado del original para CPC464 realizado por Manuel Abadía
- VigasocoSDL adapta el código SDL y lo hace portable a múltiples sistemas

+++

### API (casi) REST

- FALTA Enlace al Swagger
- ¿demo con ngrok?

---

# Tomas falsas

---?image=https://slack-files.com/TAA21ESRJ-FASEN9VV5-f67387e257

---?image=https://slack-files.com/TAA21ESRJ-FARFWPP26-a5f30563ce

+++?image=https://slack-files.com/TAA21ESRJ-FASEN9VV5-f67387e257

+++?image=https://slack-files.com/TAA21ESRJ-FARFWPP26-a5f30563ce

+++?image=https://slack-files.com/TAA21ESRJ-FAQLYCZK3-23dceac819

+++?image=https://slack-files.com/TAA21ESRJ-FAQVCHS73-fabe2f50a1

+++?image=https://slack-files.com/TAA21ESRJ-FAQQW27GQ-d1a3203f2f

+++

@fa[kiss-wink-heart fa-3x](Gracias a Manuel Pazos por la depuración del código original)

---

## Como colaborar
- [Slack](https://laabadiadelcrimen.slack.com)
  + [https://laabadiadelcrimen.slack.com](https://laabadiadelcrimen.slack.com)
- [Organización en GitHub](https://github.com/LaAbadIAdelCrimen)
  + [https://github.com/LaAbadIAdelCrimen](https://github.com/LaAbadIAdelCrimen)

---

## How will do it


---

## The strategy 

--- 

## The game engine tuning
 
---

## The web server 

- The awesome idea we had: include a web server.|
- Now we have a REST based API.|
- Two way communication:
    - We send actions.|
        - Moves
        - Resets 
        - Save/Load states|
    - We got information.|
        - State dumps
        - Checkpoints
---
## make a fast demo or video with curl 
## some dumps, etc

---    
## How to scale

- At the beginning a laptop was enough.|
- But very soon you need more CPU/GPU.| 
- Then product like Google Cloud is your best ally.| 
- We create a Dockerfile, so now we can execute lots of instances of the game in parallel.

note: If we use Google Cloud services like GKE, we can launch hundred of games in parallel.

--- 

## Gathering information

- We recollect a lot of information: 
    - Game Info (timestamps, rewards, bonus, obsequium)|
    - Games moves (state, action, reward, new_state)|
    - Checkpoints (to restore the game at an interesting time)|
    - Models (for recovering good models o just make a benchmark)|

** Show some logs

---

## There are a lot of plumbing

- It takes a lot of time to get all the parts working all together.
- Building tests, testing every piece, every option. 
- Sometimes I feel like I was Mario Bros

(Include a picture of Mario Bros)   

--- 

## Managing the information at scale 

- As you grow the number of parallel game servers, the amount of information is bigger too.
- We can use Google Storage Buckets to store json.|
- We can use Bigquery to store all the info:|
    - Cheap storage.| 
    - Very Fast Queries.|
    - Billions of records (games, moves, etc)

---

## Now we need a playground to training the agents

- One the most frequently used tool is OpenAI Gym. 
- So we design an AbadIA gym. 
- The gym is an standarized place to train and interact with Reinforcement Learning agents.
- In our project the gym is framework to wrap the game engine.
- You can get it or fork it in this Github Repo: 
https://www.github.com/LaAbadIAdelCrimen/abadia-gym

--- 
--- 
## State of the Project AbadIA


--- 


## The Team

---

## Next steps

---

## How to Collaborate







---?image=../assets/image/lukas_blazek.jpg

## Tips!

<br>

@fa[arrows gp-tip](Press F to go Fullscreen)

@fa[microphone gp-tip](Press S for Speaker Notes)

---?image=assets/image/lukas_blazek.jpg

## Template Features

- Code Presenting |
- Repo Source, Static Blocks, GIST |
- Custom CSS Styling |
- Slideshow Background Image |
- Slide-specific Background Images |
- Custom Logo, TOC, and Footnotes |

---?code=sample/go/server.go&lang=golang&title=Golang File

@[1,3-6](Present code found within any Git repo source file.)
@[8-18](Without ever leaving your slideshow.)
@[19-28](Using GitPitch code-presenting with (optional) annotations.)

---?image=assets/image/maarten_deckers.jpg

@title[JavaScript Block]

<p><span class="slide-title">JavaScript Block</span></p>

```javascript
// Include http module.
var http = require("http");

// Create the server. Function passed as parameter
// is called on every request made.
http.createServer(function (request, response) {
  // Attach listener on end event.  This event is
  // called when client sent, awaiting response.
  request.on("end", function () {
    // Write headers to the response.
    // HTTP 200 status, Content-Type text/plain.
    response.writeHead(200, {
      'Content-Type': 'text/plain'
    });
    // Send data and end response.
    response.end('Hello HTTP!');
  });

// Listen on the 8080 port.
}).listen(8080);
```

@[1,2](You can present code inlined within your slide markdown too.)
@[9-17](Displayed using code-syntax highlighting just like your IDE.)
@[19-20](Again, all of this without ever leaving your slideshow.)

---?gist=onetapbeyond/494e0fecaf0d6a2aa2acadfb8eb9d6e8&lang=scala&title=Scala GIST

@[23](You can even present code found within any GitHub GIST.)
@[41-53](GIST source code is beautifully rendered on any slide.)
@[57-62](And code-presenting works seamlessly for GIST too, both online and offline.)

---?image=assets/image/lukas_blazek.jpg

## Template Help

- [Code Presenting](https://github.com/gitpitch/gitpitch/wiki/Code-Presenting)
  + [Repo Source](https://github.com/gitpitch/gitpitch/wiki/Code-Delimiter-Slides), [Static Blocks](https://github.com/gitpitch/gitpitch/wiki/Code-Slides), [GIST](https://github.com/gitpitch/gitpitch/wiki/GIST-Slides) 
- [Custom CSS Styling](https://github.com/gitpitch/gitpitch/wiki/Slideshow-Custom-CSS)
- [Slideshow Background Image](https://github.com/gitpitch/gitpitch/wiki/Background-Setting)
- [Slide-specific Background Images](https://github.com/gitpitch/gitpitch/wiki/Image-Slides#background)
- [Custom Logo](https://github.com/gitpitch/gitpitch/wiki/Logo-Setting), [TOC](https://github.com/gitpitch/gitpitch/wiki/Table-of-Contents), and [Footnotes](https://github.com/gitpitch/gitpitch/wiki/Footnote-Setting)

---?image=assets/image/lukas_blazek.jpg

## Go GitPitch Pro!

<br>
<div class="left">
    <i class="fa fa-user-secret fa-5x" aria-hidden="true"> </i><br>
    <a href="https://gitpitch.com/pro-features" class="pro-link">
    More details here.</a>
</div>
<div class="right">
    <ul>
        <li>Private Repos</li>
        <li>Private URLs</li>
        <li>Password-Protection</li>
        <li>Image Opacity</li>
        <li>SVG Image Support</li>
    </ul>
</div>

---?image=assets/image/lukas_blazek.jpg

### Questions?

<br>

@fa[twitter gp-contact](@gitpitch)

@fa[github gp-contact](gitpitch)

@fa[medium gp-contact](@gitpitch)

---?image=assets/image/gitpitch-audience.jpg

@title[Download this Template!]

### <span class="white">Get your presentation started!</span>
### [Download this template @fa[external-link gp-download]](https://gitpitch.com/template/download/timber)
