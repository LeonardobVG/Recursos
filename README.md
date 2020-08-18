# Recursos

### Para remover títulos do vimeo: 
```
?&portrait=0&byline=0&title=0
```

### Inserir a função button:
```
button type="button" id="botao" onclick="location.href='tela-5.html'" class="btn-top w-button" onclick="saveProgress();"
```

### Script Gen
```
<script src="js/gen_report.js" type="text/javascript"></script>
```

### Adiciona Counter
```
<script>    document.getElementById("botao").disabled= true; </script>

<script>    
var counter = 0;
function myTimer() {  
  var timer = setTimeout( function() 
  {    counter++;
  if( counter < 124 ) {
  myTimer();
  }    
  else {
  document.getElementById("botao").disabled= false;
  } 
  }, 1000 );
  }  
  myTimer(); 
  </script>
```
### VIMEO
```
var iframe = document.getElementById('vimeo-video'); //id do video 
    var player = new Vimeo.Player(iframe);

    var json = {};
    json.aluno = "aluno"; //webservice-rest
    json.url = document.URL;
    json.video = {};
    json.video.title = "vimeo_title";

    player.on('play', function() {
      json.video.started = true;
      json.video.finished = false;
      console.log(JSON.stringify(json));
    });

    player.on('ended', function() {
      document.getElementById("botao").disabled = false;
      json.video.finished = true;
      console.log(JSON.stringify(json));
    });
 ```
  
### QUESTÕES/ATIVIDADES
 ```
 <script>
	  
	  document.getElementById("avancar").disabled = true;
	 	  
	  function enable_avancar () {
	    document.getElementById("avancar").disabled = false;
	  }
    
  </script>
   ```
Inserir no input da resposta correta: ```  onclick="enable_avancar();"```

### Iframe da interação do Articulate
```
<iframe width="980" height="550" frameborder="0" scrolling="no" marginheight="10" marginwidth="50"src="interacao/story.html"></iframe>
```

### Iframe Responsivo
```
.wrapper {
  width: 100%;
  height: 100%;
  margin: 0 auto;
  background: #ffffff;
}

.h_iframe {
  position: relative;
}

.h_iframe .ratio {
  display: block;
  width: 100%;
  height: auto;
}

.h_iframe iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```

Inserir ```class=wrapper``` em cada iframe
