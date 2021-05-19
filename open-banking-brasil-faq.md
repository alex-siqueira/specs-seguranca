# Pergunta Frequentes

## Quais os níveis de autenticação (LoA - Level of Assurance) exigido pelo Open Banking Brasil?
O ACR (Authentication Context Class Reference) é um parâmetro opcional que é utilizado para enviar informações adicionais sobre o nível de autenticação exigida para o usuário final, sendo especificado através do LoA (Level of Assurance)

Para o Open Banking Brasil são definidos:
* **LoA2:** Autenticação realizada através de fator único
* **LoA3:** Autenticação realizada através de múltiplo fatores (MFA)

Sendo necessário:
* **APIs de Consulta:** Deve ser solicitado ao menos LoA2, podendo a instituição transmissora realizar a critério (de acordo com resoluçõa vigente) executar autenticação usando LoA3.
* **APIs de Escrita (Transacional):** Deve ser solicitado ao menos LoA3.

## Quais os critérios de Múltiplos Fatores de Autenticação?
Considerando que os fatores de autenticação são compostos por métodos:
* Algo que você sabe; como uma senha ou uma frase;
* Algo que você tem; como um token ou um smartcard;
* Algo que você é; como uma validação biométrica.

Para realizar uma autenticação MFA é necessário que o usuário final apresente ao menos dois métodos distintos de autenticação conforme listado acima. Um mesmo método utilizado duas vezes não é aceito como autenticação de múltiplo fator.

## O Open Banking Brasil utiliza JAR/JARM?

JAR (JWT Secured Authorization Request) e JARM (JWT Secured Authorization Response) são suportados pelo Open Banking Brasil Financial-grade API Security Profile 1.0 porém não têm sua implementação exigida.

## É permitido a utilizaçao de PKI Privada para emissão de certificados responsáveis por autenticação (cliente) e assinatura no Open Banking Brasil?

De acordo com a MEDIDA PROVISÓRIA No 2.200-2, DE 24 DE AGOSTO DE 2001 (http://www.planalto.gov.br/ccivil_03/mpv/antigas_2001/2200-2.htm) a utilização de PKI Privada é autorizada como mecanismo válido para autenticação e assinatura.

Para o Open Banking Brasil, a utilização de PKI Privada para emissão de certificados de autenticação (cliente) e assinatura é permitido apenas quando provisionado pela entidade atuando como transmissora de dados, e quando a entidade receptora de dados não participa do Ecossistema do Open Banking Brasil de maneira a não possuir cadastro no Serviço de Diretório do Open Banking Brasil e o **certificado deve possuir as mesmas características de chaves criptográficas e atributos conforme especificado pelo Open Banking Brasil.**

# Reconhecimento

Agradecemos a todos que estabeleceram as bases para o compartilhamento seguro e seguro de dados por meio da formação do Grupo de Trabalho FAPI da OpenID Foundation, o GT-Segurança do Open Banking Brasil e aos pioneiros que ficarão em seus ombros.

As seguintes pessoas contribuíram para este documento:

* Marcos Rodrigues (Itaú)

# Informativo

Copyright (c) 2021 Estrutura Inicial do Open Banking Brasil.

A Estrutura Inicial do Open Banking Brasil (EIOBB) concede a qualquer Colaborador, desenvolvedor, implementador ou outra parte interessada uma licença de direitos autorais mundial não exclusiva, livre de royalties para reproduzir, preparar trabalhos derivados, distribuir, executar e exibir, estes Implementadores Rascunho ou Especificação Final exclusivamente para fins de (i) desenvolver especificações e (ii) implementar Rascunhos de Implementações e Especificações Finais com base em tais documentos, desde que a atribuição seja feita ao EIOBB como a fonte do material, mas que tal atribuição o faça não indica endosso do EIOBB.

A tecnologia descrita nesta especificação foi disponibilizada a partir de contribuições de várias fontes, incluindo membros da OpenID Foundation, do GT-Segurança do Open Banking Brasil e outros. Embora a Estrutura Inicial do Open Banking Brasil tenha tomado medidas para ajudar a garantir que a tecnologia esteja disponível para distribuição, ela não toma posição quanto à validade ou escopo de qualquer propriedade intelectual ou outros direitos que possam ser reivindicados como pertencentes à implementação ou uso do tecnologia descrita nesta especificação ou até que ponto qualquer licença sob tais direitos pode ou não estar disponível; nem representa que fez qualquer esforço independente para identificar tais direitos. A Estrutura Inicial do Open Banking Brasil e os contribuidores desta especificação não oferecem (e por meio deste expressamente se isentam de quaisquer) garantias (expressas, implícitas ou de outra forma), incluindo garantias implícitas de comercialização, não violação, adequação a uma finalidade específica ou título, relacionados a esta especificação, e todo o risco quanto à implementação desta especificação é assumido pelo implementador. A política de Direitos de Propriedade Intelectual do Open Banking Brasil exige que os contribuidores ofereçam uma promessa de patente de não fazer valer certas reivindicações de patentes contra outros contribuidores e implementadores. A Estrutura Inicial do Open Banking Brasil convida qualquer parte interessada a trazer à sua atenção quaisquer direitos autorais, patentes, pedidos de patentes ou outros direitos de propriedade que possam abranger a tecnologia que possa ser necessária para praticar esta especificação.
