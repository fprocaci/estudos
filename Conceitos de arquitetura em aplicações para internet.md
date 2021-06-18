# Arquitetura de Sistemas

###### **Introdução a Arquitetura de Sistemas (Objetivos da Aula)**

###### - Tipos de arquitetura.

###### - Comparativo entre os tipos de arquitetura.

###### - Gerenciamento de erros e volume de acesso.

######  

###### **Requisitos Básicos**

###### - Conhecimento básico sobre protocolo HTTP e Proxy.

###### - Entendimento sobre RestAPI.

###### - Conhecimento sobre Docker.

###### - Saber programar.

######  

###### **Tipos de arquitetura**

###### - Monolito, Microserviços (Vários Modelos)

######  

###### **Comparando os modelos Monolito e Microserviços (Objetivo da Aula)**

###### **Monolito**

###### - **Pros -** Baixa complexidade, Monitoramento simplificado.

###### - **Contras -** Stack única, Compartilhamento de recursos, Acoplamento, Mais complexo a escalabilidade.

######  

###### **Microserviços 1**

###### - **Pros -** Stack dinâmica, Simples escalabilidade.

###### - **Contras -** Acoplamento, Monitoramento mais complexo, Provisionamento mais complexo.

######  

###### **Microserviços 2**

###### - **Pros -** Stack dinâmica, Simples escalabilidade, Desacoplamento.

###### - **Contras -** Monitoramento mais complexo, Provisionamento mais complexo **.**

######  

###### **Microserviços 3**

###### - **Pros -** Stack dinâmica, Simples escalabilidade, Desacoplamento, Menor complexidade.

###### - **Contras -** Provisionamento mais complexo, Plataforma inteira depende do gerenciador de pipeline.

######  

###### **Gerenciamento de erros e volume de acesso (Objetivos da Aula)**

###### **Gerenciamento de erros**

###### Onde é mais complexo:

###### - Processos assíncronos (Microsserviços 2)

###### - Pipeline

###### Solução:

###### - Dead letter queue

###### - Filas de re-tentativas

modificado

