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
- Quando o programa C# é executado, o assembly é carregado no CLR, em seguda o CLR executará a compilção ***just in time (JIT)*** para converter o código IL em instruções de máquina nativas
- CLR fornece também outros serviços:
  - Garbage Collector => é um processo usado para a automação do gerenciamento de memória. Com ele é possível recuperar uma área de memória inutilizada por um programa, o que pode evitar problemas de vazamento de memória, resultando no esgotamento da memória livre para alocação.
  - Exception Handler => é o processo de responder à ocorrência de *exceções* - condições anômalas ou excepcionais que requerem processamento especial - durante a execução de um programa.
  - Resources Manager => Gerenciador de recursos
- Como Funciona:
  - Arquivo C# > Compilador Roslyn > Managed Assembly DLL ou EXE > CLR / .Net Class Libraries > Linguagem de máquina
- Estruturas de programa:
  - 



