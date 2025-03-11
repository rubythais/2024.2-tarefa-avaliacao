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


# RESPOOSTAS:

## Questão 1. Introdução a Sistemas Operacionais

O sistema operacional (SO) é como o "gerente geral" do computadpr, organizando e controlando hardware e software para garantir que tudo funcione de maneira eficiente e segura. Aqui estão os principais pontos pedidos na questão:

- **Gerenciamento de Processos**: O SO decide quais pos rogramas que podem usar o processador em cada momento. Por exemplo, quando assisto a uma aula online e anoto informações em um editor de texto, ele alterna rapidamente entre essas tarefas.
- **Gerenciamento de Memória**: Distribui a RAM para os programas abertos. Se um jogo e um navegador estão em execução, o SO aloca a memória de forma eficiente para evitar travamentos.
- **Gerenciamento de Dispositivos de Entrada e Saída (I/O)**: Atua como "tradutor" entre dispositivos e programas, garantindo que arquivos sejam salvos corretamente ao conectar um pendrive, por exemplo.
- **Gerenciamento de Arquivos**: Organiza os dados no disco, garantindo que arquivos sejam salvos no local correto e protegidos conforme as permissões definidas.

## Questão 2. Estrutura de Sistemas Operacionais

### **Análise das Arquiteturas de Sistemas Operacionais**

#### **Complexidade de Implementação e Manutenção**
- **Monolítica**: Desenvolvimento rápido, mas manutenção complicada. Ex.: **Linux, Unix**.
- **Microkernel**: Desenvolvimento mais demorado, mas falhas são isoladas. Ex.: **Minix, QNX**.
- **Em Camadas**: Manutenção mais simples, pois falhas podem ser isoladas. Ex.: **Windows NT**.

#### **Segurança e Vulnerabilidades**
- **Monolítica**: Uma falha pode comprometer todo o sistema.
- **Microkernel**: Maior segurança, pois módulos separados não afetam o núcleo.
- **Em Camadas**: Depende de comunicação eficiente entre camadas.

#### **Facilidade de Atualização e Correção de Falhas**
- **Monolítica**: Atualizações podem ser complicadas.
- **Microkernel**: Mais fácil atualizar, pois módulos podem ser alterados separadamente.
- **Em Camadas**: Atualização fácil, desde que interações entre camadas sejam bem geridas.

## Questão 3. Introdução à Segurança de Sistemas Operacionais

### **Controle de Acesso**

#### Beneficips:
- **Segurança**: Restringe o acesso a recursos apenas para usuários autorizados.
- **Integridade**: Evita modificações não autorizadas nos arquivos.

#### Desafios:
- **Complexidade**: Configuração de permissões pode ser desafiadora.
- **Overhead**: Pode impactar o desempenho do sistema.

#### Impacto na Experiência do Usuário:
- **Positivo**: Maior confiança na segurança do sistema.
- **Negativo**: Autenticação pode tornar o uso do sistema mais lento.

#### Exemplos Críticos:
- Em sistemas bancários e servidores de arquivos, como **Windows** e **Linux**.

### **Criptografia**

#### Benefícios:
- **Proteção de Dados**: Protege informações sensíveis.
- **Confidencialidade**: Mantém dados seguros mesmo em caso de roubo do dispositivo.

#### Desafios:
- **Desempenho**: Pode consumir muitos recursos de processamento.
- **Complexidade**: Configuração errada pode introduzir vulnerabilidades.

#### Impacto na Experiência do Usuário:
- **Positivo**: Protege informações sensíveis.
- **Negativo**: Pode causar lentidão em dispositivos mais antigos.

#### Exemplos Críticos:
- Ferramentas como **BitLocker (Windows)** e **FileVault (macOS)** garantem segurança dos dados.

## Questão 4. Custo de Processamento versus Algoritmo Ótimo de Escalonamento

### **Impacto dos Algoritmos de Escalonamento**

Os algoritmos de escalonamento afetam diretamente o tempo de resposta e a eficiência do processador. Alguns exemplos:

- **First-Come, First-Served (FCFS)**: Simples, mas pode causar longos tempos de espera.
- **Shortest Job Next (SJN)**: Reduz tempo de espera, mas pode gerar "fome" de processos longos.
- **Round Robin (RR)**: Justo para múltiplos usuários, pois dá fatias de tempo fixas para cada processo.
- **Prioridade**: Beneficia processos mais urgentes, mas pode causar inanição de processos de menor prioridade.

O algoritmo ideal depende do contexto e dos requisitos do sistema, balanceando eficiência e resposta rápida.

