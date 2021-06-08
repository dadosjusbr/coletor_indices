# Índice - DadosJusBr

## Objetivo

O projeto DadosJusBR tem como principal objetivo denunciar as dificuldades que os cidadãos e organizações têm para acessar a folha de pagamento dos órgãos do sistema de justiça (MPs e TJs). Além disso, o projeto também coleta, valida e consolida essa informação, provendo acesso em formato aberto e de forma amigável a humanos e sistemas computacionais. 

## Problema
Atualmente o dadosjusbr.org provê uma infraestrutura de software para coleta, consolidação, validação e publicação das folhas de pagamento dos órgãos do sistema de justiça. Essa é apenas uma parte da missão do projeto, que também prevê a denúncia de órgãos que dificultam o acesso à folha de pagamento, tanto para humanos, quanto para sistemas computacionais.
Mas como comparar essa falta de transparência, analisando e (potencialmente) denunciando dezenas de órgãos que compõem o sistema de justiça? Fazer isso de forma automatizada é o problema que o índice pretende solucionar.

## Critérios de avaliação

Completude: aqui serão agrupadas métricas relacionadas a disponibilidade dos dados.
Facilidade: aqui serão agrupadas métricas relacionadas a facilidade para acessar os dados que estão disponíveis de forma automatizada.

### Completude

* Lotação:  local onde o servidor exerce as atribuições e responsabilidades do cargo público.
* Cargo: função que se exerce numa organização. 
* Remuneração básica:  para os Ministérios Públicos o valor da remuneração básica é composto pela soma do valor  da remuneração do Cargo Efetivo e o valor correspondente a outras verbas remuneratórias, legais ou judiciais. Já para o CNJ esse valor é o correspondente ao subsídio que é exclusivamente de parcela única, vedado o acréscimo de qualquer gratificação, adicional, abono, prêmio, verba de representação ou outra espécie remuneratória, de qualquer origem.
* Detalhamento de Remuneração Eventual ou Temporária: valor correspondente a gratificações temporárias, como: Função de Confiança ou Cargo em Comissão, Gratificação Natalina, Férias Constitucionais, Abono Permanência, Insalubridade.
* Detalhamento de Indenizações: valor correspondente a pecúnias ou auxílios como: alimentação, saúde, creche, moradia, natalidade.
* Detalhamento de Descontos:  valor correspondentes a descontos obrigatórios como: Contribuição Previdenciária, Imposto de Renda e Retenção por Teto Constitucional


### Facilidade


* Necessário Login: a necessidade de fornecimento de informações pessoais para acesso dos dados.
* Necessário Captcha: verificação se o acesso está sendo feito por humanos.
Disponibiliza dados para download: oferece os dados em formato pronto para download (csv, json, odf, entre outros).
* Disponibiliza dados em formato aberto: dados no formato tabular é ideal que sejam publicados em formatos abertos como CSV ou ODS pois  facilita-se o acesso por parte de pessoas que não utilizam softwares de edição de planilhas fechados e/ou pagos.
* Disponibiliza API para download dos dados: facilita o processo de automatização.
* Manteve consistência no formato Esse campo captura se houve mudanças no formato como os dados foram disponibilizados.
* O site permite scraping para acesso aos dados? Quando não permite scraping é necessário utilizar outras ferramentas para simular um usuário( como por exemplo webdriver), aumentando a complexidade do processo de automatização.
* URL segue boas práticas: para nosso contexto: se é permanente, tem caminho que conseguimos construir por máquina para os diferentes meses.

## Cálculo do índice

Inicialmente calcularemos dois índices, um para cada dimensão: Completude e dificuldade.
Cada dimensão é constituída por subdimensões que agregam um conjunto de aspectos avaliados separadamente. O Índice é representado em uma escala de 0 a 100, em que 0 representa o ente menos transparente e 100, o mais transparente.

A coleta dos dados para cálculo do índice é correspondente a um único mês de um determinado órgão. Dessa forma, cada mês possui seu próprio índice, sendo possível acompanhar como se comporta a publicação dos dados no decorrer dos meses.

índice = (Completude | Facilidade / Somatório dos pontos possíveis) x 100 


