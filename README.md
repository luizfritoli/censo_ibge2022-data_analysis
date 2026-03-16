# *Análise exploratória com dados do Censo 2022*

Análise exploratória sobre características da população brasileira, utilizando dados
fornecidos pelo IBGE no Censo 2022, foram feitos tratamento e análise.

Todos os dados completos em: https://censo2022.ibge.gov.br/panorama/?localidade=BR. 

   -> 
   
   -> 
   
   -> 

## *Stack*
- R;
- RMarkdown;
- Tidyverse;
- Scales.

## *Objetivos*

- Realizar análise sobre características da população com base no Censo 2022;
- Gerar conclusões com as informações obtidas;
- Documentar passos, conclusões e considerações;
- Apresentar o conhecimento adquirido usando dashboards.

## *Execução*

- Clonagem do repositório;
- Executar `scripts/analysis.Rmd`.

## *Estrutura*

- `data/original`: Dados originais..
- `scripts/analysis.Rmd`: Script responsável pela análise dos dados usando gráficos e tabelas.

## *Considerações do tratamento dos dados*

1. **Os dados vieram em ótimo estado**
   Por se tratar do IBGE, o principal provedor de informações geográficas e estatísticas do
   Brasil, os dados vieram muito bem formatados e claros, o que favorecerá a análise.

   Foram feitas verificações iniciais de estrutura, tipagem e consistência para garantir a
   confiabilidade. 

## *Considerações da análise dos dados*

1. **Nomes mais populares**

   Dentre os 10 nomes mais populares do Brasil, todos são nomes de origem religiosa. Então,
   mesmo que o Brasil seja um país declaradamente laico, é notável a forte influência cristã
   na cultura brasileira. É importante mencionar que os nomes nem sempre têm uso exclusivamente
   religioso.

   O nome mais popular do Brasil é `Maria`, muito comum por causa da devoção à Maria no catolicismo.
   Isso é explicado pelo fato do Brasil ter sido colonizado por Portugal, que por séculos teve a Igreja
   Católica como forte influência, o que também atingiu o Brasil.

   É válido comentar que dentre os 10 nomes mais populares, há uma concentração masculina com 8 nomes,
   contra 2 nomes femininos (os nomes femininos são mais variados?). 
