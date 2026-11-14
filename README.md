# EARTHSONIC — DATA BEAT
Projeto independente (sem endosso da NASA). Next.js 15 + React 19 + TypeScript. Fontes e detalhes: DATA_SOURCES.md.

## Páginas
/ Home · /discover · /experiences · /experiences/climate · /experiences/fires (em validação) · /data · /about
Acessibilidade: botão no cabeçalho abre uma janela modal (preferências salvas neste navegador).

## Windows (PowerShell)
    npm.cmd install
    npm.cmd run update-data     # baixa o GISTEMP para public/data/climate (uso offline)
    npm.cmd test                # parser, player, seleção de mês, FIRMS
    npm.cmd run build
    npm.cmd run dev             # http://localhost:3000

## Wildfires (opcional)
Copie .env.example para .env.local e preencha FIRMS_MAP_KEY (chave gratuita do NASA FIRMS). Reinicie o servidor.
A chave só é lida no servidor. Sem ela, a página explica o que falta.

## Dados locais
Se update-data falhar: baixe https://data.giss.nasa.gov/gistemp/tabledata_v4/GLB.Ts+dSST.csv e rode
    npm.cmd run update-data -- --from-file "C:\caminho\GLB.Ts+dSST.csv"

## Publicar
Vercel (Next.js). Defina FIRMS_MAP_KEY nas variáveis de ambiente. Faça commit de public/data/climate para o modo offline.
