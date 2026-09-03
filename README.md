# 🎵 Top 100 Álbuns - Estilo Revista

Este é um projeto web front-end que exibe os 100 álbuns mais ouvidos e influentes do mundo. Ele foi construído com uma estética editorial e impactante, inspirada em grandes revistas de cultura pop e música (como a *Rolling Stone*).

## 🚀 Tecnologias Utilizadas

O projeto foi construído utilizando os fundamentos clássicos da web, sem a necessidade de frameworks pesados. Isso garante um carregamento super rápido e facilita qualquer customização:

- **HTML5**: Estruturação do layout.
- **CSS3**: Estilização visual (fundo claro, tipografia pesada de impacto e layouts em grid).
- **JavaScript (Vanilla)**: Injeção de conteúdo dinâmico e transições suaves ao alternar entre as matérias dos álbuns.

## 📂 Estrutura de Arquivos

O projeto está dividido em apenas quatro arquivos principais para manter a simplicidade:

- `index.html`: A estrutura base da página (cabeçalho, barra de navegação e layout de colunas).
- `style.css`: Todo o design do site. Totalmente responsivo, adaptando-se para celulares e desktops.
- `script.js`: A lógica responsável por trocar as informações do álbum selecionado sem precisar recarregar a tela.
- `data.js`: Nosso "banco de dados". É aqui que moram as informações de todos os álbuns (nome, artista, imagem de capa, etc.).

## 🛠️ Como Usar e Testar

Nenhuma instalação ou terminal é necessária para visualizar este projeto! 

1. Certifique-se de ter os arquivos na mesma pasta.
2. Dê um clique duplo no arquivo **`index.html`**.
3. O site abrirá instantaneamente no seu navegador padrão.

> **Dica**: Se estiver usando o VS Code, você pode usar a extensão *Live Server* para ver as alterações em tempo real.

## 📝 Como Adicionar Novos Álbuns

Para expandir a lista até chegar aos 100 álbuns, basta editar o arquivo `data.js`. Adicione um novo bloco de chaves `{}` dentro da lista seguindo exatamente esta estrutura:

```javascript
{
    id: "nome-unico-sem-espacos",
    title: "Nome do Álbum",
    artist: "Nome do Artista",
    releaseDate: "Data de Lançamento",
    genre: "Gênero Musical",
    streams: "Número de Reproduções",
    coverUrl: "url-ou-nome-da-imagem.jpg",
    description: "Um resumo sobre a importância do álbum.",
    tracklist: ["Faixa 1", "Faixa 2", "Faixa 3"],
    reception: "Como a crítica avaliou o álbum."
}
```

O código em JavaScript irá automaticamente ler as novas informações, criar o botão no menu lateral e exibir o conteúdo lindamente na tela!

## 🅰️ Sobre o uso de Angular

Embora a pasta principal do projeto se chame `projeto_em_angular` e contenha uma estrutura Angular inicial, optamos por construir a interface desta revista digital focada em música (Top 100 Álbuns) inicialmente utilizando **Vanilla HTML, CSS e JS puro**. 

Essa abordagem foi escolhida para entregar rapidamente uma base sólida, semântica e focar 100% no aperfeiçoamento da **estética e design editorial** sem a complexidade de configuração de rotas e componentes pesados no primeiro momento. 

Como o código (HTML e CSS) está extremamente limpo e modularizado, ele funciona perfeitamente como um **protótipo de alta fidelidade** e pode ser facilmente refatorado e portado para dentro dos componentes do Angular (`.component.html`, `.component.css` e `.component.ts`) no futuro!
