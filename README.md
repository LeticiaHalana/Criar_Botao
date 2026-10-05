# 🎯 Conexão entre HTML, CSS E JS + Criação de um botão funcional para alerta.

Bem-vindos ao material de aula! Aqui você encontrará os exemplos de código e o roteiro das atividades práticas.

---


## 1. Como HTML, CSS e JS se Conectam?

O **HTML** cuida da *estrutura*, o **CSS** do *estilo* e o **JavaScript** do *comportamento*. A ligação de todos os arquivos ocorre no seu `index.html`.

### 📄 `index.html`
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Exemplo Botão</title>

  <!-- 1. LIGAÇÃO COM O CSS (Usando a tag <link> dentro do <head>) -->
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- Elemento HTML -->
  <button id="meu-botao" class="btn-principal">Clique Aqui</button>

  <!-- 2. LIGAÇÃO COM O JAVASCRIPT (Usando a tag <script> antes de fechar o </body>) -->
  <script src="script.js"></script>
</body>
</html>
```

### 🎨 ` style.css`
```css
/* Estilizando o botão pela classe */
.btn-principal {
  background-color: #0056b3;
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: 6px;
  font-size: 16px;
  cursor: pointer;
}

.btn-principal:hover {
  background-color: #003d80;
}
```
### ⚡ `script.js`
```js
// O JS se conecta ao elemento do HTML buscando pelo ID 'meu-botao'
const botao = document.getElementById('meu-botao');

// Adiciona a interatividade
botao.addEventListener('click', function() {
  alert('Você clicou no botão!');
});
```

### 💡 Comparativo Rápido 

| Conceito | Como você faz em **C#** | Como você faz em **JavaScript** |
| :--- | :--- | :--- |
| **Imprimir no Terminal** | `Console.WriteLine("Olá");` | `console.log("Olá");` |
| **Variáveis** | `int idade = 20;` | `let idade = 20;` |
| **Constantes** | `const double PI = 3.14;` | `const PI = 3.14;` |
| **Condicional** | `if (x > 10) { ... }` | `if (x > 10) { ... }` *(Identico!)* |
| **Laço For** | `for (int i=0; i<5; i++)` | `for (let i=0; i<5; i++)` |

## 📥 Entrada de Dados no Navegador Web (Modo Rápido / Didático)

Se estiverem testando o código no navegador web associado a uma página HTML, a forma mais simples e direta de simular uma leitura do teclado é através do comando `prompt()`:

```javascript
// O prompt() abre uma caixa de diálogo e aguarda o usuário digitar
let nome = prompt("Digite o seu nome:");

// O prompt() SEMPRE devolve uma String. Para números, converta usando Number():
let nota1 = Number(prompt("Digite a primeira nota:"));
let nota2 = Number(prompt("Digite a segunda nota:"));

let media = (nota1 + nota2) / 2;

console.log(`Aluno: ${nome} | Média: ${media}`);
alert(`A média do ${nome} é: ${media}`);
```
# 🛠️ Atividades Práticas 

### 📝 Atividade 1: HTML — Estruturando a Página com Divs
**Instrução:** Crie um arquivo `index.html`. Monte a estrutura básica de um layout de site utilizando **3 tags `<div>`** distintas para organizar os seguintes blocos de conteúdo:

1. A primeira `<div>` deve conter um título `<h1>` com o nome da sua Software House e um parágrafo `<p>` com o slogan.
2. A segunda `<div>` deve conter um `<h2>` com o título "Nossos Serviços" e uma lista não ordenada `<ul>` com 3 itens (`<li>`).
3. A terceira `<div>` deve conter as informações de contato no rodapé (um `<p>` com e-mail e telefone).

---

### 🎨 Atividade 2: CSS — Aplicando Estilos com Classes
**Instrução:** Crie um arquivo `style.css` e conecte-o ao seu HTML. Em seguida, aplique classes para formatar o exercício das `<div>`:

1. Crie uma classe chamada `.card` e aplique nas `<div>`. Dê a elas uma cor de fundo clara (`background-color`), uma borda suave e um espaçamento interno (`padding: 20px`).
2. Crie uma classe chamada `.texto-destaque` para alterar a cor da fonte e deixar o texto em negrito. Aplique essa classe no slogan e nos contatos.
3. Crie uma classe `.titulo-secao` que mude a cor das tags `<h1>` e `<h2>` para uma cor à sua escolha.

---

### ⚡ Atividade 3: JavaScript — Lógica Básica (Semelhança com C#)
> 💡 **Dica para os alunos:** No C# você usa `int`, `string` e `Console.WriteLine()`. No JavaScript usaremos `let`, `const` e `console.log()`. A sintaxe de `if`, `else` e `for` é idêntica!

Utilize um compilador online de sua preferência:

1. **Declaração de Variáveis e Operações:**
   * **Desafio:** Declare duas variáveis (`let a` e `let b`) com valores numéricos. Crie uma terceira variável que guarde a soma de `a` e `b` e exiba o resultado no console no formato: `"A soma é: X"`.

2. **Estrutura Condicional (`if / else`):**
   * **Desafio:** Declare uma variável `let nota = 8`. Crie uma estrutura `if / else` que verifique: se a nota for maior ou igual a 7, imprima no console `"Aprovado"`. Caso contrário, imprima `"Reprovado"`.

3. **Operadores Lógicos (`&&` / `||`):**
   * **Desafio:** Declare duas variáveis: `let idade = 17` e `let possuiAutorizacao = true`. Escreva um `if` que verifique se a pessoa pode entrar no evento (a regra é: precisa ter 18 anos **OU** possuir autorização dos pais). Exiba `"Acesso liberado"` ou `"Acesso negado"` no console.

4. **Laço de Repetição (`for`):**
   * **Desafio:** Crie um laço `for` que conte de 1 até 10 e imprima cada número no console (exatamente igual ao `for` do C#).
