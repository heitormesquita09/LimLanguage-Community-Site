# LimLanguage-Community-Site

(LimLanguage Community Site)[https://limlanguage-community.vercel.app/]

Site da comunidade LimLanguage (Limeira): divulgação, agenda de eventos e contato.
Site estático (HTML, CSS e JavaScript puros), sem build, sem dependências e sem coleta de dados pessoais.

LimLanguage é uma comunidade independente, criada por estudantes de Limeira, sem vínculo oficial com a universidade.

## O que tem

- 9 páginas: Início, O que somos, Como funciona, Carimbos, Eventos, Como participar, Parcerias, Contato e Perguntas frequentes.
- Site em **português, espanhol e inglês** (seletor PT · ES · EN no topo; a escolha fica salva).
- **3 temas de cor** (seletor "Cores" no topo): cores da marca, vermelho-verde (daltonismo) e alto contraste.
- Agenda lida do arquivo `data/events.json` (veja `data/COMO-EDITAR-EVENTOS.md`).
- Botão "Entrar na comunidade" sempre visível no topo, inclusive no celular. Ele leva à página "Como participar", e só o botão dessa página abre o formulário de cadastro (em nova aba).
- Evento "próximo" com data passada vai sozinho para "Realizados". Para a equipe conferir a agenda: abra o site com `?checar=1` no endereço (ex.: `eventos.html?checar=1`).
- O link do grupo de WhatsApp **não** fica no site: ele é entregue na mensagem de confirmação do formulário de cadastro.

## Onde mexer

| O que | Onde |
|---|---|
| Link do formulário de cadastro, e-mail, Instagram | `assets/js/config.js` |
| Textos (PT/ES/EN) | `assets/js/i18n.js` |
| Eventos | `data/events.json` |
| Cores e visual | `assets/css/style.css` (variáveis no topo do arquivo) |

## Testar no computador

A agenda usa `fetch`, que não funciona abrindo o arquivo com duplo clique. Rode um servidor local na pasta do projeto:

```
python -m http.server 8000
```

e abra http://localhost:8000.

## Publicar (GitHub Pages)

Settings → Pages → Branch `main` → pasta `/ (root)`. Não há nenhuma etapa de build.
