# SnakeGame
Projeto baseado em linguagem JavaScript e desenvolvido através do acompanhamento das aulas disponibilizadas pela Digital Innovation One juntamente com a professora: Gabriela Pinheiro (Mobile Developer Hurst Capital).  
https://digitalinnovation.one    
![](https://github.com/JoaoErick/projeto-SnakeGame-javascript/blob/master/img/demonstracao2.png)
> Fonte: Próprio autor (2020)  
-------------  
### Como Jogar 
Assumindo que o download deste repositório já foi realizado na máquina.
* Abra a pasta raiz.
* Execute o arquivo ```index.html``` no seu navegador preferido.
* Com o jogo renderizado, utilize as setas do teclado para movimentar a cobrinha ```⇦``` ```⇧``` ```⇨``` ```⇩```
* Consiga o maior número de pontos possível comendo as frutinhas do mapa.
* Caso a sua cobrinha se chocar com o seu próprio corpo: GAME OVER!
* Para reiniciar o jogo, atualize o seu navegador.
* Divirta-se!!!
-------------  
### Trecho de código desenvolvido em JavaScript　

```JavaScript
function criarCobrinha(color){
    for(i=0; i<snake.length; i++){
        context.fillStyle = color;
        context.fillRect(snake[i].x, snake[i].y, box, box);
    }
}

function drawFood(){
    context.fillStyle = "red";
    context.fillRect(food.x, food.y, box, box);
}

document.addEventListener('keydown', update);

function update(event){
    if(event.keyCode == 37 && direction != "right") direction = "left";
    if(event.keyCode == 38 && direction != "down") direction = "up";
    if(event.keyCode == 39 && direction != "left") direction = "right";
    if(event.keyCode == 40 && direction != "up") direction = "down";
}
```  
-------------  
### Trecho de código desenvolvido em CSS

```css
h1{
    margin-bottom: 2px;;
}

.canvas{
    border-color: black;
    border-style: solid;
}

.count{
    margin-top: 1px;
    font-family: arial;;
}
```  
-------------  

### Trecho de código desenvolvido em HTML

```html
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <link rel="stylesheet" href="./css/style.css">
        <link rel="shortcut icon" href="./img/Blackvariant-Button-Ui-Requests-13-Snake.ico" />
        <script defer src="./js/script.js"></script>
        <title>Snake Game</title>
    </head>
</html>
```
### Fim
