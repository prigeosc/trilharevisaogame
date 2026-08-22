# Prigeosc · Trilha do Terceirão

Site estático (HTML + CSS + JS puro, sem build) com a trilha gamificada de
revisão de Geografia. Não precisa de Node, servidor nem build — é só
hospedar os arquivos como estão.

## Estrutura

```
index.html    → o jogo inteiro (HTML + CSS + JS num arquivo só)
prigeosc.png  → mascote (precisa ficar ao lado do index.html)
mapas/        → recompensas (mapas mentais) desbloqueadas ao concluir cada etapa
```

## Progresso do aluno

O progresso (XP, estrelas, sequência, conquistas, etapas concluídas) fica
salvo automaticamente no navegador do aluno (`localStorage`) — sem login,
sem conta, sem servidor. Isso significa que o progresso é por
navegador/aparelho: se o aluno limpar os dados do navegador, trocar de
computador ou usar outro navegador, ele começa do zero naquele lugar. Não
há sincronização entre dispositivos.

## Rodar localmente

Não precisa de nada além de um navegador — dá para abrir o `index.html`
direto. Se preferir servir por HTTP:

```bash
npx serve .
# ou
python3 -m http.server 8080
```

## Publicar

### GitHub Pages
Em **Settings → Pages** do repositório, escolha a branch `main` e a pasta
raiz (`/`). O site fica em `https://SEU-USUARIO.github.io/SEU-REPO/`.

### Qualquer hospedagem estática
Como é só HTML/CSS/JS (sem build), também funciona em Netlify, Vercel,
Firebase Hosting, ou qualquer servidor que sirva arquivos estáticos — é só
subir os três itens da estrutura acima, mantendo-os na mesma pasta.

## Subir para o GitHub

```bash
git init
git add .
git commit -m "Trilha Prigeosc"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
git push -u origin main
```
