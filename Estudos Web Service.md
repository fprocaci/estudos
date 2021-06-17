1. **Web Service**

   - URI
   - Serviços Web são API`s  mas não o contrario
     - Comunicação feita pelo protocolo HTTP
   - Vantagens:
     - Linguagem comum
     - Integração
     - Reutilização
     - Segurança
     - Custos
   - Principais Tecnologias
     - SOAP
     - REST
     - XML
     - JSON

   

   1.1 **SOAP** - Simple Object Access Protocol

   - ë um protocolo baseado em XML para acessar serviços web principalmente por http.
   - Define como os serviços web se comunicam
   - Facilita integrações e aplicações

   - Vantagens: 
     - Permite integrações entre aplicações
     - É independente de plataforma e software
     - Meio de transporte genérico, pode ser usado por outros protocolos além do HTTP.
   - Estrutura SOAP:
     - SOAP Envelope>SOAP Header>SOAP Body
     - SOAP Envelope - É o primeiro elemento, é usado para encapsular toda a mensagem SOAP
     - SOAP Header - é o elemento onde possui informações de atributos e metadados da requisição.
     - SOAP Body é o elemento que contém os detalhes da mensagem

   1.2 **XML** - Extensible Markup Language

   - É uma linguagem de marcação da década de 90
   - Facilita a separação de conteúdos
   - Não tem limitação de criação
   - Linguagem comum para integrações entre aplicações

   1.3 **WSDL** Web Services Descripton Language
   
   - Usado para descrever Web Services, funciona como um contato do serviço.
   - A descrição é feito em um documento XML, onde é descrito o serviço, especificações de acesso, operações e métodos.
   
   1.4 **XSD**  - XML Schema Definition
   
   - É um schema no formato XML usado para definir a estrutura de dados que será validada no XML.
   - O XSD funciona como uma documentação de como deve ser montado o SOAP Message (XML)  que será enviado através de Web Service.
   
   1.5 **REST** - Representational State Transfer
   
   - Ë um estilo de arquitetura de software que define a implementação de serviço WEB.
   - Pode trabalhar com os formatos XML, JSON ou outros.
   - Vantagens:
     - Permite integrações entre aplicações e também entre cliente e  servidor em páginas web e aplicações
     - Utiliza dos métodos HTTP
     - Arquitetura de fácil compreensão
   - API - Application Programming Interface
     - Conjunto de rotinas documentados para que outras aplicações possam consumir suas funcionalidades
   
   1.6 **JSON** - JavaScript Object Notation
   
   - Formatação leve utiliza para troca de mensagens entre sistemas
   - Usa uma estrutura de chave e valor e também de listas ordenadas
   
   1.7 **Principais métodos HTTP** 
   
   - GET - Solicita a representação de um recurso
   - POST - Solicita a criação de um recurso
   - DELE - Solicita a exclusão de um recurso
   - PUT - Solicita a atualização de um recurso
   
   

