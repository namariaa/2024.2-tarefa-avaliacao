# 2024.2 Avaliação do 1o período de Sistemas Operacionais

## Informações pessoais 
- Aluna: Ana Maria Ferreira de Abreu Guedes
- Matrícula: 20232014040001 

## Informações gerais
- **Objetivo do repositório**: Avaliação do 1o bimestre da Disciplina de sistemas operacionais do curso de TADS do IFRN-CNAT
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** Sistemas Operacionais
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)

## Avaliação
- **Lembre de fazer o fork deste repositório**
- As questões foram construídas com o auxílio do [copilot](https://copilot.microsoft.com/)

# Questão 1. Introdução a sistemas operacionais

Considere as funções e objetivos principais de um sistema operacional conforme discutido no texto. Explique como um sistema operacional gerencia os recursos de hardware e software de um computador para garantir eficiência e segurança. Em sua resposta, aborde os seguintes pontos:

- Gerenciamento de processos
- Gerenciamento de memória
- Gerenciamento de dispositivos de entrada e saída
- Gerenciamento de arquivos

**Dica**: Pense em exemplos práticos de como o sistema operacional realiza essas tarefas no dia a dia de um usuário.

**Resposta**: O SO serve como uma espécie de interface que "esconde" detalhes de operação do hardware do desenvolvedor e ele faz isso gerenciando tarefas e recursos (processadores, memória, discos,...) conciliando as requisições feitas ao hardware de forma rápida. Quando falamos do gerenciamento de recurso o SO é resposável pela distribuição otimizada do processador durante a execução de tarefas e do espaço de armazenamento.
O seus principais objetivos são: 
- Gerência do processador: Distribuindo a capacidade do processador, como foi citado acima 
- Gerência de memória: Fornecimento de um espaço de memória específico para cada aplicação de acordo com as necessidades 
- Gerência de dispositivos: Gerenciamento de periféricos através da detecção desses dispositivos de entrada/saída e utilização de drivers para isso
- Gerência de arquivos: Criação de arquivos e diretórios 
- Gerência de proteção: Colocar níveis de acesso e permissões que cada usuário ode acessar  


# Questão 2. Estrutura de sistemas operacionais

## Texto informativo
### Estrutura de Sistemas Operacionais: Custo de Desenvolvimento e Segurança da Informação

A estrutura de um sistema operacional (SO) é fundamental para determinar tanto o custo de desenvolvimento e manutenção quanto a segurança da informação. Existem várias arquiteturas de SO, como monolítica, microkernel e em camadas, cada uma com suas próprias implicações em termos de custo e segurança.

#### Custo de Desenvolvimento e Manutenção

1. **Arquitetura Monolítica**:
   - **Desenvolvimento**: Geralmente, mais rápida de desenvolver inicialmente, pois todos os componentes do SO são integrados em um único bloco de código.
   - **Manutenção**: Pode ser mais complexa e cara, pois qualquer alteração em um componente pode afetar todo o sistema, exigindo testes extensivos e cuidadosos.

2. **Arquitetura Microkernel**:
   - **Desenvolvimento**: Pode ser mais demorada e cara inicialmente, pois envolve a criação de um núcleo mínimo e a implementação de serviços adicionais como processos separados.
   - **Manutenção**: Mais fácil e menos custosa, já que os componentes são isolados. Atualizações e correções podem ser feitas em módulos específicos sem impactar o núcleo do sistema.

3. **Arquitetura em Camadas**:
   - **Desenvolvimento**: Moderadamente complexa, pois cada camada deve ser bem definida e interagir corretamente com as outras.
   - **Manutenção**: Relativamente fácil, pois problemas podem ser isolados e corrigidos em camadas específicas sem afetar o restante do sistema.

#### Segurança da Informação

1. **Arquitetura Monolítica**:
   - **Segurança**: Pode ser mais vulnerável, pois uma falha em qualquer parte do sistema pode comprometer todo o SO. A integração de todos os componentes em um único bloco de código pode dificultar a implementação de medidas de segurança robustas.

2. **Arquitetura Microkernel**:
   - **Segurança**: Geralmente mais segura, pois isola os serviços em processos separados. Isso limita o impacto de uma falha ou ataque a um único componente, protegendo o núcleo do sistema e outros serviços.

3. **Arquitetura em Camadas**:
   - **Segurança**: Oferece um bom equilíbrio, pois cada camada pode implementar suas próprias medidas de segurança. No entanto, a comunicação entre camadas deve ser cuidadosamente gerenciada para evitar vulnerabilidades.

### Conclusão

A escolha da arquitetura de um sistema operacional tem um impacto significativo tanto no custo de desenvolvimento e manutenção quanto na segurança da informação. Arquiteturas monolíticas podem ser mais rápidas e baratas de desenvolver inicialmente, mas podem acarretar custos de manutenção mais altos e maiores riscos de segurança. Por outro lado, arquiteturas microkernel e em camadas podem exigir um investimento inicial maior, mas oferecem vantagens em termos de manutenção e segurança.

## Questão
Com base no texto sobre a estrutura de sistemas operacionais, analise como as diferentes arquiteturas (monolítica, microkernel e camadas) impactam o custo com a equipe de desenvolvimento e a segurança do sistema operacional. Em sua resposta, considere os seguintes pontos:
- Complexidade de implementação e manutenção
- Necessidade de especialização da equipe
- Potenciais vulnerabilidades de segurança
- Facilidade de atualização e correção de falhas

**Dica:** Utilize exemplos de sistemas operacionais reais que adotam essas arquiteturas para ilustrar sua análise.

**Reposta:** Existem diferentes arquiteturas pelos diversos tipo de organização possível dos componentes do SO e a escolha influi bastante para o funcionamento interno. Falaremos agora sobre optar-se pela escolha de algumas arquiteturas:
- Arquiterura monolítica: Apesar dos componetes do sistema serem compilados em módulos separados eles são unificados em um único programa executável o que posteriormente pode acarretar em um grande comprometimento do sistema caso houver problemas em algum dos processos, desencadeando erros no núcleo do sistema pois essa arquitetura utilizada o modo kernel (núcleo, que é responsável pela comunicação entre os processos e gerências de memória, processador, dispositvos perifericos e de sistemas de arquivos). Apesar de não ser de complexa implementação, pelos problemas citados anteriormente a gerência se torna algo difícil tornando essencial uma equipe especializada para a manuntenção e atualizações. Um exemplo de seu uso foi na primeira versão do linux.
![sistemas_operacionais_a01_f05_a](https://github.com/user-attachments/assets/a829dcde-7e45-4834-adfb-c6a762d746e8)

- Arquitetura kernel/micro-núcleo: Retira todos os aspectos de alto nível como controle de acesso aos recursos fora do núcleo e mantém apenas código de baixo nível com propósito de interação com o hardware. Os processos não possuem acesso a componentes do sistema e isso torna a margem de erro total menor, pois se ocorrer um erro em uma das partes não prejudicará todo o sistema isso se deve pela proteção do núcleo nesse processo trazendo uma maior segurança apesar de sua implementação ser mais complexa e custosa sua manunteção é facilitada e "barata". Um exemplo de seu uso é a openVMS.
  ![kernel2](https://github.com/user-attachments/assets/b9567f28-aef0-4bc7-8f91-6b6a910e84c7)

- Arquitetura em camadas: Com o aumento de complexidade dos So's essa arquitetura dividiu o processo em níveis onde os inferiores (provem interaface com o hardware) e as intermediárias (provem abstração) se comunicam com os níveis superiores(interface para as aplicações). Como principais vantagens podemos citar o isolomento das camadas que resulta em uma maior segurança e proteção. Quando falamos das principais desvantagens podemos citar um menor desempenho pela mudança constante de modo de acesso pois quando uma aplicação faz uma solicitação para o kernel é necessário passar por diversa camadas. Apesar do fácil desenvolvimento não possui fácil facilidade implantação pois uma pequena mudança em um componente pode gerar a necessidade colocar toda a aplicação no ar novamente.
  
# Questão 3. Introdução à Segurança de Sistemas Operacionais

## Texto informativo

A segurança de um sistema operacional é um aspecto crucial que visa proteger os recursos do sistema contra acessos não autorizados, ataques maliciosos e falhas. Um sistema operacional seguro deve garantir a integridade, confidencialidade e disponibilidade dos dados e serviços. Para alcançar esses objetivos, várias técnicas e mecanismos são implementados, incluindo:

1. **Controle de Acesso**: Define quem pode acessar o sistema e quais recursos podem ser utilizados. Isso é feito através de autenticação (verificação de identidade) e autorização (permissão de acesso).

2. **Criptografia**: Utilizada para proteger dados em trânsito e em repouso, garantindo que apenas usuários autorizados possam acessar informações sensíveis.

3. **Auditoria e Monitoramento**: Registra atividades do sistema para detectar e responder a comportamentos suspeitos ou anômalos.

4. **Isolamento de Processos**: Garante que os processos sejam executados em ambientes isolados, evitando que um processo comprometa a segurança de outro.

5. **Atualizações e Patches**: Manter o sistema operacional atualizado é essencial para corrigir vulnerabilidades conhecidas e proteger contra novas ameaças.


## Questão

Considerando os mecanismos de segurança discutidos, analise como a implementação de controles de acesso e criptografia pode impactar a performance e a usabilidade de um sistema operacional. Em sua resposta, aborde os seguintes pontos:
- Benefícios e desafios de cada mecanismo
- Impacto na experiência do usuário
- Exemplos de situações onde esses mecanismos são críticos

**Dica:** Pense em como esses mecanismos são aplicados em sistemas operacionais que você utiliza no dia a dia, como Windows, Linux ou macOS.

**Resposta:** Quando se trata a controle de acesso ele divide em modo usuário e kernel com diferenças apenas no nível de acesso a funcionalidades que cada um possui isso serve como uma forma de proteção para o núcleo do sistemas e não tornar ele vunerável a alterções de processo indévidos que acarretem problemas no funcionamento como um todo. Isso traz um ambiente mais seguro para o usuário de proteção de dados pois o controle de acesso responde rapidamente a qualquer atividade suspeita.
E quando se trata de criptografia ela tem uma papel crucial também na segurança trazendo confiabilidade para os usuários e assim como o controle de acesso ele traz um significativa importância na proteção de dados e conteúdos e como diferenciação tem uma função contra cópias.

# Questão 4. Custo de Processamento versus Algoritmo Ótimo de Escalonamento

## Texto informativo

O escalonamento de processos é uma função crítica de um sistema operacional, responsável por determinar a ordem em que os processos são executados pelo processador. O objetivo é maximizar a eficiência do sistema, garantindo que os recursos sejam utilizados de maneira justa e eficaz. No entanto, encontrar o algoritmo de escalonamento ótimo envolve um equilíbrio delicado entre o custo de processamento e a eficiência do escalonamento.

### Custo de Processamento

O custo de processamento refere-se ao tempo e aos recursos necessários para executar um algoritmo de escalonamento. Algoritmos mais complexos podem oferecer melhores resultados em termos de tempo de resposta e utilização do processador, mas também podem exigir mais recursos computacionais para tomar decisões de escalonamento. Isso pode incluir tempo de CPU, memória e outras operações de sistema.

### Algoritmo Ótimo de Escalonamento

Um algoritmo ótimo de escalonamento é aquele que maximiza a eficiência do sistema operacional, minimizando o tempo de espera dos processos, o tempo de resposta e o tempo de retorno. Alguns dos algoritmos de escalonamento mais comuns incluem:

- **First-Come, First-Served (FCFS)**: Simples e fácil de implementar, mas pode levar a longos tempos de espera para processos curtos.
- **Shortest Job Next (SJN)**: Minimiza o tempo médio de espera, mas pode ser difícil de implementar devido à necessidade de prever o tempo de execução dos processos.
- **Round Robin (RR)**: Oferece uma abordagem justa, atribuindo fatias de tempo iguais a todos os processos, mas pode resultar em maior sobrecarga de contexto.
- **Priority Scheduling**: Processos com maior prioridade são executados primeiro, mas pode levar à inanição de processos de baixa prioridade.

## Questão

Considerando os conceitos de custo de processamento e algoritmo ótimo de escalonamento, analise como diferentes algoritmos de escalonamento podem impactar a performance de um sistema operacional em termos de tempo de resposta, tempo de espera e utilização do processador. Em sua resposta, aborde os seguintes pontos:
- Vantagens e desvantagens de pelo menos dois algoritmos de escalonamento
- Impacto do custo de processamento na escolha do algoritmo
- Exemplos de situações onde um algoritmo pode ser preferível a outro

**Dica:** Pense em como esses algoritmos são aplicados em diferentes cenários, como sistemas de tempo real, servidores web e sistemas operacionais de uso geral.

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre a complexidade e os trade-offs envolvidos na escolha de um algoritmo de escalonamento, aplicando conceitos teóricos a contextos práticos.

# Questão 5. Aplicativo em python vs aplicativos em c

## Questão

Explique o caminho que as instruções seguem desde um aplicativo escrito em Python e um aplicativo escrito em linguagem C até serem executadas pelo hardware. Em sua resposta, considere os seguintes pontos:
- O papel do interpretador no caso do Python
- O processo de compilação no caso do C
- A interação entre o kernel do sistema operacional e os drivers de dispositivo
- A tradução final das instruções para o formato binário (0 e 1) executado pelo hardware

**Dica:** Compare e contraste os dois processos, destacando as principais diferenças e semelhanças na forma como as instruções são processadas e executadas.

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre os diferentes caminhos que as instruções seguem em linguagens interpretadas e compiladas, aplicando conceitos teóricos a contextos práticos.
