# Prompt:
```
 
Tens o endpoint https://baze.cm-maia.pt/BaZe/api/x4rt.php 
1. Descreve o que o endpoint representa
2. Identifica variáveis principais
3. Analisa tendências ao longo do tempo
4. Detecta anomalias ou valores estranhos
5. Sugere possíveis interpretações
6. Lista limitações dos dados
7. Indica o que falta fazer para os endpoints serem mais explicativos / autoexplicativos
Responde de forma estruturada.

```

## Claude

### Resposta
[https://claude.ai/share/405c4250-32eb-4e2a-aaf4-62127a8ea4e5](https://claude.ai/share/405c4250-32eb-4e2a-aaf4-62127a8ea4e5)

## ChatGPT

### Resposta
[https://chatgpt.com/share/69e67539-4968-8332-8bef-c1f01fb3230b](https://chatgpt.com/share/69e67539-4968-8332-8bef-c1f01fb3230b)

## Deepseek

### Resposta
[https://chat.deepseek.com/share/t6zkx26js4byqh9rgh](https://chat.deepseek.com/share/t6zkx26js4byqh9rgh)

## Perplexity

### Resposta
[https://www.perplexity.ai/search/tens-o-endpoint-https-baze-cm-4BlTQdOcRMaFrOuaYBPbog](https://www.perplexity.ai/search/tens-o-endpoint-https-baze-cm-4BlTQdOcRMaFrOuaYBPbog)

## Copilot

### Resposta
[https://copilot.microsoft.com/conversations/join/ro72GV2PsxUHMrXJ2NGnU](https://copilot.microsoft.com/conversations/join/ro72GV2PsxUHMrXJ2NGnU)

## Gemini

### Resposta
[https://gemini.google.com/share/2fd8bdbac4ef](https://gemini.google.com/share/2fd8bdbac4ef)

# Análise/Síntese

### Claude

Mostra alguma informação sobre os passos que realizou para obter a resposta.

Neste caso, o LLM tentou analisar um conjunto de endpoints para obter a resposta. Dois deles são iguais aos exemplos que aparecem no json retornado pelo endpoint, os outros, alguns falharam e não sei onde os foi buscar (mas existem). Não sei por que razão escolheu estes urls. Alguns estavam nos exemplos, mas o LLM não chamou (usou) outros que também estavam nos exemplos.

O LLM também apresenta uma imagem onde separa as séries em 3 categorias.

Não apresenta mais fontes ou referências diretas e explícitas.

Nas variáveis principais identificadas, apresenta alguns dos sensores. Com mais detalhe os que chamou com sucesso nos endpoints usados para obter a resposta: meteo1 e airq1. 

Nas tendências ao longo do tempo, o LLM refere o ssql=True e o ORDER BY id DESC LIMIT 1 que deve ter visto numa das chamadas que fez. Penso que usa mais info do json para inferir informação acerca de outras séries (sensores). Refere-se ao valor de td, recebido nas respostas e ao seu valor pequeno. Indica que seria necessário usar o tstart/tend quando disponível, para obter tendências.

Nas anomalias e valores estranhos, analisou a resposta dos dois endpoints, que chamou automaticamente para obter a resposta. Queixa-se de vários valores.

Nas possíveis interpretações, faz uma análise com algumas suposições. O que parece natural, se não existir informação clara disponível.

Nas limitações dos dados, o LLM apresenta várias limitações.

No que falta para os endpoints serem mais explicativos/auto-explicativos, o LLM apresenta várias sugestões de melhoria.

Em comparação com os outros endpoints (outras duas experiências, a-1 e a-2), a resposta parece ser mais detalhada e o LLM chamou vários endpoints de dados a partir do endpoint apresentado no prompt. Fiz esta experiência no fim, por isso não sei se o LLM se começou a adaptar ao meu perfil ou se é da estrutura do json (que me parece muito semelhante ao dos outros endpoints).
De qualquer das formas, o comportamento do LLM apresenta algumas diferenças que me parecem importantes e significativas.

### ChatGPT

Apresenta sources e algumas referências explícitas no texto.

O LLM indica que analisou informação pública disponível em torno do endpoint https://baze.cm-maia.pt/BaZe/api/x4rt.php e das páginas do ecossistema BaZe da Câmara Municipal da Maia. Como o endpoint em si não expõe documentação direta no resultado pesquisável, a análise é inferencial, baseada nas páginas que o referenciam (apresentado pelo LLM). Ou seja, não analisou o que o endpoint retorna, o que coloca algumas limitações na análise apresentada.

Indica que, o endpoint x4rt.php aparenta ser uma API REST interna / catálogo de dados operacionais do projeto BaZe (Balanço Zero de Carbono) da Câmara Municipal da Maia.
O endpoint x4rt.php parece ser o ponto central de acesso programático aos datasets em tempo real e históricos usados nos dashboards públicos do portal BaZe.

Apresenta sobretudo suposições.

Nas variáveis principais identificadas, o LLM apresenta alguma informação com o que encontrou publicamente e algumas suposições (por falta de informação). Algumas suposições parecem estar corretas.

Nas tendências ao longo do tempo, fala em tendências observáveis no ecossistema BaZe e sem acesso direto ao output bruto do endpoint, só é possível inferir tendências a partir dos dashboards públicos. Não mostra informação concreta.

Nas anomalias ou valores estranhos detectáveis, diz que as próprias páginas públicas já admitem anomalias e apresenta esses exemplos. Também apresenta anomalias que podem aparecer neste tipo de endpoints.

Nas possíveis interpretações, apresenta uma visão técnica, uma espécie de camadas, visão estratégica e institucional.

Nas limitações dos dados, apresenta alguns, muito high-level, muito genérico (não analisou o payload retornado pelo endpoint).

No que falta para os endpoints serem auto explicativos, apresenta várias sugestões.

Resposta longa, talvez das mais longas, mas com pouca informação concreta acerca do endpoint.

Aparentemente, o LLM é capaz de consultar outros urls, mas estes 3 (experiências a-1, a-2 e a-3), aparentemente, não. Parece pouco útil para este tipo de tarefa.

### DeepSeek

Não apresenta passos, fontes e referências.

Parece conseguir ler o json retornado pelo endpoint.

Parece perceber do que se trata. 

Divide os sensores em áreas.

Nas variáveis principais, apresenta uma tabela com tipo de sensor, id e descrição e também apresenta os parâmetros adicionais. Mostra este param: &estimates=True - mostra estimativas (depende do sensor), que não vi diretamente no json (pode-me ter escapado).

Na análise de tendências ao longo do tempo. indica que a API não retorna dados históricos completos de imediato, apenas o último valor ou um intervalo restrito. Apresenta algumas afirmações com base na documentação, que não identifica de uma forma clara e concreta.

Nas anomalias ou valores estranhos, fala em possíveis anomalias a detetar uma vez que os dados não foram observados.

Nas possíveis interpretações, apresenta possíveis análises dos dados para obter informação acerca de determinados aspectos. Fala em cruzar dados para fazer determinadas análises.

Nas limitações dos dados, apresenta uma tabela com várias limitações.

No que falta fazer para os endpoints serem mais explicativos, apresenta várias sugestões.

Uma das questões com o Deep é que não apresenta fontes nem referências explicitamente. Diria que é um dos LLMs que apresenta resultados mais interessantes, juntamente com o Claude.

### Perplexity

Apresenta alguma informação acerca dos passos usados para obter a resposta. Apresenta referências no texto e fontes.

Consultou fontes externas, mas não é claro se analisou o json retornado pelo endpoint. Parece-me que não.

Afirma que … um catálogo/base de acesso aos dados usados nas páginas de monitorização do PT Torre. Isto é uma simplificação da realidade, digo eu.

Mais à frente aparece: o endpoint parece ser a camada de exposição dos dados brutos/estruturados de um sistema de monitorização elétrica local, ligado ao PT Torre do Lidador e aos consumos associados ao complexo municipal da Maia. O que para mim não é absolutamente claro e correto.

Nas variáveis principais, penso que se foca muito na torre do lidador que deve ter sido uma das fontes que encontrou (https://baze.cm-maia.pt/BaZe/PTTorre.htm).

Nas tendências ao longo do tempo, refere as que aparecem no texto de referência (PTTorre) como padrões esperados.

Nas anomalias ou valores estranhos, refere-se às da página PTTorre.

Nas possíveis interpretações, apresenta suposições.

Nas limitações dos dados, apresenta várias com referência a PTTorre.

No que falta para ser auto explicativo, apresenta várias sugestões, high level, muito genéricas.

Apresenta o seguinte: Falta, прежде de mais, uma especificação formal do endpoint …

Pede para enviar o payload da resposta do endpoint para análise.

Não apresenta informação concreta baseada no que o endpoint retorna. 

A resposta é pouco fiável e útil. Ao nível do chatGPT ou inferior.

### Copilot

Não mostra passos, fontes ou referências. Parece perceber o que o endpoint representa.

Nas variáveis principais, apresenta os parâmetros disponibilizados, com uma descrição de cada um e separa os sensores por categorias.

Nas tendências ao longo do tempo, apresenta inferências com base no tipos (tipologia) dos dados. Não indica a quantidade de dados retornada por omissão, como faz se não me engano o Claude, ou o Deep.

Nas anomalias ou valores estranhos, apresenta suposições de anomalias esperadas com base no tipo de sensor.

Nas possíveis interpretações, apresenta as utilizações possíveis do endpoint.

Nas limitações dos dados, apresenta algumas, por alto (sem referir o json que o endpoint retorna, diretamente).

No que falta para os endpoints serem mais explicativos, apresenta algumas sugestões que parecem mais genéricas.

Resposta com pouco detalhe. Aparentemente teve acesso ao json retornado pelo endpoint. Penso que este LLM é o 3 mais útil entre os 6. Os mais úteis são o Claude e o Deep.

### Gemini

Não mostra passos, fontes ou referências. 

Parece conseguir perceber o que o endpoint representa.

Nas variáveis principais, diz que o endpoint é parametrizável e mostra o id, depois fala em Identificadores: device_id (nome do sensor), timestamp ou date (momento da leitura). e apresenta outras coisas, por exemplo: Mobilidade: Lat, Lng (coordenadas GPS para trackers), Battery (estado da bateria do sensor). Não sei onde foi buscar esta informação.

Nas tendências ao longo do tempo, fala em coisas genéricas, que não sei de onde vêm, por exemplo, sazonalidade e ciclos circadianos.

Nas anomalias e Valores Estranhos, fala em coisas que é comum encontrar neste tipo de endpoints.

Nas possíveis interpretações, apresenta conclusões que me parecem pouco plausíveis e que não sei que base/fundamentação têm.

Nas limitações dos Dados, apresenta algumas, mas penso que não considerou o payload que o endpoint retorna.

Nas sugestões de melhoria, apresenta várias de forma genérica.

Nestas experiências, a-1, a-2 e a-3, o Gemini, o Perplexity e o ChatGPT, por esta ordem, parecem ser os LLMs mais inúteis para serem usados neste tipo de tarefa. Não sei se esta situação poderia melhorar com prompts diferentes.

# Conclusões

Mais interessante: Claude, Deep, Copilot, Chat GPT, Perplexity e Gemini.

O Gemini parece pouco útil. 

O Deep apresenta as coisas com algum detalhe, mas não apresenta fontes e referências, o que me parece cada vez mais essencial para garantir transparência e rastreabilidade.
