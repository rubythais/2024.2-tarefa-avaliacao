# 2024.2 Avaliação do 1o período de Sistemas Operacionais

# Informações pessoais
- Tâmara Thais Lourenço de carvalho
- Matricula: 20232014040040

## Informações gerais
- **Objetivo do repositório**: Avaliação do 1o bimestre da Disciplina de sistemas operacionais do curso de TADS do IFRN-CNAT
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** Sistemas Operacionais
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)

## Avaliação
- **Lembre de fazer o fork deste repositório**
- As questões foram construídas com o auxílio do [copilot](https://copilot.microsoft.com/)

# RESPOSTAS:
## Questão 1. Introdução a sistemas operacionais


- Para iniciar as conclusões do 1BM sobre o que é SO< na minha visão, é como o "gerente geral" do computador, o "cérebro". Ele organiza e controla tudo o que está acontecendo, tanto no hardware quanto no software, pra garantir que as coisas funcionem bem e com segurança. Segue os pontos que foram pedidos na questão:

- Gerenciamento de Processos: O SO cuida dos programas que estão sendo usados, decidindo quem pode usar o processador em cada momento. Por exemplo, quando eu estou assistindo a uma aula online e, ao mesmo tempo, usando um editor de texto pra anotar, o SO alterna entre essas tarefas de forma tão rápida que parece que tudo acontece ao mesmo tempo.

- Gerenciamento de Memória: Ele é quem distribui a RAM para os programas que abri. Se eu abro um jogo e deixo o navegador rodando, o SO aloca a memória pra cada um sem que um interfira no outro. Isso evita travamentos e faz o uso do computador ser mais fluido.

- Gerenciamento de Dispositivos de Entrada e Saída (I/O): O SO é o "tradutor" entre os dispositivos e os programas. Por exemplo, quando eu conecto um pendrive pra salvar arquivos, ele se encarrega de fazer a ponte entre o pendrive e o sistema, pra que os dados sejam transferidos corretamente.

- Gerenciamento de Arquivos: O SO organiza tudo no disco. Se eu salvo um trabalho da faculdade numa pasta, ele cuida de colocar o arquivo no lugar certo e ainda protege com permissões, se eu quiser, pra que só eu consiga acessar.

  
## Questão 2. Estrutura de sistemas operacionais
### Análise das Arquiteturas de Sistemas Operacionais: Monolítica, Microkernel e em Camadas

A escolha da arquitetura de um sistema operacional influencia bastante o custo, a segurança e a manutenção do sistema. Vou apresentar uma análise das arquiteturas monolítica, microkernel e em camadas, considerando a complexidade de implementação, a especialização necessária da equipe, as questões de segurança e a facilidade de atualização.

### **Complexidade de Implementação e Manutenção**

- **Monolítica**: Inicialmente, o desenvolvimento é mais rápido porque todos os componentes estão integrados em um único bloco de código. No entanto, a manutenção pode ser mais complicada, já que qualquer alteração pode afetar o sistema todo. Exemplos: **Linux** e **Unix**.
- **Microkernel**: Esse modelo é mais demorado de implementar, já que o núcleo é mínimo e serviços são separados em módulos. Mas, a manutenção tende a ser mais simples, pois falhas ficam restritas a componentes isolados. Exemplos: **Minix** e **QNX**.
- **Em Camadas**: A complexidade é intermediária. A manutenção é mais fácil, já que falhas podem ser isoladas em camadas específicas sem afetar o sistema todo. Exemplo: **Windows NT**.

### **Necessidade de Especialização da Equipe**

- **Monolítica**: A equipe pode ser mais generalista no começo, mas conforme o sistema cresce, será necessário ter especialistas para lidar com a complexidade que surge com o tempo.
- **Microkernel**: Exige uma equipe altamente especializada, pois o design e a comunicação entre os módulos exigem conhecimento profundo e experiência.
- **Em Camadas**: Requer uma especialização moderada, já que cada camada precisa ser bem definida, mas a interação entre elas é mais fácil de gerenciar em comparação com o microkernel.

### **Potenciais Vulnerabilidades de Segurança**

- **Monolítica**: Como todos os componentes estão juntos, uma falha pode afetar o sistema inteiro, tornando-o mais vulnerável.
- **Microkernel**: A segurança é melhor, pois falhas em módulos isolados não comprometem o núcleo do sistema, oferecendo maior proteção.
- **Em Camadas**: A segurança também é boa, mas depende de uma comunicação bem gerida entre as camadas para evitar falhas que possam gerar vulnerabilidades.

### **Facilidade de Atualização e Correção de Falhas**

- **Monolítica**: A atualização e a correção de falhas podem ser complicadas, já que uma modificação pode afetar várias partes do sistema ao mesmo tempo.
- **Microkernel**: Aqui, é muito mais fácil corrigir ou atualizar, pois os módulos podem ser alterados sem afetar o núcleo.
- **Em Camadas**: Também facilita a atualização, já que mudanças podem ser feitas em camadas isoladas, desde que as interações entre elas sejam bem controladas.


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

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre o equilíbrio entre segurança, performance e usabilidade, aplicando conceitos teóricos a contextos práticos.


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
