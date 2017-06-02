# SO---exerc-cios-Aula-14-

# 1) Quais são as 3 camadas de hierarquia de memória?

  inboard memory ( registers, cache )
  Outboard Storage (cd)
  Off-line Storage (Magnetic Tape)
  
# 2) Como é feita a aplicação do princípio da localidade em uma memória organizada de forma hierárquica?

  A hierarquia baseia-se no princípio da localidade: durante a execução de um programa, as referências à memória realizadas por uma UCP, tanto para instruções como para dados, tendem a se aglutinar.
  
  Exemplos:
     Um laço de repetição em um programa que executa repetidamente um mesmo grupo de instruções.
     A utilização de uma estrutura de dados, como por exemplo um arranjo, onde todos os acessos aos dados ocorrem na mesma localidade da memória.

# 3) No que consiste a memória virtual?
    
   Espaço de endereçamento virtual.
    
# 4) Qual é a função do registrador de base no gerenciamento de memória?

   Quando um programa é carregado na memória, o endereço do início do programa na memória física é armazenado no registrador de base (base register).
    
    Em todo acesso à memória, o endereço lógico indicado pelo programa é adicionado ao conteúdo do base register, resultando no endereço físico real da posição de memória a ser acessada.
    
# 5) No que consiste a segmentação da memória?

  Um programa é dividido em vários segmentos.
  Cada segmento é alocado na memória física e recebe registradores de base e tamanho.
  Todo acesso do programa à memória é identificado pelo número do segmento e pelo of set.

# 6) Qual é o papel dos device drivers?

  Os controladores (device drivers)asdasdasdasretamente com os dispositivos.
  São estruturas de dados e procedimentos, e conhecem os detalhes de hardware de um dispositivo.
  
# 7) O que é o descritor de um arquivo?

  O descritor é um índice (que começa a contagem com o valor 0) desta tabela, utilizado pela aplicação para identificar a stream ao realizar uma operação.
  
# 8) Qual é a solução adotada pela técnica de buf ering?

  Uma solução é agrupar as operações em um lote e realizar a transferência física em uma única vez.
  Esta técnica é conhecida como buf ering.

# 9) O que é gravado no bloco de boot de um disco?

  Contém o programa de bootstrap (programa executado automaticamente logo que a máquina é ligada.
  No bloco de boot há informação de cada partição (início, fim e tipo de sistema de arquivo).
  
# 10) Qual é a dificuldade que pode ser encontrada na alocação contígua de um disco?

  Uma dificuldade nesta forma de organização é encontrar um espaço grande o suficiente para acomodar um novo arquivo.
  
# 11) Como é feita a organização de um disco através de blocos ligados?

  Cada arquivo ocupa blocos que não precisam ser contíguos.
  A entrada do arquivo no diretório de arquivos contém o endereço do primeiro bloco do arquivo.
  Cada bloco tem um ponteiro para o próximo bloco.
  O último bloco tem um ponteiro para NULL.
  
# 12) Cite 3 exemplos de sistemas de arquivos.

  Microsoft FAT32
  Microsoft NTFS
  Linux EXT2
  
# 13) Quais são as 3 categorias de softwares de virtualização?

  Hypervisor: o software apresenta às camadas superiores um hardware abstrato, similar ao original. Exemplos: VMWare ESX, Xen, Hyper-V.

  Contâiner: o software é executado a partir de um sistema operacional convencional. Cria partições lógicas, onde cada partição é vista como uma máquina isolada, compartilhando o mesmo sistema operacional.
Exemplos: Docker

  Plataforma virtual para aplicações: define uma máquina abstrata sobre a qual são executadas aplicações desenvolvidas em uma linguagem de alto nível. Exemplo: a máquina virtual Java.


# 14) Quais são os 2 tipos de hypervisors e quais são as características de cada tipo?

  Tipo I (baremetal, nativo ou supervisor): executa diretamente no hardware do servidor. Controla o hardware e o acesso do sistema
operacional convidado (guest). O papel do hypervisor nativo é compartilhar os recursos de hardware entre as máquinas virtuais, de
forma que cada uma delas imagine ter os recursos exclusivos para si.
Exemplos: VMWare ESX Server, Microsoft Hyper-V e Xen Server.


Tipo II (hosted): aplicação que fornece um ambiente de execução para outras aplicações. É executado sobre um sistema operacional como se
fosse um processo deste. A camada de virtualização é composta por um hardware virtual e um sistema operacional hóspede (guest). Exemplos: VMWare Player, VirtualBox e Virtual PC.
