========Descrição original:

Cada diretório contém arquivos de memória destinados aos respectivos processadores. 
MEM_Instruction deve ser carregado na memória de instruções e MEM_Data na de dados (com exceção do MIPS Monociclo, que possui uma memória para ambos).
Além disso, a versão do processador com pipeline inclui o arquivo de ROM de controle, pois a instrução J não está implementada na versão original.

O programa em assembly é o seguinte:

LW R1, 0(R0)
LW R2, 4(R0)
ADD R3, R1, R2
SUB R3, R3, R2
BEQ R3, R1 LB1
SW R0, 8(R0)
J 0
LB1:
SW R3, 8(R0)
J 0

Ele carrega as duas primeiras posições da memória de dados (no multiciclo, carrega os endereços 40 e 44) em R1 e R2, soma esses registradores e armazena em R3. Em seguida, subtrai R3 de R2 e armazena em R3 e compara R3 com R1. Se os registradores forem iguais (deu tudo certo), pula para LB1 e armazena R3 no endereço 8 (48 no multiciclo), se não, armazena R0 em 8.
O objetivo do programa é testar as operações básicas que já estão implementadas no processador. A sugestão é inserir as instruções novas após o SW R0, 8(R0), pois (de acordo com a especificação do trabalho) TODAS as instruções já existentes DEVEM conntinuar funcionando.


========Minhas adições:

Eu botei todas o que cada processador precisa nas suas respectivas pastas, não só os arquivos de memória.


