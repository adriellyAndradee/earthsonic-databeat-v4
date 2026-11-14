# EARTHSONIC 🌎🎵
### Hear the changes of our planet.

**Equipe:** Data Beat  
**Desafio:** NASA Space Apps Challenge  
**Projeto:** Plataforma interativa de sonificação de dados ambientais e científicos da Terra.

---

## 1. Sobre o projeto

O EARTHSONIC é uma proposta de plataforma interativa que transforma dados científicos sobre o nosso planeta em experiências sonoras.

A ideia é permitir que as pessoas não apenas visualizem as mudanças ambientais representadas nos dados e nas visualizações da NASA, mas também possam percebê-las por meio do som.

A plataforma busca aproximar ciência, tecnologia, música e acessibilidade, criando uma maneira alternativa e interativa de explorar informações sobre a Terra.

**Conceito principal:**

> Hear the changes of our planet.

## 2. O desafio

O projeto parte da proposta de explorar as visualizações do NASA Earth Information Center (EIC) e seus respectivos dados científicos.

O objetivo é desenvolver uma experiência que conecte:

- Visualizações científicas da NASA;
- Dados ambientais e climáticos;
- Sonificação de dados;
- Interatividade;
- Acessibilidade e inclusão.

A sonificação deve estabelecer uma relação compreensível entre os valores dos dados e os elementos sonoros. O som não deve ser aleatório: cada característica sonora precisa ter uma correspondência documentada com os dados utilizados.

## 3. Como o EARTHSONIC funciona

A experiência proposta segue este fluxo:

1. O usuário acessa a plataforma.
2. Explora as visualizações e os temas disponíveis.
3. Seleciona uma experiência científica.
4. Visualiza os dados correspondentes.
5. Reproduz a sonificação associada aos dados.
6. Compara a representação visual e sonora para compreender as informações.

A plataforma também pretende oferecer recursos de acessibilidade e suporte a diferentes idiomas.

## 4. Tecnologias

Tecnologias identificadas na estrutura inicial do projeto:

- Next.js
- React
- TypeScript
- Web Audio API
- HTML e CSS

As tecnologias e dependências devem ser conferidas no `package.json` da versão atual.

## 5. Estrutura do projeto

A organização geral esperada é:

```text
earthsonic-databeat/
├── app/
├── components/
├── lib/
├── public/
├── scripts/
├── tests/
├── package.json
├── package-lock.json
├── README.md
└── .gitignore
```

A estrutura real pode apresentar diferenças conforme a implementação atual.

## 6. Como executar o projeto

### Requisitos

- Node.js instalado;
- npm instalado;
- Visual Studio Code (recomendado);
- Git instalado para colaboração.

### Instalação

Clone o repositório:

```bash
git clone COLE_AQUI_O_LINK_DO_REPOSITORIO
```

Entre na pasta do projeto:

```bash
cd earthsonic-databeat
```

Instale as dependências:

```bash
npm install
```

Inicie o servidor de desenvolvimento:

```bash
npm run dev
```

Acesse no navegador:

http://localhost:3000

**Windows PowerShell:** caso o comando `npm` apresente problemas com a política de execução, utilize `npm.cmd install` e `npm.cmd run dev`.

Se houver variáveis de ambiente necessárias, consulte o arquivo `.env.example` e configure seu próprio `.env.local`. Nunca compartilhe chaves privadas no GitHub.

## 7. Desenvolvimento e estado atual

O projeto está em desenvolvimento. A equipe deve validar cada funcionalidade antes de considerá-la concluída.

### Funcionalidades e pontos de verificação

- [ ] Conferir a execução completa do aplicativo.
- [ ] Validar a navegação entre as páginas.
- [ ] Organizar a área de descoberta das visualizações.
- [ ] Validar as experiências individuais.
- [ ] Conferir a correspondência entre os dados e os sons.
- [ ] Validar a reprodução, pausa e controles de áudio.
- [ ] Conferir as fontes e referências dos dados científicos.
- [ ] Revisar a experiência em português e inglês.
- [ ] Testar recursos de acessibilidade.
- [ ] Verificar a adaptação para dispositivos móveis.
- [ ] Corrigir erros encontrados durante os testes.

### Melhorias previstas

- Aprimorar a organização e a navegação da plataforma.
- Tornar as experiências mais interativas.
- Melhorar a apresentação das visualizações e dos dados.
- Aprimorar os recursos de acessibilidade.
- Revisar a experiência sonora e suas correspondências científicas.
- Melhorar o desempenho e a estabilidade.

**Importante:** esta lista é um ponto de partida. Os colaboradores devem atualizar os itens conforme verificarem o código e concluírem as tarefas.

## 8. Acessibilidade

A acessibilidade é um dos aspectos importantes do EARTHSONIC.

Entre os recursos que devem ser avaliados e desenvolvidos estão:

- Navegação por teclado;
- Compatibilidade com leitores de tela;
- Contraste adequado;
- Textos e alternativas visuais para informações sonoras;
- Legendas e transcrições quando aplicáveis;
- Controles acessíveis de áudio;
- Ajustes de tamanho de texto;
- Suporte a movimento reduzido.

A integração com VLibras deve ser disponibilizada na versão em português, quando implementada e validada.

## 9. Fontes científicas

As experiências devem apresentar suas fontes, períodos, unidades, métodos e limitações.

Referências iniciais:

- NASA Earth Information Center: https://science.nasa.gov/earth/earth-information-center/
- NASA Scientific Visualization Studio: https://svs.gsfc.nasa.gov/
- NASA GISS: https://data.giss.nasa.gov/gistemp/
- NASA FIRMS: https://firms.modaps.eosdis.nasa.gov/

As fontes utilizadas em cada experiência devem ser documentadas individualmente. Não se deve apresentar uma sonificação artística como se fosse uma relação física natural entre o fenômeno e o som.

## 10. Colaboração

O EARTHSONIC é um projeto colaborativo.

Para contribuir:

1. Clone o repositório.
2. Instale as dependências.
3. Execute o projeto localmente.
4. Analise a estrutura dos arquivos.
5. Identifique problemas e melhorias.
6. Faça alterações em conjunto com a equipe.
7. Teste antes de enviar suas modificações.

Antes de começar a editar, sincronize sua cópia com a versão mais recente do GitHub.

Evite que duas pessoas alterem simultaneamente os mesmos arquivos sem combinar previamente.

## 11. Observações importantes

- Os dados científicos devem manter suas fontes e referências.
- Não inventar valores ou resultados.
- Não afirmar que o projeto possui parceria ou aprovação oficial da NASA.
- Recursos ainda não implementados devem ser identificados como planejados.
- Funcionalidades que não foram testadas não devem ser apresentadas como concluídas.

---

**DATA BEAT**  
*EARTHSONIC — Hear the changes of our planet.*
