# ☁️ Desafio AWS — Gerenciamento de Instâncias EC2, AMI e EBS

Repositório criado para documentar o desafio da **DIO** sobre **gerenciamento de instâncias EC2** na **Amazon Web Services (AWS)**.
O objetivo é consolidar o aprendizado prático sobre criação, configuração, backup e restauração de instâncias na nuvem.

---

## 🎯 Objetivo do Desafio

Aplicar na prática os principais conceitos aprendidos nas aulas de **EC2**, **AMI** e **EBS**, demonstrando domínio das etapas de criação, segurança e gerenciamento de instâncias na AWS.

---

## 🧠 Conceitos Abordados

- **Amazon EC2 (Elastic Compute Cloud)** — Criação e gerenciamento de instâncias virtuais.  
- **Amazon Machine Image (AMI)** — Criação de imagens personalizadas para reutilização.  
- **Amazon EBS (Elastic Block Store)** — Armazenamento persistente e criação de snapshots.  
- **Security Groups** — Controle de tráfego de entrada e saída.  
- **Acesso SSH** — Conexão segura às instâncias.  

---

## ⚙️ Etapas do Laboratório

### 1️⃣ Criação e Configuração da Instância EC2
- Tipo de instância: `t2.micro` (elegível ao free tier).  
- Par de chaves SSH gerado para acesso seguro.  
- Associação a um **Security Group** com regras:
  - **Inbound:** Porta 22 (SSH) liberada apenas para meu IP.  
  - **Outbound:** Tráfego liberado para todas as portas.  
- Teste de acesso via terminal (usando o arquivo `.pem`).

---

### 2️⃣ Criação e Uso de Imagens AMI
- Após a configuração inicial da instância, foi criada uma **imagem AMI personalizada**.  
- Essa imagem permite **replicar a instância** com as mesmas configurações e pacotes instalados.  
- Passos realizados:
  1. No console EC2, selecione a instância.
  2. Clique em **Actions > Image and templates > Create image**.
  3. Defina o nome da imagem e confirme.
- Resultado: uma AMI disponível na conta para futuras instâncias.

---

### 3️⃣ Snapshots EBS
- Criado um **snapshot** do volume EBS anexado à instância.
- Snapshots são backups incrementais que permitem **restaurar volumes** em caso de falha ou exclusão.
- Passos realizados:
  1. Acessar o menu **Elastic Block Store > Volumes**.
  2. Selecionar o volume e clicar em **Create snapshot**.
  3. Inserir descrição e confirmar.
- Também foi testada a **restauração de um volume** a partir de um snapshot.

---

## 🖼️ Evidências Visuais
As imagens estão disponíveis na pasta [`/images`](./images):

*(As imagens demonstram o processo passo a passo realizado no laboratório.)*

---

## 🧰 Tecnologias e Ferramentas Utilizadas

- **AWS EC2, AMI e EBS**
- **Git e GitHub**
- **Markdown**
- **SSH (Secure Shell)**
- **Draw.io**

---

## 🚀 Como Reproduzir o Laboratório

1. Criar uma instância EC2
2. Configurar um Security Group com porta 22 liberada para seu IP.  
3. Conectar via SSH usando a chave `.pem`.  
4. Criar uma **imagem AMI** da instância.  
5. Gerar um **snapshot EBS** do volume principal.  
6. Documentar todo o processo no GitHub.

---

## 📚 Referências

- [Documentação AWS — Amazon EC2](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/concepts.html)  
- [Documentação AWS — AMI](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/AMIs.html)  
- [Documentação AWS — EBS Snapshots](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/EBSSnapshots.html)  
- [Guia de Markdown no GitHub](https://guides.github.com/features/mastering-markdown/)

---

## 👩‍💻 Autora

**Jéssica Fernandes**  
Estudante de **Ciência da Computação** e **biomédica em transição de carreira para Tecnologia**, com foco em **Desenvolvimento Full Stack** e **Análise de Dados**.  
Apaixonada por aprendizado contínuo e pela criação de soluções que conectam **pessoas e tecnologia**.

📎 [Meu GitHub](https://github.com/Jessica-SFernandes)
