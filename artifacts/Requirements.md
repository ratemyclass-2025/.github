# Requisitos Funcionais  e Não Funcionais

## 1. Introdução  
Este documento descreve os **requisitos funcionais e não funcionais** do sistema de avaliação acadêmica e compartilhamento de materiais. Ele define as principais funcionalidades que o sistema deve possuir para atender aos objetivos do projeto.  

---

## 2. Requisitos Funcionais  

### **1 Autenticação e Conta de Usuário**  

#### RF-01 Criar Conta de Usuário  
- O sistema deve permitir que usuários se cadastrem usando **e-mail institucional**.  
- O e-mail deve ser validado antes da ativação da conta.  
- O usuário deve fornecer **nome, curso e senha** no cadastro.  

#### RF-02 Fazer Login  
- O usuário deve poder fazer login utilizando **e-mail e senha válidos**.  
- O sistema deve exibir uma **mensagem de erro** caso as credenciais sejam inválidas.  
- Deve haver opção de **recuperação de senha** via e-mail.  

#### RF-03 Recuperar Senha  
- O usuário deve poder solicitar uma **nova senha**.  
- O sistema deve enviar um **link de redefinição de senha** para o e-mail cadastrado.  

---

### **2 Perfil de Usuário**  

#### RF-04 Criar e Exibir Perfil de Usuário  
- O sistema deve permitir que cada usuário tenha um perfil contendo **nome, curso, avaliações feitas e materiais compartilhados**.  
- Apenas o **próprio usuário** pode visualizar seu perfil completo.  

#### RF-05 Editar Informações do Perfil  
- O usuário pode editar seu **nome e curso**.  
- O e-mail **não pode ser alterado** após o cadastro.  

#### RF-06 Visualizar e Gerenciar Materiais Compartilhados  
- O usuário pode ver **todos os materiais que compartilhou** no sistema.  
- O usuário pode **excluir ou editar** seus próprios materiais.  

---

### **3 Avaliação de Disciplinas e Professores**  

#### RF-07 Avaliar uma Disciplina  
- O usuário pode avaliar uma disciplina, atribuindo **notas de 1 a 5** em critérios como:
  - **Dificuldade**  
  - **Didática do professor**  
  - **Carga horária**  
- O usuário pode adicionar um **comentário opcional** à sua avaliação.  

#### RF-08 Avaliar um Professor  
- O usuário pode avaliar um professor com base nos seguintes critérios:
  - **Pontualidade**  
  - **Didática**  
  - **Suporte ao aluno**  
- O usuário pode deixar um **comentário sobre a experiência com o professor**.  

#### RF-09 Editar ou Excluir Avaliações  
- O usuário pode **editar ou excluir** suas próprias avaliações.  
- Após a exclusão, a avaliação **não poderá ser recuperada**.  

#### RF-10 Moderação de Avaliações  
- Usuários podem **denunciar avaliações** que sejam ofensivas ou inapropriadas.  
- Administradores podem **remover avaliações denunciadas**.  

---

### **4 Compartilhamento de Materiais**  

#### RF-11 Adicionar Material de Estudo  
- O usuário pode compartilhar **links externos** ou **arquivos permitidos** pelo sistema.  
- O material deve estar **vinculado a uma disciplina específica**.  

#### RF-12 Avaliar a Utilidade dos Materiais  
- O usuário pode **curtir ou reagir** a um material compartilhado.  
- O sistema deve exibir os **materiais mais bem avaliados** primeiro.  

#### RF-13 Editar ou Excluir Materiais  
- O usuário pode **editar a descrição** de um material que compartilhou.  
- O usuário pode **excluir um material** que não seja mais relevante.  

---

### **5 Busca e Organização**  

#### RF-14 Pesquisar Disciplinas e Professores  
- O usuário pode pesquisar disciplinas e professores **pelo nome**.  
- Os resultados devem exibir **notas médias e comentários** sobre cada disciplina ou professor.  

#### RF-15 Aplicar Filtros de Busca  
- O usuário pode filtrar a busca por:
  - **Curso**  
  - **Departamento**  
  - **Popularidade (notas mais altas)**  

#### RF-16 Sugestões de Pesquisa  
- O sistema deve sugerir **disciplinas e professores populares** com base nas buscas mais frequentes.  

---

### **6 Moderação e Segurança**  

#### RF-17 Denúncia de Comentários e Avaliações  
- O usuário pode denunciar avaliações e comentários inadequados.  
- Um administrador poderá visualizar **todas as denúncias recebidas** e tomar uma decisão.  

#### RF-18 Restrição de Edições Após um Período  
- Para evitar manipulações, avaliações só poderão ser editadas dentro de **48 horas** após serem publicadas.  

#### RF-19 Notificações ao Usuário  
- O usuário será notificado quando:
  - Uma avaliação ou material que postou **receber curtidas**.  
  - Uma avaliação que fez **for respondida por outro usuário**.  
  - Um **material seu for denunciado ou removido**.  

---
## 2. Não Funcionais (RNF) 
Esses requisitos garantem a **qualidade e desempenho** do sistema.  

### **RNF-01 Disponibilidade**  
- O sistema deve estar disponível **24h por dia, 7 dias por semana**, com **tempo de inatividade máximo de 5% ao mês**.  

### **RNF-02 Usabilidade**  
- A interface deve ser **intuitiva e responsiva** para facilitar a navegação dos usuários.  

### **RNF-03 Segurança**  
- O sistema deve armazenar senhas utilizando **hashing seguro (bcrypt ou Argon2)**.  
- O acesso ao sistema deve ser protegido por **autenticação JWT**.  

### **RNF-04 Desempenho**  
- As buscas por disciplinas e professores devem retornar resultados em **menos de 4 segundos**.  
- O tempo de resposta do servidor deve ser **inferior a 500ms** para requisições padrão.  



