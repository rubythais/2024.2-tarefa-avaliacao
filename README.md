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


## Questão 3. Introdução à Segurança de Sistemas Operacionais

### **Controle de Acesso**

#### Benefícios:
- **Segurança**: O controle de acesso assegura que apenas usuários ou processos autorizados possam acessar e modificar recursos do sistema, protegendo dados e configurações sensíveis.
- **Integridade**: Impede que modificações indesejadas ou maliciosas ocorram em arquivos e configurações, aumentando a confiabilidade do sistema.

#### Desafios:
- **Complexidade**: A implementação de controles de acesso exige uma configuração cuidadosa de permissões, o que pode ser desafiador em sistemas grandes ou dinâmicos.
- **Overhead**: Cada vez que um usuário tenta acessar um recurso, o sistema precisa verificar as permissões, o que pode resultar em um custo adicional de processamento.

#### Impacto na Experiência do Usuário:
- **Positivo**: Usuários têm maior confiança na segurança do sistema, sabendo que seus dados e recursos estão protegidos.
- **Negativo**: Processos de autenticação e verificação de permissões podem tornar o uso do sistema mais lento e incômodo, especialmente quando exigem múltiplos passos para acesso.

#### Exemplos Críticos:
- Em sistemas bancários ou em servidores de arquivos, como no **Windows** ou **Linux**, onde o controle de acesso é vital para garantir que apenas usuários autorizados possam acessar dados sensíveis, como transações financeiras ou documentos confidenciais.

### **Criptografia**

#### Benefícios:
- **Proteção de Dados**: A criptografia garante que os dados tanto em trânsito quanto em repouso, fiquem protegidos contra interceptações ou acessos que não foram autorizados.
- **Confidencialidade**: Assegura que informações sensíveis, como senhas, dados bancários ou documentos pessoais, sejam mantidas em segredo, mesmo que sejam acessadas por atacantes.

#### Desafios:
- **Desempenho**: O processo de criptografar e descriptografar dados pode consumir recursos de processamento e impactar o desempenho, especialmente em operações que envolvem grandes volumes de dados.
- **Complexidade de Implementação**: Implementar criptografia de forma eficiente, sem introduzir vulnerabilidades, pode ser desafiador, exigindo configurações precisas e cuidados contínuos.

#### Impacto na Experiência do Usuário:
- **Positivo**: Usuários se sentem mais seguros sabendo que seus dados estão protegidos, principalmente ao fazer transações financeiras ou ao armazenar informações mais confidenciais.
- **Negativo**: O uso de criptografia pode resultar em lentidão em operações de leitura e gravação de dados, especialmente em dispositivos com recursos limitados, como smartphones ou outros sistemas mais antigos.

#### Exemplos Críticos:
- Em sistemas operacionais como **macOS** e **Windows**, onde a criptografia é usada para proteger dados armazenados no disco rígido (como o **BitLocker** no Windows ou o **FileVault** no macOS), garantindo q mesmo em caso de roubo do dispositivo, os dados estejam inacessíveis a outros acessos.



## Questão 4. Custo de Processamento versus Algoritmo Ótimo de Escalonamento

No escalonamento de processos, a escolha do algoritmo pode realmente impactar a performance do sistema operacional, principalmente quando a gente pensa no tempo de resposta, tempo de espera e utilização do processador. Vou explicar como vejo esses algoritmos e como eles afetam a performance de um sistema:

### **Algoritmos de Escalonamento**

1. **First-Come, First-Served (FCFS)**:
   - **Vantagens**: O **FCFS** é bem simples e fácil de implementar. Em cenários mais simples ou quando os processos chegam de maneira bem organizada, ele pode funcionar muito bem. Eu diria que ele é uma boa escolha para sistemas pequenos ou com menos complexidade.
   - **Desvantagens**: No entanto, ele pode ser bem ineficiente em sistemas com muitos processos de diferentes durações. Quando um processo longo é executado primeiro, os processos curtos ficam esperando muito tempo, o que pode resultar em um grande tempo de espera.

2. **Round Robin (RR)**:
   - **Vantagens**: O **Round Robin** parece ser bem mais justo, já que todos os processos recebem a mesma quantidade de tempo para execução. Eu vejo isso como uma boa escolha para sistemas interativos, onde queremos garantir que nenhum processo fique "preso" por muito tempo.
   - **Desvantagens**: Porém, ele pode gerar mais sobrecarga, porque o sistema precisa trocar de processo constantemente, o que consome mais tempo de CPU. Isso é algo que deve ser considerado, especialmente em sistemas com muitos processos.

### **Impacto do Custo de Processamento**

A escolha do algoritmo de escalonamento realmente depende do quanto estamos dispostos a gastar em termos de recursos do sistema. No caso do **FCFS**, como é um algoritmo mais simples, ele consome menos CPU, mas pode ser menos eficiente quando lidamos com uma grande variedade de processos. Por outro lado, o **Round Robin** oferece uma abordagem mais justa, mas exige mais tempo de processamento devido às trocas de contexto.

### **Exemplos de Situações**

- **Sistemas de Tempo Real**: Em sistemas onde a precisão e o tempo são cruciais, como em dispositivos médicos ou carros autônomos, talvez o **Priority Scheduling** seja mais adequado. Esse algoritmo prioriza processos de alta importância, garantindo que tarefas críticas sejam executadas primeiro.
- **Servidores Web**: Eu imagino que, em um servidor web, o **Round Robin** funcionaria bem, pois ele distribui o tempo de CPU igualmente entre as requisições, garantindo que nenhuma requisição seja deixada de lado.

### **Conclusão**

Em resumo, a escolha do algoritmo depende muito do tipo de sistema e das necessidades específicas de cada situação. Para sistemas mais simples, o **FCFS** pode ser suficiente, mas em sistemas interativos ou com muitos processos, o **Round Robin** parece ser mais eficaz, apesar da sobrecarga. O segredo está em balancear eficiência, justiça e o custo de processamento de acordo com as demandas de cada contexto.




# Questão 5. Aplicativo em python vs aplicativos em c

Quando comparamos o processo de execução de um aplicativo escrito em **Python** e um escrito em **C**, fica claro que os dois têm abordagens bem diferentes, principalmente em como o código é transformado até ser executado pelo hardware.

### **Python**

No Python, o código não é executado diretamente pelo computador. Ele passa por um **interpretador**, que lê e traduz o código para uma forma que o computador consiga entender. A primeira etapa é o interpretador converter o código Python para um **bytecode**, que é como um código intermediário, e esse bytecode é depois executado pela **máquina virtual Python (PVM)**. Esse processo pode ser mais lento, porque o código não é convertido de uma vez só em instruções que o processador entende. Em vez disso, ele é interpretado linha por linha enquanto o programa está rodando.

Além disso, o **kernel** do sistema operacional, que gerencia os recursos do computador (como memória e CPU), precisa interagir com os **drivers de dispositivo** para acessar o hardware necessário. Porém, como o Python depende do interpretador, essa interação pode ser mais demorada.

### **C**

No caso do C, a coisa funciona de uma forma diferente. O código C é **compilado** antes de ser executado. Ou seja, um **compilador** pega o código e transforma ele diretamente em **código de máquina**, que o processador entende, no formato binário (0 e 1). Isso significa que, quando o programa é executado, o computador já tem as instruções prontas e pode processá-las rapidamente, sem a necessidade de ficar interpretando o código durante a execução.

Depois de compilado, o programa em C pode interagir diretamente com o **kernel** e os **drivers** do sistema para acessar o hardware. E como o código já está em binário, o processo é mais rápido e eficiente.

### **Comparação**

- **Python**: O código é mais flexível e fácil de escrever, mas como precisa ser interpretado, ele acaba sendo mais lento. O interpretador vai traduzindo o código enquanto o programa está rodando.
  
- **C**: O código precisa ser compilado antes de ser executado, o que pode demorar mais na hora de compilar, mas depois a execução é bem mais rápida porque o código já está pronto para ser entendido pelo processador.

Quando penso na diferença entre um aplicativo em **Python** e um em **C**, posso ver que o processo até chegar ao hardware é bem distinto, e isso afeta tanto o desempenho quanto a forma como as coisas acontecem.

### **Aplicativo em Python**

- No caso do **Python**, o código não é diretamente executado pelo processador como o C. Isso porque o Python é uma linguagem **interpretada**. O que acontece é que quando rodo um programa Python, o **interpretador** entra em ação. Em vez de o código ser transformado de uma vez em código binário (1, 0) que o processador entende, o interpretador vai lendo e convertendo o código Python linha por linha para uma forma intermediária chamada **bytecode**. Esse bytecode ainda não é executado diretamente pelo processador, mas sim pela **máquina virtual do Python (PVM)**, que faz a interpretação dessas instruções.

- Além disso, o **kernel** do sistema operacional tem que mediar a comunicação entre o código Python e o hardware. Por exemplo, se o programa precisar acessar a memória ou um dispositivo de entrada/saída, o kernel é quem vai controlar essa questãp. Os **drivers de dispositivo** são responsáveis por traduzir as instruções do programa pra comandos que o hardware entenda. Esse processo torna o Python mais flexível, mas um pouco mais lento, já que há mais etapas envolvidas.

### **Aplicativo em C**

- Já o **C** é uma linguagem **compilada**, o que significa que o código fonte é transformado em **código de máquina** antes de ser executado. Quando escrevo um programa em C, passo por uma etapa de **compilação**, onde o **compilador** converte todo o código que escrevi diretamente para um arquivo executável que já está em formato binário, pronto para ser entendido pelo processador. Esse arquivo pode ser rodado diretamente sem precisar de uma tradução intermediária, o que geralmente torna a execução muito mais rápida.

- Apesar de o código já estar compilado, ainda é o **kernel** do sistema operacional que gerencia os recursos do sistema, como memória e processador, e se o programa precisar acessar o hardware, os **drivers de dispositivo** entram em cena, traduzindo o que o software pede para algo que o hardware realmente entenda. Mas o que diferencia é que, como o código já está em um formato de máquina, essa interação é muito mais direta e rápida.

### **Comparando os Dois**

- O que fica claro é que o **Python** tende a ser mais flexível, já que o código não precisa ser compilado antes de ser executado, mas isso faz com que o processo de execução seja mais demorado. O interpretador tem que traduzir tudo enquanto o código está sendo executado, o que torna o Python mais lento em termos de performance.

- Já o **C**, apesar de ser mais rápido na execução, exige mais trabalho inicial: preciso compilar o código primeiro para que ele seja transformado em um formato que o processador consiga entender. Mas, no final, o programa roda de forma muito mais eficiente, já que não depende de um interpretador no meio do caminho.

### **Conclusão**
- Então, a principal diferença que percebo entre **Python** e **C** é que o **Python** faz o código ser interpretado em tempo real, o que traz flexibilidade, mas pode impactar a velocidade. No **C**, o código é transformado em código de máquina antes de rodar, o que faz o programa ser mais rápido, mas requer um passo extra de compilação. Em ambos os casos, o **kernel** e os **drivers de dispositivo** ajudam a fazer a ponte entre o programa e o hardware, mas o processo é bem diferente para cada linguagem.
