# Estudos .Net Core
Comandos:

- dotnet --help => Mostra os coamandos de ajuda do .Net
- dotnet --version => Mostra a versão atual do .Net instalado no PC
- dotnet --info => Mostra informações sobre o .Net que está seno usado
- dotnet new console -n NOME_DA_PASTA => Cria um novo projeto do tipo console
- dotnet restore => Restaura os pacotes
- dotnet build => Restaura os pacotes e pega o código fonte e realiza o processo de compilação
- dotnet run => Comando para rodar os projetos

### 1 - Oque é e como funciona o .Net

- Compilador do C# é o __Roslyn__ 
- O código fonto escrito em C# é compilado em uma **linguagem intermadiária** __(IL)__
- O código e os recursos de **(IL)** são armazenados no disco em um arquivo executável chamado assembly, geralmente com uma extensão **.exe** ou **.dll** 
- Quando o programa C# é executado, o assembly é carregado no CLR, em seguida o CLR executará a compilção ***just in time (JIT)*** para converter o código IL em instruções de máquina nativas
- CLR fornece também outros serviços:
  - Garbage Collector => é um processo usado para a automação do gerenciamento de memória. Com ele é possível recuperar uma área de memória inutilizada por um programa, o que pode evitar problemas de vazamento de memória, resultando no esgotamento da memória livre para alocação.
  - Exception Handler => é o processo de responder à ocorrência de *exceções* - condições anômalas ou excepcionais que requerem processamento especial - durante a execução de um programa.
  - Resources Manager => Gerenciador de recursos
- Como Funciona:
  - Arquivo C# > Compilador Roslyn > Managed Assembly DLL ou EXE > CLR / .Net Class Libraries > Linguagem de máquina
- Estruturas de programa:
  - programas
    - Consistem em um ou mais arquivos
  - namespaces
    - Declaram tipos, que contem membros e podem ser organizados em namespaces
  - tipos
    - Classes e interfaces são exemplos de tipos
  - membros
    - Campos, métodos, propriedades e eventos são exemplos de membros
  - assemblies

### 2 - Conhecendo variáveis e instruções

#### Tipos Valor:

- Numéricos - **byte, short, int, long, sbyte, ushort, uint, ulong**
- Caracteres Unicode - **char**
- Pontos flutuantes - **float, double, decimal**
- Booleano - **bool**

#### Tipos de referência:

- Tipos Classe - **class, object, string**
- Tipos Arrays - **int[], int[,], etc...**
- interface, delegate

#### Instruções:

- { Bloco de instruções entre as chaves }
- Condicionais
  - if
  - switch
- Repetição
  - while
  - do
  - for
  - foreach
- Outras que nos auxiliam
  - break
  - continue
  - return
  - throw
  - try .. catch .. finally
  - using

### 3 - Classes e objetos essenciais em C#

#### O que são Classes e Objetos em C#:

- Classes são os tipos mais fundamentais de C#
- Uma Classe **é uma estrutura de dados que combina estado(campos) e ações(métodos)**
- Objetos são **instâncias** de uma classe
- As classes suportam **herança e polimorfismo**
- A memória de um objeto é recuperada automaticamente quando o objeto não está mais acessível
- Membros de uma classe podem ser estáticos ou membros de instância 
- Membros estáticos pertecem a classe e membros de instância pertencem ao objeto
- Constantes, variáveis, métodos, propriedades, construtores e etc...
- Cada membro de uma classe tem uma acessibilidades associada, que controla as regiões do texto do programa que podem acessar o membro
  - public
  - protect
  - internal
  - private
- Herança
  - Uma declaração de classe pode especiificar uma classe base, herddando os membros public, internal e protected da classe base
  - Omitir uma especificação de classe base é o mesmo que derivar do tipo object
- Método
  - Método é um membro que implementa uma computação ou ação que pode ser executada por um objeto ou classe
  - Os métodos podem ter uma lista de parâmetros, que representam valores ou referências de variáveis passados para o método, e um tipo de retorno, que especifica o tipo do valor calculado e retornado pelo método

### 4 - Trabalhando com structs, interfaces e enums

#### O que são Structs:

- Como as classes, **as structs são estruturas de dados que podem conter membros de dados e membros de ação**, mas, diferentemente das classes, **as structs são tipos de valor e não requerem alocação de heap**
- Uma **variável de um tipo de struct** armazena diretamente os dados da estrutura, enquanto uma **variável de um tipo de classe** armazena uma referência a um objeto alocado na memória
- Structs **não aceitam herança determinada pelo desenvolvedor**
- São úteis para **pequenas estruturas de dados que possuem semântica de valor** : números complexos, pontos em um sistema de coordenadas ou pares de chave-valor em um dicionárioi são bons exemplosdded utilização
- O uso de structs em vez de classes para pequenas estruturas de dados pode fazer uma grande diferença no número de alocação de memória
- Construtores de structs são chamados com o operador new, semelhante a um construtor de classe, mas em vez de alocar dinamicamente um objeto no heap gerenciado e retornar uma referência a ele, um construtor struct simplesmente retorna o próprio valor struct (normalmente em um local temporário na stack), e esse valor é copiado conforme necessário

#### Entendendo a função de interfaces e enums:

#### Interfaces

- Uma interface **define um contrato que pode ser implementado por classes e structs**
- Um interfaace **pode conter métodos, propriedades, eventos e indexadores**
- Uma interface **não fornece implementações dos membros que define** - apenas suas "assinaturas"
- As interfaces **podem empregar herança multipla**

#### Enuns

- É um tipo de valor distinto com um conjunto de constantes nomeadas
- Você define enumerações quando precisa definir um tipo que pode ter um conjunto de valores discretos. Eles usam um dos tipos de valor integral como armazenamento subjacente. Eles fornecem significadosemântico aos valores discretos
- Cada tipo de enum possui um tipo integral correspondente chamado tipo subjacente do tipo enum
- Um tipo de enumeração que não declara explicitamente um tipo subjacente tem um tipo subjacente ***int***





