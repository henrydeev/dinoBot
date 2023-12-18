# dinoBot

Um bot que joga o jogo do T-Rex do Google Chrome por você.

![Pontuação Máxima](https://i.imgur.com/uAlZzuq.png)

Quando comecei este projeto, achei que seriam pelo menos 200 linhas de código, mas aqui estou eu atingindo pontuações de seis dígitos, sendo que o bot em si tem apenas 10 linhas de código. Obviamente, preciso simular as entradas de teclas, e é isso que ocupa as outras 50 linhas.

Consegui reduzir bastante o código encontrando uma fórmula para calcular a distância necessária para pular antes de um obstáculo. Descobri isso apenas jogando o jogo e registrando a velocidade exata do T-Rex e várias outras variáveis que o jogo utiliza. Ao inserir isso em qualquer software de gráficos, seria possível ver uma clara correlação entre a velocidade do T-Rex e a distância do próximo obstáculo (no momento do pulo). A distância sempre seria cerca de 20 * velocidade. A partir daí, só restou digitar o código!

# Como Usar

1. Abra o Chrome e vá para: chrome://dino/ (ou desconecte sua internet)
2. Pressione "F12" e vá para "Console"
3. Copie e cole o seguinte texto e pressione Enter.
```js
var scripturl='https://raw.githubusercontent.com/henrydeev/dinoBot/main/dinoBot.txt';
fetch(scripturl).then(r=>r.text()).then(s=>{var e=document.createElement('script');e.innerHTML=s;document.head.appendChild(e);}).catch(e=>console.error('Erro ao carregar o script:',e));
```
4. Inicie o jogo!

**Esse bot foi escrito em JavaScript apenas para fins educacionais, eu permito a modificação para aprimorar o bot, mas deve adicionar meu repositório como créditos.**

## Autor

- henrydeev / henrydxd
