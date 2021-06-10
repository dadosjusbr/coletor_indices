# Índice - DadosJusBr

## Objetivo

O projeto DadosJusBR tem como principal objetivo denunciar as dificuldades que os cidadãos e organizações têm para acessar a folha de pagamento dos órgãos do sistema de justiça (MPs e TJs). Além disso, o projeto também coleta, valida e consolida essa informação, provendo acesso em formato aberto e de forma amigável a humanos e sistemas computacionais. 

## Problema
Atualmente o dadosjusbr.org provê uma infraestrutura de software para coleta, consolidação, validação e publicação das folhas de pagamento dos órgãos do sistema de justiça. Essa é apenas uma parte da missão do projeto, que também prevê a denúncia de órgãos que dificultam o acesso à folha de pagamento, tanto para humanos, quanto para sistemas computacionais.
Mas como comparar essa falta de transparência, analisando e (potencialmente) denunciando dezenas de órgãos que compõem o sistema de justiça? Fazer isso de forma automatizada é o problema que o índice pretende solucionar.

## Metodologia

O Índice de Transparência do DadosJusBr é um indicador sintético composto por duas dimensões: Completude e Facilidade. Inicialmente calcularemos dois índices, um para cada uma das dimensões.

Cada dimensão é constituída por subdimensões que agregam um conjunto de aspectos avaliados separadamente. O Índice é representado em uma escala de 0 a 100, em que 0 representa o ente menos transparente e 100, o mais transparente.

A coleta dos dados para cálculo do índice é correspondente a um único mês de um determinado órgão. Dessa forma, cada mês possui seu próprio índice, sendo possível acompanhar como se comporta a publicação dos dados no decorrer dos meses.

### Critérios de avaliação

Completude: aqui serão agrupadas métricas relacionadas a disponibilidade dos dados.
Facilidade: aqui serão agrupadas métricas relacionadas a facilidade para acessar os dados que estão disponíveis de forma automatizada.


### Completude

* Lotação:  local onde o servidor exerce as atribuições e responsabilidades do cargo público. Esse critério receberá 0 caso a planilha não apresente esse campo; 0.5 caso alguns funcionários não apresentem essa informação; 1 se todos os funcionários apresentam o campo lotação preenchido.

* Cargo: função que se exerce numa organização. Esse critério receberá 0 caso a planilha não apresente esse campo; 0.5 caso alguns funcionários não apresentem essa informação; 1 se todos os funcionários apresentam o campo lotação preenchido. 

* Remuneração básica:  para os Ministérios Públicos o valor da remuneração básica é composto pela soma do valor  da remuneração do Cargo Efetivo e o valor correspondente a outras verbas remuneratórias, legais ou judiciais. Já para o CNJ esse valor é o correspondente ao subsídio que é exclusivamente de parcela única, vedado o acréscimo de qualquer gratificação, adicional, abono, prêmio, verba de representação ou outra espécie remuneratória, de qualquer origem. Esse critério receberá 0 caso não informe a remuneração básica e 1 caso contrário.

* Detalhamento de Remuneração Eventual ou Temporária: valor correspondente a gratificações temporárias, como: Função de Confiança ou Cargo em Comissão, Gratificação Natalina, Férias Constitucionais, Abono Permanência, Insalubridade. Esse critério receberá 0 caso a planilha não apresente esse campo, 0.5 caso só apresente o valor total e 1 caso detalhe a distribuição do valor total.

* Detalhamento de Indenizações: valor correspondente a pecúnias ou auxílios como: alimentação, saúde, creche, moradia, natalidade. Esse critério receberá 0 caso a planilha não apresente esse campo, 0.5 caso só apresente o valor total e 1 caso detalhe a distribuição do valor total.

* Detalhamento de Descontos:  valor correspondentes a descontos obrigatórios como: Contribuição Previdenciária, Imposto de Renda e Retenção por Teto Constitucional. Esse critério receberá 0 caso a planilha não apresente esse campo, 0.5 caso só apresente o valor total e 1 caso detalhe a distribuição do valor total.


### Facilidade


* Necessário Login: a necessidade de fornecimento de informações pessoais para acesso dos dados. Esse critério receberá 1 caso não seja necessário fazer login e 0 caso contrário.

* Necessário Captcha: verificação se o acesso está sendo feito por humanos. Caso haja essa verificação,  esse critério receberá 0 e caso não, receberá 1.

* Disponibiliza dados para download: oferece os dados em formato pronto para download (csv, json, odf, entre outros). Esse critério receberá 1 caso disponibilize e 0 caso contrário.

* Disponibiliza dados em formato aberto: dados no formato tabular é ideal que sejam publicados em formatos abertos como CSV ou ODS pois  facilita-se o acesso por parte de pessoas que não utilizam softwares de edição de planilhas fechados e/ou pagos. Esse critério receberá 1 caso os dados estejam disponibilizados em formato aberto, 0 caso contrário.

* Disponibiliza API para download dos dados: facilita o processo de automatização. Caso apresente API esse critério receberá 1 e caso não, receberá 0.

* Manteve consistência no formato Esse campo captura se houve mudanças no formato como os dados foram disponibilizados. Caso exista alguma mudança esse critério pontuará 1, caso contrário, receberá 0.

* O site permite scraping para acesso aos dados? Quando não permite scraping é necessário utilizar outras ferramentas para simular um usuário (como por exemplo webdriver), aumentando a complexidade do processo de automatização. Esse critério pontuará 1 caso permita scraping e caso contrário, 0.

* URL segue boas práticas: para nosso contexto se é permanente, tem caminho que conseguimos construir por máquina para os diferentes meses. Caso siga boas práticas pontuará 1, caso contrário 0.

### Cálculo do índice

índice = (Completude | Facilidade / Somatório dos pontos possíveis) x 100 

[Exemplo do cálculo do índice](https://docs.google.com/spreadsheets/d/1QeemKTNJGZHIiCaTnvCavR-tRYSeji9nBoM9ARvjwgQ/edit#gid=1445671395)

