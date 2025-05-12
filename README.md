# 🔠 Gerador de Letras em Círculo

Uma ferramenta web para criar imagens de letras ou iniciais dentro de círculos coloridos, perfeito para avatares, ícones e identificação visual.
<!--
![Preview do Gerador](https://raw.githubusercontent.com/souzaseven/Site2/Desafios/icon%20eu.ico)
-->
## ✨ Funcionalidades

- **Personalização Completa**:
  - Letra ou texto curto (até 10 caracteres)
  - Seletor de cores para o círculo
  - Seletor de cores para o texto
  - Ajuste automático do tamanho da fonte

- **Exportação Fácil**:
  - Download como imagem PNG
  - Download como ícone ICO
  - Visualização em tempo real

- **Design Responsivo**:
  - Adapta-se a qualquer tamanho de tela
  - Interface intuitiva
  - Previsualização interativa

## 🛠️ Tecnologias Utilizadas

- **Frontend**:
  - HTML5 Canvas
  - CSS3 moderno
  - JavaScript puro (ES6+)

- **Bibliotecas**:
  - Google Analytics (métricas)
  - Google AdSense (monetização)

## 📂 Estrutura de Arquivos
gerador-letras/ <br>
├── index.html # Página principal <br>
├── styles.css # Estilos personalizados <br>
└── script.js # Lógica do gerador <br>


## 🎨 Design e Interface

- **Tema Azul Moderno**:
  - Fundo azul (#007ced)
  - Área branca para controles
  - Sombras e bordas arredondadas

- **Layout Organizado**:
  - Controles à esquerda
  - Visualização à direita
  - Botões de ação claros

- **Interações**:
  - Atualização em tempo real
  - Efeitos hover nos botões
  - Feedback visual imediato

## ⚙️ Como Funciona

### Geração da Imagem
```javascript
function generateImage() {
    // Configura canvas
    canvas.width = 512;
    canvas.height = 512;
    
    // Desenha círculo
    ctx.beginPath();
    ctx.arc(canvas.width/2, canvas.height/2, 200, 0, Math.PI*2);
    ctx.fillStyle = circleColor;
    ctx.fill();
    
    // Ajusta tamanho da fonte
    let fontSize = 200;
    do {
        ctx.font = `bold ${fontSize}px Arial`;
        fontSize -= 10;
    } while(ctx.measureText(textInput).width > 400 && fontSize > 20);
    
    // Desenha texto
    ctx.fillStyle = textColor;
    ctx.fillText(textInput, canvas.width/2, canvas.height/2);
}
```
### Download da Imagem
```javascript
// Configura links de download
downloadLink.href = canvas.toDataURL('image/png');
iconDownloadLink.href = canvas.toDataURL('image/x-icon');
```
###💡 Dicas de Uso  <br>
Para melhores resultados:  <br>
Use 1-2 caracteres para ícones  <br>
Cores contrastantes entre texto e fundo  <br>
Tamanho padrão de 512x512 pixels  <br>

Personalização:
```css
/* Para mudar o tema */
body {
    background-color: #2c3e50;
}
.btn {
    background-color: #e74c3c;
}
```
Para modificar o canvas:
```javascript
// Alterar tamanho do círculo
ctx.arc(canvas.width/2, canvas.height/2, 150, 0, Math.PI*2);
```
