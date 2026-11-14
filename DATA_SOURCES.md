# DATA_SOURCES — EARTHSONIC (DATA BEAT)
Projeto independente, sem endosso da NASA. Campos "Não verificado" precisam ser conferidos pela equipe. Nenhum dado deste repositório foi inventado.
A relação de cada visualização com o NASA Earth Information Center (EIC) vem do briefing do projeto e **ainda não foi verificada na galeria**.

## 1. Climate — Climate Spiral
| Campo | Valor |
|---|---|
| Visualização NASA / ID SVS | NASA Climate Spiral, SVS 5057 (1880–2022); versão mais recente SVS 5190 |
| Relação com o EIC | Não verificado (citada como item do Main Dashboard) |
| Dataset original | NASA GISS GISTEMP v4, Global-mean monthly Land-Ocean Temperature Index |
| URL | https://data.giss.nasa.gov/gistemp/tabledata_v4/GLB.Ts+dSST.csv · https://data.giss.nasa.gov/gistemp/ |
| Variável / unidade | Anomalia de temperatura, °C |
| Linha de base | 1951–1980 |
| Período | 5057: 1880–2022 (o site limita os dados a esse intervalo). 5190: atualizada ~2 semanas após cada mês |
| Atualização | Mensal |
| Acesso | CSV público. Cópia local: `npm.cmd run update-data` → `public/data/climate/` (CSV, metadata.json com URL, data, SHA-256) |
| Chave de API | Não |
| Data de obtenção | Registrada em `public/data/climate/metadata.json` quando você roda o script (nenhum arquivo foi baixado na construção deste pacote) |
| Créditos | NASA GISS; NASA Scientific Visualization Studio |
| Limitações | Média global esconde diferenças regionais; meses ausentes (`***`) são ignorados, nunca preenchidos |
| Sonificação (escolha da DATA BEAT) | 1 mês = 1 nota senoidal; frequência = 440 × 2^(anomalia/4) Hz; 0 °C = 440 Hz. Não é relação física |

## 2. Wildfires — EM VALIDAÇÃO
| Campo | Valor |
|---|---|
| Visualização NASA / ID SVS | Active Fires (VIIRS), SVS 5113 |
| Relação com o EIC | Não verificado |
| Dataset original | NASA FIRMS, produtos VIIRS_SNPP_NRT e VIIRS_NOAA21_NRT |
| URL | https://firms.modaps.eosdis.nasa.gov/ · https://firms.modaps.eosdis.nasa.gov/api/ |
| Variável / unidade | Detecções e FRP (potência radiativa do fogo), MW |
| Período | Dias recentes (near real time) |
| Atualização | Diária (segundo o briefing; confirmar na documentação do FIRMS) |
| Acesso | API de área, só no servidor (`/api/nasa/fires`), janelas de até 5 dias por requisição |
| Chave de API | **Sim**: MAP_KEY gratuita em `FIRMS_MAP_KEY` (ver `.env.example`). Nunca no navegador |
| Data de obtenção | Registrada em cada resposta (`collectedAt`) e versão do dado (`versions`) |
| Limitações | Área é um retângulo (não divisa de estado); contagem de detecções não mede tamanho nem intensidade; dias sem detecção não são preenchidos; não confirmado se os parâmetros da API (limite de dias, formato) estão atuais |
| Janela temporal | Opção de janela móvel de 5 dias, para se aproximar da visualização 5113 (conferir) |
| Sonificação (escolha da DATA BEAT) | 1 dia = 1 passo; altura (220–880 Hz, escala log no período) = FRP médio; nº de pulsos (1–6) = nº de detecções |
| Para validar | Com a chave, comparar contagens e datas com a visualização 5113 e com o site do FIRMS antes de marcar como Available |

## 3. Oceans — NÃO DISPONÍVEL
SVS 5101 (Sea Surface Temperature, near real time). Dataset, acesso numérico, unidade, resolução e correspondência com a visualização **ainda não identificados**. Não há página nem sonificação. Só marcar Available depois de cumprir os itens do briefing.

## Observações
- SVS API fornece metadados e links de mídia, não os dados numéricos. GIBS fornece imagens/mapas, não dados para sonificação. Não são misturados.
- Os IDs 40529, 40531, 40477, 40479 e 5101 aparecem apenas como referência em Discover Earth ("não verificada").
