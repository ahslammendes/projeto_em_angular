# Meu App Angular — Ambiente Musical 3D Interativo

Projeto desenvolvido em **Angular 21** (com suporte a Server-Side Rendering) integrado a uma cena interativa em **Three.js** para visualização de um ambiente musical retrô em 3D, estilizado com iluminação e paleta de cores inspiradas em um jazz club noturno e galeria de álbuns de vinil personalizados na parede.

---

## Sobre o Projeto

O objetivo deste repositório é unir uma base moderna em Angular com visualização gráfica 3D no navegador utilizando WebGL / Three.js:

- **Ambiente 3D (`retro_music_lovers_date.glb`):** Sala retrô completa com vitrola/gramofone, sofá, luminária de arco, plantas, velas, taças de vinho e discos na parede lateral.
- **Galeria de Álbuns na Parede (`vinyl_record_with_custom_album.glb`):** 6 capas de álbuns posicionadas em duas fileiras de três na parede principal, texturizadas dinamicamente com capas personalizadas (`public/capas/album1.jpg` a `album6.jpg`).
- **Paleta & Iluminação Customizadas:** Reestilização completa de materiais em tempo de execução e iluminação atmosférica quente (tons de carmesim, mogno, âmbar e dourado) com `ACESFilmicToneMapping` e `OrbitControls` para navegação livre em 360°.
- **Base Angular 21 + SSR:** Estrutura limpa do componente raiz pronta para expansão em rotas e componentes Angular.

---

## Tecnologias Utilizadas

- **[Angular 21](https://angular.dev/)** (`@angular/core`, `@angular/router`, `@angular/ssr`)
- **[Three.js](https://threejs.org/)** (`GLTFLoader`, `OrbitControls`, `WebGLRenderer`)
- **TypeScript 5.9** & **Express 5** (para SSR)
- **Vitest** (testes unitários)

---

## Estrutura de Pastas Principais

```text
meu-app-angular/
├── public/
│   ├── capas/                              # Capas personalizadas dos álbuns (album1.jpg a album6.jpg)
│   ├── retro_music_lovers_date.glb         # Modelo 3D principal do ambiente retrô
│   ├── vinyl_record_with_custom_album.glb  # Modelo 3D base da capa de vinil
│   └── viewer.html                         # Visualizador 3D interativo em Three.js
├── src/
│   ├── app/                                # Componentes, rotas e configuração do Angular
│   ├── index.html                          # HTML principal da aplicação Angular
│   ├── main.ts                             # Ponto de entrada do cliente (Browser)
│   ├── main.server.ts                      # Ponto de entrada do servidor (SSR)
│   └── server.ts                           # Servidor Express para SSR
├── angular.json                            # Configurações de build e serve do Angular CLI
└── package.json                            # Dependências e scripts do projeto
```

---

## Como Executar Localmente

### Pré-requisitos

- **Node.js** (versão 20+ recomendada)
- **npm** (instalado junto com o Node.js)

### Passo a passo

1. Clone o repositório:
   ```bash
   git clone https://github.com/ahslammendes/projeto_em_angular.git
   cd projeto_em_angular
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Inicie o servidor de desenvolvimento:
   ```bash
   npm start
   ```
   *(ou `npx ng serve`)*

4. Acesse no navegador:
   - **Aplicação Angular:** `http://localhost:4200/`
   - **Visualizador 3D do Ambiente Musical:** `http://localhost:4200/viewer.html`

---

## Personalizando os Álbuns na Parede

No arquivo [`public/viewer.html`](public/viewer.html), você pode alterar facilmente as capas exibidas, o tamanho ou a disposição das fileiras editando as constantes no topo do script:

```js
const ALBUMS = [
  { cover: 'capas/album1.jpg' },
  { cover: 'capas/album2.jpg' },
  { cover: 'capas/album3.jpg' },
  { cover: 'capas/album4.jpg' },
  { cover: 'capas/album5.jpg' },
  { cover: 'capas/album6.jpg' },
];
const ALBUM_SIZE = 16;      // lado do álbum
const ALBUM_GAP_X = 4;      // espaço horizontal entre álbuns
const ALBUM_GAP_Y = 3.5;    // espaço vertical entre fileiras
const ALBUM_COLS = 3;       // álbuns por fileira
```
