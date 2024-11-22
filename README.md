<!---
<style>
r { color: Red }
o { color: Orange }
g { color: Green }
</style>
-->
<!---

<p float="left">
  <img src="images/hierarquia.png" width="400" />
  <img src="images/piramidemodelos.png" width="400" />
</p>

🔴 red: +5V
🟠 orange: +3.3V
⚫ black: ground
⚪ white: ground (pull-down)
🟣 purple: I2C signal
🟢 green: clock signal
🟡 yellow: WS2812 signal
🔵 blue: resistor bridge (analogue) input
-->

# AWS Cloud Practitioner Study Guide

Este repositório contém conteudos e resumos, focados em Cloud computing e AWS, que aprendi durante o estudo para a certificação AWS Cloud Practitioner e outras certificações.

O exame tem os seguintes domínios do conteúdo e ponderações:

- Domínio 1: Conceitos da nuvem (24% do conteúdo pontuado)
- Domínio 2: Segurança e conformidade (30% do contéudo pontuado)
- Domínio 3: Tecnologia e serviços da nuvem (34% do contéudo pontuado)
- Domínio 4: Cobrança, preços e suporte (12% do conteúdo pontuado)

O conteúdo está **_numerado_** de acordo com os domínios da certificação AWS Practitioner, porém **_ordenado_** da melhor maneira para o entendimento.

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request com melhorias ou correções.

## 1.Conceitos da nuvem

Computação em nuvem é a entrega sob demanda de poder computacional, armazenamento de banco de dados, aplicativos e outros recursos de TI por meio de uma plataforma de serviços em nuvem via Internet, com precificação <**pay-as-you-go**>.

Essa abordagem oferece uma maneira simples de acessar servidores, armazenamento, bancos de dados e um amplo conjunto de serviços de aplicativos pela Internet.

A AWS possui e mantém o hardware conectado à infraestrutura necessária para executar esses serviços, enquanto você provisiona e utiliza o que precisa por meio de uma aplicação web.

## 1.Vantagens da Nuvem AWS

1. **Custo Reduzido:**

   1. **Troque despesas de capital por despesas variáveis:**
      - Pague apenas pelos recursos de computação que consome, eliminando a necessidade de investir antecipadamente em data centers e servidores.

1. **Escala Global:**
   1. **Torne-se global em minutos:**
      - Implante aplicativos em várias regiões do mundo com facilidade, proporcionando uma melhor experiência para os clientes
1. **Performance:**
   1. **Pare de adivinhar a capacidade:**
      - Elimine a adivinhação sobre suas necessidades de capacidade, obtendo acesso flexível e escalável conforme necessário.
1. **Velocidade e Agilidade:**
   1. **Aumente a velocidade e a agilidade:**
      - Desenvolva e disponibilize recursos de TI em minutos, proporcionando maior agilidade organizacional.
1. **Produtividade:**
   1. **Pare de gastar dinheiro executando e mantendo data centers:**
      - Concentre-se em projetos diferenciais, deixando a infraestrutura para provedores de nuvem como a AWS.
1. **Segurança:**
   1. **Seguro:**
      - A AWS utiliza uma abordagem de ponta a ponta para proteger e fortalecer nossa infraestrutura, incluindo medidas físicas, operacionais e de software. Para obter informações, consulte o Centro de Segurança da AWS.
1. **Flexibilidade:**
   1. **Flexível:**
      - A AWS permite que você selecione o sistema operacional, a linguagem de programação, a plataforma de aplicativos da web, o banco de dados e outros serviços necessários. Com a AWS, você recebe um ambiente virtual que lhe permite carregar o software e os serviços que o seu aplicativo necessita. Isso facilita o processo de migração para aplicativos existentes enquanto preserva opções para criar novas soluções.

> _Benefícios_:

https://aws.amazon.com/pt/application-hosting/benefits/

## Modelos de Computação em Nuvem

![modelosComputacao](images/modelos.jpg)

1. **Infraestrutura como Serviço (IaaS):**
   - Contém os componentes básicos da TI em nuvem e, geralmente, dá acesso (virtual ou no hardware dedicado) a recursos de rede e computadores, como também espaço para o armazenamento de dados.
   - Um exemplo comum de IaaS na AWS é o Amazon EC2, do qual você tem acesso virtual a recursos de computação na nuvem.
2. **Plataforma como Serviço (PaaS):**
   - Elimina a necessidade de gerenciar a infraestrutura subjacente, permitindo que você se concentre no desenvolvimento e gerenciamento de aplicativos.
   - Um exemplo comum de PaaS na AWS é o Amazon RDS, do qual você não tem a necessidade de gerenciar a infraestrutura subjacente para iniciar um banco de dados relacional.
3. **Software como Serviço (SaaS):**
   - Não é necessário saber em como o serviço é mantido ou como a infraestrutura subjacente é gerenciada, você só precisa pensar em como usará este tipo específico de software.
   - Um exemplo comum de aplicação do SaaS é o webmail, no qual você pode enviar e receber e-mails sem precisar gerenciar recursos adicionais para o produto de e-mail ou manter os servidores e sistemas operacionais no qual o programa de e-mail está sendo executado.

Exemplo: Zendesk(AWS MarketPlace), Google Sheets, etc.

<p float="left">
  <img src="images/hierarquia.png" width="400" />
  <img src="images/piramidemodelos.png" width="400" /> 
</p>

## 3.Tipos de implantação na Nuvem

Existem três tipos comuns de implantação em nuvem:

1. **Nuvem Pública:**
   - Totalmente implantada na nuvem, com todas as partes da aplicação em execução na nuvem.
2. **Nuvem Híbrida:**
   - Conecta recursos em nuvem AWS, a recursos existentes fora da nuvem (ambiente on-premises), proporcionando uma integração híbrida entre esses ambientes.
3. **Nuvem Privada (on-premises):**
   - Nuvem gerenciada internamente, usando virtualização e ferramentas de gerenciamento de recursos. Ela pode estar tanto on-premises, quanto em um hardware dedicado em uma provedora de nuvem.

## Planos do AWS Support

Existem 4 planos de suporte AWS:

Developer, Business, Enterprise On-Ramp, Enterprise

(Ler a tabela inteira em:https://aws.amazon.com/pt/premiumsupport/plans/)

### Legenda:

- **Service quotas**(cotas de serviço)**:** Limites impostas via recurso(numero máximo de EC2 em uma região) ou conta (numero máximo de buckets em um s3), existem limites flexíveis(soft limits) e não flexíveis(hard limits)
- **Trusted Advisor**(consultor confiável**)**:Ferramenta da AWS para te ajudar através de conselhos e indicações, como Reduzir custo, Aumentar a performance, Melhorar a Segurança e te indicar Possíveis falhas futuras(Fault tolerance).
- **API do Support**: API utilizada para abrir casos no suporte(Apenas enterprise on-Ramp, ou enterprise)
- **Support automation workflows**: Diagnostico e correção automático a partir de coleções de troubleshooting comuns feitos pela engenharia do suporte.
- **AWS re:Post**: Comunidade(Fórum) da AWS, tendo acessos a conteúdos selecionados e especialistas cloud

![planos_support](images/planos_support.png)
![planos_support2](images/support2.jpg)

## 2.3 IAM

No IAM da AWS, funções, políticas e grupos são todos usados para gerenciar o acesso aos recursos da AWS.

Uma **função** define um conjunto de **políticas de acesso** que determinam quais ações um **usuário ou serviço** da AWS pode realizar. As funções são úteis quando você deseja conceder acesso (temporário) a recursos da AWS a uma entidade de terceiros, como um serviço da AWS ou um usuário fora da sua conta da AWS.

Uma **política**, por outro lado, é um documento em **JSON** que define um conjunto de **permissões** e especifica a quais recursos da AWS essas **permissões** concedem acesso. **As políticas podem ser anexadas a funções**, grupos ou usuários individuais para definir seu **nível de acesso** aos recursos da AWS. As políticas são úteis quando você deseja definir e impor permissões específicas para um recurso ou conjunto de recursos específicos.

Um **grupo** é uma coleção de usuários que compartilham permissões comuns. Os grupos facilitam a gestão de permissões para vários usuários de uma vez, pois as políticas podem ser anexadas a um grupo e aplicadas a todos os usuários dentro desse grupo. Ao atribuir permissões a um grupo, é possível conceder ou revogar o acesso para vários usuários com uma única ação.

De maneira geral, as funções são usadas para conceder acesso a recursos ou serviços específicos, as políticas são usadas para definir as permissões para esses recursos ou serviços, e os grupos são usados para organizar e gerenciar vários usuários com permissões semelhantes.

## **2.3 Funções do IAM com instâncias EC2**

As funções do IAM podem ser usadas para conceder permissões a aplicativos em execução em instâncias EC2 para solicitações de API da AWS usando perfis de instância.

Apenas uma função pode ser atribuída a uma instância EC2 por vez.

Uma função pode ser atribuída no momento da criação da instância EC2 ou a qualquer momento posteriormente.

Crie uma função do IAM com duas políticas:

- Política de permissões – concede ao usuário da função as permissões necessárias em um recurso.
- Política de confiança – especifica as contas confiáveis que têm permissão para assumir a função. Wildcards(todos, no caso usa-se o asterisco (\*)) não podem ser especificados como principal. Uma política de permissões também deve ser anexada ao usuário na conta confiável

## 2.3 IAM Identity Center

O **IAM Identity Center** foi desenvolvido com base no AWS **Identity** and Access Management (**IAM**) para simplificar o gerenciamento de **acesso a várias contas da AWS**, **aplicações da AWS** e outras **aplicações de nuvem habilitadas para SAML.**

**_IAM:_** Habilita usuários e grupos, para os recursos e serviços da conta que foram criados, **preferencialmente utilizado** de modo programático em uma única conta
**_IAM Identity Center:_** Habilita novos usuários e grupos, para terem **acesso a várias contas** AWS, **aplicações da AWS** por exemplo um PaaS ou SaaS, **preferencialmente utilizado** a usuários que precisam de acesso ao **portal**

![portal_aws](images/Portal_acesso_aws.png)

> Portal de Acesso AWS, contas e serviços

## 4. AWS Organizations

AWS Organizations é uma poderosa ferramenta para gerenciar, organizar e aplicar políticas de segurança em um ambiente multi-conta AWS.

Utilizando OUs e SCPs, é possível manter um controle rigoroso sobre as permissões e garantir conformidade em toda a organização, enquanto aproveita a flexibilidade e a escalabilidade da nuvem AWS.

**Lembre-se para o exame, que:**

- O AWS Organizations é um serviço de gerenciamento de contas, que permite **consolidar várias contas AWS**, **em uma única organização**.
- A grande vantagem de utilizar o AWS Organizations é obter **faturamento consolidado**.

Nesse diagrama do AWS Organizations, é possível ver a Master Account, Unidades Organizacionais (OUs), Contas AWS e políticas de acesso (ServiceControlPolicies).

![aws-organizations](images/aws_organizations.jpg)

## 3.2 Definir a infraestrutura global da AWS.

Sua infraestrutura é constituída por Regiões, Zonas de Disponibilidade, Pontos de Presença (também conhecido como locais de borda) e zonas locais

Uma **Região da AWS** é uma localização física no mundo, é completamente independente e contém várias zonas de disponibilidade.

Uma **Zona de Disponibilidade** consistem em um ou mais data centers discretos, cada um com energia redundante, rede, alojados em instalações separadas e conectados com links de baixa latência

Os **Pontos de Presença(Locais de borda)** são uma infraestrutura de servidores alocados distantes de regiões da AWS, e servem como **cache de informações dos dados de usuários,** para acelerar a entrega de conteúdo para usuários distantes.

E as **Zonas Locais** são um tipo de **implantação de infraestrutura da AWS** que oferecem baixa latência em algum ponto geográfico, sendo geralmente associado em alguma cidade , permitindo aplicações com requisitos de latência inferior a 10 milissegundos aos usuários, devido ter uma **conexão de rede privada direta**, com uma AZ da AWS.

> _Resumo:_

- **\*Edge Locations (Pontos de Presença):** Ideais para distribuição de conteúdo estático e dinâmico, aceleração de sites, APIs, e melhoria de desempenho global e segurança.\*
- **\*Local Zones (Zonas Locais):** Melhor utilizadas para aplicativos sensíveis à latência, que precisam de recursos computacionais próximos aos usuários, ou para garantir conformidade e desempenho específicos de uma região.\*

AZ’s(Availability Zone)

- Você mantém controle completo e propriedade sobre a região na qual seus dados estão fisicamente localizados, facilitando o atendimento aos requisitos regionais de conformidade e residência de dados.
- Observe que há uma taxa para transferência de dados entre regiões.
- Cada Zona de Disponibilidade é projetada como uma zona de falha independente.
- Se distribuir suas instâncias EC2 em várias Zonas de Disponibilidade e uma instância falhar, você pode projetar sua aplicação para que uma instância em outra Zona de Disponibilidade possa lidar com as solicitações.

Para garantir que os recursos sejam distribuídos entre as Zonas de Disponibilidade de uma região, a AWS mapeia independentemente as Zonas de Disponibilidade para nomes de cada conta da AWS.

Por exemplo, a Zona de Disponibilidade us-east-1a para sua conta da AWS pode não ser a mesma localização que us-east-1a para outra conta da AWS.

Para coordenar as zonas de disponibilidade entre contas, use o *ID da AZ* que é um identificador exclusivo e consistente para uma zona de disponibilidade.Por exemplo,`use1-az2` é uma ID AZ para a `us-east-1` região e tem a mesma localização em todas as AWS contas.

### CloudFront

![regional-edge-caches.png](images/regional-edge-caches.png)

## 2.1 Modelo de responsabilidade compartilhada da AWS

O modelo de responsabilidade compartilhada da AWS define o que você (como titular/usuário de uma conta AWS) e a AWS são responsáveis no que diz respeito à segurança e conformidade.

- Responsabilidade da AWS: “segurança DA nuvem”: a AWS é responsável por proteger a infraestrutura que executa todos os serviços oferecidos na Nuvem AWS. Essa infraestrutura é composta por hardware, software, redes e instalações que executam os Serviços de nuvem AWS.
- Responsabilidade do cliente: “segurança NA nuvem”: a responsabilidade do cliente será determinada pelos Serviços de nuvem AWS selecionados por ele.

![00.2_shared-responsibility-model_PT-BR.png](images/00.2_shared-responsibility-model_PT-BR.png)

## 3.3 EC2

O Amazon Elastic Compute Cloud (Amazon EC2) é um serviço de **virtualização** na nuvem da AWS, sendo um dos principais serviços da AWS.

### Hypervisor

Um hipervisor é um hardware, software ou firmware que cria e gerencia máquinas virtuais e aloca recursos a elas.

![vm-docker.png](images/vm-docker.png)

![docker.png](images/docker.png)

### Tipos de instância do Amazon EC2

**Nomenclatura para classificação de instâncias**

- **Instâncias de Uso Geral (A, T, M)**
- **Instâncias Otimizadas para Computação (C)**
- **Instâncias Otimizadas para Memória (R, X, U, Z)**
- **Instâncias Otimizadas para Armazenamento (D, I, H)**
  - Começam com I(IOPS) e D

### Modelos de preço EC2

- **On Demand**
  - As instâncias sob demanda permitem que você pague pela capacidade computacional **por hora ou segundo**, sem nenhum compromisso de longo prazo.
- **Reserva de capacidade sob demanda**
  - Permitem que você reserve capacidade de computação para suas instâncias do EC2 em uma zona de disponibilidade específica por **qualquer duração**. As reservas de capacidade reduzem o risco de não conseguir obter capacidade sob demanda em caso de restrições de capacidade e garantem que você sempre tenha acesso à capacidade do EC2 quando precisar.
- **Spot**
  - Instâncias EC2 menos estáveis, ofertadas com base na **oferta e demanda**, quando sua solicitação Spot for atendida, suas Instâncias Spot serão lançadas no preço Spot atual, não excedendo o preço On Demand.
- **Dedicated**
  - Hardware físico dedicado especificamente para sua aplicação, utilizado por empresas que por questões de conformidade e regulação, necessitem de ter um hardware único e não compartilhado, para armazenamento de dados (Financeiro/Governos)
- **Saving Plans**
  - Menor custo que On Demand, pelo compromisso com uma quantidade consistente de uso (medida em $/hora) por um período de 1 ou 3 anos. Existem 3 tipos de Saving Plans
    - **Compute Savings Plans**
      - Os Compute Savings Plans fornecem a **maior flexibilidade**. Esses planos se aplicam automaticamente ao uso da instância do EC2, **independentemente de família de instâncias**, tamanho, AZ, região, sistema operacional ou locação da instância, e também se aplicam ao uso do **Fargate ou Lambda**.
    - **EC2 Instance Savings Plans**
      - Os EC2 Instance Savings Plans fornecem os preços mais baixos em troca do comprometimento com o uso de **famílias de instâncias** individuais em uma região (por exemplo, usar M5 no Norte da Virginia). Isso reduz automaticamente seu custo na **família de instâncias selecionadas nessa região**, qualquer que seja a AZ, o tamanho, o sistema operacional ou a locação.
    - **Amazon SageMaker Savings Plans**
      - O mesmo do Compute Savings Plans, porém para uso de instâncias tipos ML(Machine Learning)

## 2.4 Security Groups e ACLs(Firewalls)

As **Listas de Controle de Acesso à Rede (ACLs)** fornecem uma camada de firewall/segurança no nível de sub-rede.

Os **Security Groups** fornecem uma camada de firewall/segurança no nível de instância.

A tabela abaixo descreve algumas diferenças entre **Security Groups** e **Network ACLs**:

| **GRUPOS DE SEGURANÇA**                                          | **LISTA DE CONTROLE DE ACESSO À REDE (NACLs)**        |
| ---------------------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------- |
| Aplica-se a **uma** **instância** apenas se associada a um grupo | Aplica-se automaticamente a **todas as instâncias**   | nas sub-redes com as quais está associada |
| Opera no nível de **instância** (interface)                      | Opera no nível de sub-rede                            |
| Avalia todas as regras                                           | Processa as regras na ordem                           |
| **Stateful** (se foi permitido entrar, é permitido sair)         | **Stateless** (precisa de uma regra de entrada/saida) |
| Suporta apenas **regras de permissão**                           | Suporta **regras de permissão e negação**             |

![states.png](images/stateless_full.png)

## 3.6 Serviços de armazenamento da AWS

O Amazon Elastic Block Store (EBS) é um serviço de armazenamento de alto desempenho oferecido pela AWS para uso com Amazon Elastic Compute Cloud (EC2). Ele foi projetado para aplicativos que exigem armazenamento de baixa latência para ler e escrever dados em blocos.

Aqui estão algumas características principais do EBS:

1. **Desempenho de Armazenamento**: EBS fornece armazenamento em bloco de alto desempenho que pode ser anexado a uma instância EC2. Os volumes EBS são otimizados para cargas de trabalho que exigem operações de E/S de baixa latência, como bancos de dados e aplicativos que exigem muita E/S.
2. **Durabilidade**: O EBS é projetado para durabilidade. **Os volumes EBS são automaticamente replicados em sua zona de disponibilidade** para proteger contra falhas de componentes, proporcionando alta disponibilidade e durabilidade.
3. **Tipos de Volume**: EBS oferece vários tipos de volume para atender às necessidades de armazenamento e desempenho. Isso inclui os volumes SSD-backed para cargas de trabalho transacionais de uso geral **(gp2 e gp3)** e de alto desempenho **(io1 e io2)**, e os volumes HDD-backed para cargas de trabalho throughput intensivas **(st1 e sc1)**.
4. **Backup com Snapshots**: O EBS oferece a capacidade de criar **snapshots (cópias)** dos seus volumes, que são armazenados no **Amazon S3** para durabilidade. Esses snapshots podem ser usados para criar novos volumes EBS ou para aumentar o tamanho do volume.
5. **Criptografia**: O EBS oferece a opção de criar volumes criptografados e controlar as chaves de criptografia usando o AWS Key Management Service (KMS). Isso ajuda a atender aos requisitos de conformidade e segurança.
6. **Integração com a AWS**: EBS é profundamente integrado com outros serviços da AWS, como Amazon CloudWatch para monitoramento, AWS Identity and Access Management (IAM) para controle de acesso, e AWS Snapshot Scheduler para automação de backup.

Em resumo, o Amazon EBS é uma solução de armazenamento em bloco de alto desempenho que é fundamental para muitas aplicações em execução na AWS devido à sua durabilidade, flexibilidade e integração com a AWS.

### Armazenamento de instância (Instance store)

- Os volumes da store de instâncias são **discos locais** de alta performance **fisicamente** conectados ao computador host em que uma instância EC2 é executada.
- As stores de instâncias são efêmeras, o que significa que os dados são perdidos quando desligados (não persistentes).
- As stores de instâncias são ideais para o armazenamento temporário de informações que mudam com frequência, como buffers, caches ou dados temporários.
- Os volumes da store de instâncias raiz são criados a partir de modelos de AMI armazenados no S3.
- Os volumes da store de instâncias não podem ser destacados/reattached.

## Amazon EFS e FSX

O **Amazon Elastic File System (EFS)** é um serviço de armazenamento de arquivos totalmente gerenciado que facilita a configuração e o dimensionamento de sistemas de arquivos em nuvem na AWS. O EFS foi projetado para ser altamente disponível, durável e seguro, e pode ser usado com uma ampla gama de serviços da AWS e aplicações on-premise.

Aqui estão alguns pontos-chave sobre o Amazon EFS:

1. **Escalabilidade**: O EFS é projetado para escalar automaticamente para acomodar o crescimento dos dados, de alguns gigabytes a petabytes, sem a necessidade de provisionar o armazenamento.
2. **Alta Disponibilidade e Durabilidade**: O EFS armazena automaticamente os arquivos em vários dispositivos dentro e entre várias zonas de disponibilidade para garantir a disponibilidade e durabilidade dos dados.
3. **Compartilhamento de Arquivos**: O EFS suporta o compartilhamento de arquivos entre várias instâncias do Amazon EC2, permitindo que múltiplos servidores acessem um sistema de arquivos simultaneamente.
4. **Integração com AWS**: O EFS pode ser integrado a outros serviços da AWS, como o AWS Backup para backups automatizados e o AWS IAM para controle de acesso.
5. **Tipos de armazenamento**: O EFS oferece várias classes de armazenamento, incluindo Standard e Infrequent Access (IA), permitindo que você otimize os custos com base em seus padrões de acesso aos arquivos.
6. **Segurança**: O EFS inclui suporte para criptografia de dados em repouso e em trânsito, bem como integração com o AWS Key Management Service (KMS) para gerenciamento de chaves de criptografia.

Resumindo, o Amazon EFS é uma solução de armazenamento de arquivos escalável, de alta disponibilidade e segura, que facilita o compartilhamento de arquivos entre instâncias EC2 e outros serviços AWS.

O **Amazon FSx** é um serviço de armazenamento de arquivos totalmente gerenciado da AWS que facilita o lançamento e a execução de sistemas de arquivos de terceiros. O FSx fornece o rico conjunto de recursos e a rápida performance que esses tipos de aplicativos precisam, e atualmente suporta dois sistemas de arquivos: **Windows File Server** para aplicações baseadas em Windows, e **Lustre** para cargas de trabalho de computação intensiva.

Aqui estão alguns pontos chave sobre o Amazon FSx:

1. **FSx para Windows File Server**: Ele fornece um sistema de arquivos nativamente compatível com o Windows, permitindo que você mova com facilidade as aplicações baseadas em Windows que exigem o sistema de arquivos do Windows para a AWS. É construído sobre o Windows Server e oferece suporte a recursos como de duplicação de dados, criptografia de dados em repouso, e acesso via SMB (Server Message Block) e NFS (Network File System).
2. **FSx para Lustre**: O Lustre é um sistema de arquivos popular para cargas de trabalho de computação intensiva, como análise de big data, modelagem de machine learning e processamento de mídia. O FSx para Lustre é totalmente gerenciado pela AWS, simplificando o processo de criação e execução de um sistema de arquivos Lustre.
3. **Desempenho**: O Amazon FSx foi projetado para oferecer o desempenho rápido necessário para suportar aplicações exigentes. Ele fornece baixa latência e altas taxas de transferência de dados.
4. **Compatibilidade e Integração**: O Amazon FSx é totalmente compatível com os sistemas de arquivos que suporta, o que significa que você pode usar suas ferramentas e aplicações existentes sem modificação. Além disso, o FSx se integra com uma série de outros serviços AWS para coisas como backup, monitoramento e acesso seguro a arquivos.
5. **Segurança**: O Amazon FSx oferece várias funcionalidades de segurança, como a capacidade de armazenar dados em redes virtuais privadas da Amazon (VPCs), suporte a redes de acesso (ACLs) para o Windows File Server, criptografia de dados em repouso e em trânsito, e integração com AWS Key Management Service (KMS) para gerenciamento de chaves de criptografia.

Em resumo, o Amazon FSx é um serviço poderoso e flexível que torna mais fácil do que nunca para você executar sistemas de arquivos totalmente gerenciados na AWS. Ele suporta sistemas de arquivos Windows e Lustre, oferecendo um alto nível de desempenho, segurança e integração com outros serviços AWS.

- **IMPORTANTE!**
  EFS é para Linux, FSx para Windows

## Amazon S3

O Amazon S3 é um armazenamento de objetos projetado para armazenar e recuperar qualquer quantidade de dados de qualquer lugar – sites e aplicativos móveis, aplicativos corporativos e **dados de sensores ou dispositivos IoT**.

- Você pode armazenar qualquer tipo de arquivo no S3.
- Os arquivos podem ter de 0 bytes a 5 TB.
- Não há limite de armazenamento disponível.
- Os arquivos são armazenados em buckets e são chamados de objetos.
- Buckets são pastas de nível raiz.
- Qualquer subpasta em um bucket, é conhecida como “pasta”.
- O S3 é um namespace universal, então os nomes de buckets devem ser exclusivos globalmente.
- Ao criar um bucket, você precisa selecionar a região onde ele será criado.

**Atenção**: Enquanto o Amazon S3 é um serviço global, o Bucket S3 é um serviço regional.

**Existem oito classes de armazenamento do S3:**

1. S3 Padrão (durável, imediatamente disponível, acessado com frequência).
2. S3 Intelligent-Tiering (move automaticamente dados para a camada mais econômica).
3. S3 Padrão-IA (durável, imediatamente disponível, acessado com pouca frequência).
4. S3 One Zone-IA (custo mais baixo para dados acessados com pouca frequência, com menos resiliência).
5. S3 Glacier Instant Retrieval (dados raramente acessados e que exigem recuperação em milissegundos).
6. S3 Glacier Flexible Retrieval (dados arquivados, tempos de recuperação em minutos ou horas).
7. S3 Glacier Deep Archive (classe de armazenamento de menor custo para retenção de longo prazo).
8. S3 Outpost (armazenamento de objetos para seu ambiente de AWS Outposts on-premises).

A tabela a seguir fornece uma descrição de armazenamentos de dados persistentes, transitórios e efêmeros e qual serviço da AWS usar:

| **TIPO DE ARMAZENAMENTO** | **DESCRIÇÃO**                                                                                             | **EXEMPLOS**                              |
| ------------------------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| Persistente               | Dados são duráveis e permanecem após reinicializações, reinícios ou ciclos de energia.                    | S3, Glacier, EBS, EFS                     |
| Transitório               | Dados são apenas armazenados temporariamente e passados para outro processo ou armazenamento persistente. | SQS, SNS                                  |
| Efêmero                   | Dados são perdidos quando o sistema é desligado.                                                          | Armazenamento de Instância EC2, Memcached |

## AWS Storage Gateway

![types-of-aws-gateway.jpg](images/types-of-aws-gateway.jpg)

## 3.3 ASG e ALB

Diferença entre Escalabilidade, elasticidade e disponibilidade

- **Escalabilidade**

  - Horizontal
    - Scale out: inicia novas instâncias
    - Scale in: termina novas instâncias
  - Vertical
    - Scale up: melhorar as instâncias

- **Elasticidade**
  Capacidade de **dimensionamento**(dimensionar) automaticamente as mudanças conforme a demanda.
  Como se fosse literalmente um elástico.
  - Horizontal
    - Capacidade de diminuir(scale-in) ou aumentar (scale-out) automaticamente de acordo com a necessidade
  - Vertical
    - Capacidade de melhorar(scale-up) ou diminuir (scale-down) os recursos de uma instância
- **Disponibilidade**
  Capacidade de espalhar os recursos ou servidores(instâncias) em varias zonas de disponibilidade(AZs)
  ![Elastic ASG.jpg](images/Elastic%20ASG.jpg)

### **Amazon EC2 Auto Scaling**

O **Amazon EC2 Auto Scaling** automatiza o processo de lançamento (escalonamento para fora) e término (escalonamento para dentro) de instâncias Amazon EC2 com base na demanda de tráfego para sua aplicação.

> _O Amazon EC2 Auto Scaling fornece elasticidade e escalabilidade._

Você cria **coleções** de instâncias EC2, chamadas de grupo Auto Scaling (ASG).

Você pode especificar um **número mínimo**, **desejado** e **máximo** de instâncias em cada ASG.

Por exemplo, o seguinte grupo do Auto Scaling tem um tamanho mínimo de uma (01) instância, uma capacidade desejada de duas (02) instâncias e um tamanho máximo de quatro (04) instâncias.

![ASG-AWS.png](images/ASG-AWS.png)

**Políticas de Escalabilidade**

As políticas de escalabilidade que você define ajustam o número de instâncias, dentro dos limites mínimo e máximo de instâncias, com base nos critérios que você especifica.

As políticas de dimensionamento determinam quando, se e como o ASG escala e diminui, usando:

- **Escalonamento dinâmico/on-demand:** Ajusta a quantidade de instâncias em resposta a mudanças na demanda.
- **Escalonamento cíclico/agendado:** Ajusta a quantidade de instâncias em horários específicos, de acordo com um cronograma.

**Planos de Dimensionamento**

Os Planos de Dimensionamento definem os gatilhos e momentos em que as instâncias devem ser provisionadas ou desprovisionadas.

Você pode especificar políticas de dimensionamento que controlam quando o Auto Scaling inicia ou termina instâncias.

### **Amazon Elastic Load Balancing (ELB)**

O Amazon Elastic Load Balancing (ELB) distribui automaticamente o tráfego de aplicativos recebido entre vários destinos, como **instâncias Amazon EC2**, **contêineres** e **endereços IP**.

O ELB pode lidar com a carga variável do tráfego da sua aplicação em **várias Zonas de Disponibilidade**.

Ele também possui alta disponibilidade, dimensionamento automático e segurança robusta necessária para tornar suas aplicações tolerantes a falhas.

> _Existem três tipos de Balanceador de Carga Elástico (ELB) na AWS:_

![types elb.jpeg](images/types%20elb.jpeg)

## 3.4 Serviços de banco de dados na AWS

![TIPOS DE BANCO DE DADOS!](images/tipos-de-banco-de-dados-aws.jpg)

TIPOS DE BANCO DE DADOS!

### **Amazon Relational Database Service (RDS)**

O Amazon Relational Database Service (Amazon RDS) é um **serviço gerenciado** que facilita a configuração, operação e escalabilidade de um banco de dados relacional na nuvem.

> _RDS é um tipo de banco de dados Online Transaction Processing (OLTP)._

> O Amazon RDS é um serviço totalmente gerenciado e você não tem acesso à instância EC2 subjacente (sem acesso ao root).

**Mecanismos de Banco de Dados Suportados no Amazon RDS**

1. IBM db2
2. MySQL
3. PostgreSQL
4. Microsoft SQL Server
5. Oracle
6. MariaDB

O **Amazon Aurora**, apesar de estar sendo demonstrado como **mecanismo** no **Amazon RDS**, ele é um serviço de propriedade AWS, e utiliza seu **próprio mecanismo para gerenciar** um banco de dados relacional MySQL e PostgreSQL.

**O Serviço RDS Inclui:**

- Segurança e atualização das instâncias de banco de dados.
- Backup automático para as instâncias de banco de dados.
- Atualizações de software para o mecanismo de banco de dados.
- Escalonamento fácil para armazenamento e computação.
- **Opção** Multi-AZ com replicação síncrona.
- Failover automático para opção Multi-AZ.
- Horas de instância do banco de dados (horas parciais são cobradas como horas completas).
- Opção de réplicas de leitura para cargas de trabalho de leitura intensiva.
- As réplicas de leitura são usadas para bancos de dados com muitas leituras e a replicação é assíncrona.
- Réplicas de leitura são para compartilhamento de carga de trabalho e alívio de carga.

**Escalabilidade:**

- Você só pode **escalar o RDS para cima** (computação e armazenamento).
- Você não pode **diminuir o armazenamento alocado** para uma instância do RDS.
- Você pode escalar o armazenamento e alterar o tipo de armazenamento para todos os mecanismos de banco de dados, exceto o MS SQL.

### **Amazon ElastiCache**

ElastiCache é um serviço web que facilita a implantação e execução de nós de servidor compatíveis com os protocolos Memcached ou Redis na nuvem.

- Cache em memória que melhora significativamente a latência e o throughput para muitas cargas de trabalho de aplicativos voltadas para leitura ou cargas de trabalho intensivas de computação(ML/IA).
- Melhor para cenários em que a carga do banco de dados é baseada em transações de Processamento Analítico Online (OLAP).
- Os nós EC2 ElastiCache não podem ser acessados pela Internet, nem podem ser acessados por instâncias EC2 em outras VPCs.
- Pode ser em instâncias sob demanda ou reservadas (mas não em instâncias Spot).

| **CASOS DE USO**                  | **BENEFÍCIOS**                                                                                                                                                                                                                |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Armazenamento de Sessão Web       | Em casos com servidores web equilibrados, armazene informações de sessão na **Redis**, para que, **se um servidor for perdido**, as **informações da sessão** não sejam perdidas e **outro servidor web possa recuperá-las**. |
| Cache de Banco de Dados           | Use o Memcached na frente do AWS RDS para armazenar consultas populares para aliviar o trabalho do RDS e retornar resultados mais rapidamente aos usuários.                                                                   |
| Quadros de Classificação          | Use o Redis para fornecer um quadro de classificação ao vivo para milhões de usuários do seu aplicativo móvel.                                                                                                                |
| Dashboards de Dados em Tempo Real | Forneça um local para dados de sensores em tempo real no chão de fábrica, fornecendo displays de painel ao vivo em tempo real.                                                                                                |

**Existem dois tipos de mecanismos do ElastiCache:**

1. **Memcached**: modelo mais simples, pode executar grandes nós com vários núcleos/tarefas, pode ser dimensionado para cima e para baixo, pode armazenar objetos como bancos de dados.
2. **Redis**: modelo mais complexo, suporta criptografia, replicação mestre/escravo, cross-AZ (alta disponibilidade), failover automático e backup/restauração.

## **Amazon DynamoDB**

Amazon DynamoDB é um serviço de banco de dados NoSQL totalmente gerenciado que oferece desempenho rápido e previsível com escalabilidade contínua.

**Características do DynamoDB**

1. Baseado em SSD e usa indexação limitada em atributos para desempenho.
2. Usa HTTP sobre SSL (HTTPS) como transporte e JSON como formato de serialização de mensagem.
3. Armazena três réplicas geograficamente distribuídas de cada tabela para alta disponibilidade e durabilidade de dados.
4. Replicação síncrona em três instalações (AZs) em uma região.
5. Escala armazenamento e throughput para cima ou para baixo conforme necessário sem alterações de código ou tempo de inatividade.

**Fornece dois modelos de leitura:**

- **Leituras eventualmente consistentes (padrão)**:A opção de consistência eventual maximiza seu throughput de leitura (melhor desempenho de leitura).Uma leitura eventualmente consistente **pode não refletir os resultados de uma gravação concluída recentemente**. Consistência em todas as cópias alcançada dentro de 1 segundo.
- **Leituras fortemente consistentes:** Uma leitura fortemente consistente retorna um resultado **que reflete todas as gravações** que receberam uma resposta bem-sucedida antes da leitura (consistência mais rápida).

## Data Analytics Reference/Processo

![data_analytics](images/data_analytics.png)

EMR:Amazon Elastic MapReduce
SageMaker: Modelos de ML

![oltp.png](images/oltp.png)

![dados.png](images/dados.png)

**O OLAP é otimizado para análises e relatórios de dados complexos, enquanto o OLTP é otimizado para processamento transacional e atualizações em tempo real.**

## 3.5 Serviços de rede da AWS

### VPC (Virtual Private Cloud)

Um *Amazon Virtual Private Cloud (VPC)* é uma rede virtual dedicada à sua conta AWS. Ele é logicamente isolado de outras redes virtuais na AWS Cloud.

> _Use como analogia, ter seu próprio data center dentro da AWS._

O seguinte diagrama mostra uma VPC, que possui uma sub-rede em cada zona de disponibilidade na região, instâncias do EC2 em cada sub-rede e um gateway da Internet para permitir a comunicação **entre os recursos em sua VPC e a Internet:**

![amazon-vpc.png](images/amazon-vpc.png)

1. Quando você cria sua conta AWS pela primeira vez, uma VPC padrão é criada para você em cada região AWS, com uma sub-rede em cada AZ (zona de disponibilidade).
2. Uma VPC abrange todas as Zonas de Disponibilidade (AZ) na região.
3. Oferece controle total sobre o ambiente de rede virtual, incluindo seleção de intervalos de IP, criação de sub-redes e configuração de tabelas de roteamento e gateways.
4. Você pode **criar seus próprios intervalos de endereços IP** e **criar sub-redes**, **tabelas de roteamento** e **gateways de rede**.

A VPC padrão possui **todas as sub-redes públicas.**

As **sub-redes públicas** são sub-redes que têm:

- “Auto-atribuir endereço IPv4 público” definido como “Sim”.
- A tabela de roteamento da sub-rede tem um Gateway de Internet anexado.

As **instâncias na VPC padrão** sempre têm tanto um endereço IP **público** quanto um endereço IP **privado**.

**Componentes de uma VPC**

- **Virtual Private Cloud:** Uma rede virtual logicamente isolada na AWS. Você define o espaço de endereço IP de uma VPC a partir dos intervalos que você seleciona.
- **Subnet:** Um segmento do intervalo de endereços IP de uma VPC onde você pode colocar grupos de recursos isolados (um para um mapeamento com uma AZ).
- **Internet Gateway:** A parte da Amazon VPC de uma conexão com a Internet pública.
- **NAT Gateway:** Um serviço de Tradução de Endereço de Rede (NAT) gerenciado e altamente disponível para seus recursos em uma sub-rede privada acessarem a Internet.
- **Conexão VPN de hardware:** Uma conexão VPN baseada em hardware entre sua Amazon VPC e seu data center, rede doméstica ou instalação de co-localização.
- **Virtual Private Gateway:** A parte da Amazon VPC de uma conexão VPN.
- **Customer Gateway:** Sua parte de uma conexão VPN.
- **Roteador:** Roteadores interconectam sub-redes e direcionam o tráfego entre Gateways de Internet, Gateways Privados Virtuais, Gateways NAT e sub-redes.
- **Conexão de Interligação:** Uma conexão de interligação permite que você roteie o tráfego via endereços IP privados entre duas VPCs interligadas.
- **Pontos de Extremidade da VPC:** Permitem conectividade privada a serviços hospedados na AWS, de dentro da sua VPC, sem usar um Gateway de Internet, VPN, dispositivos de Tradução de Endereços de Rede (NAT) ou proxies de firewall.
- **Gateway de Internet somente de saída:** Um gateway com estado para fornecer acesso de saída somente para o tráfego IPv6 da VPC para a Internet.

## Resumo VPC

![vpc_resumo](images/VPC.jpg)

### VPC Endpoint

Existem três tipos de endpoints da VPC:

- **_endpoints de interface_**
- **_endpoints de gateway_**
- **endpoints de balanceador de carga de gateway**

Os endpoints de interface e endpoints de balanceador de carga de gateway são desenvolvidos pelo **AWS PrivateLink** e usam uma interface de rede elástica (**ENI**) como ponto de entrada para o tráfego destinado ao serviço.
Os endpoints de interface normalmente são acessados usando o nome DNS público ou privado associado ao serviço, enquanto os endpoints de gateway e endpoints de balanceador de carga de gateway funcionam como **destino para uma rota na tabela de rotas** para o tráfego destinado ao serviço.

![vpc_endpoint](images/vpc_endpoint.jpg)

### AWS PrivateLink

O **AWS PrivateLink** fornece conectividade privada entre **nuvens privadas virtuais (VPCs), serviços da AWS ou terceiros, Marketplace e suas redes on-premises** **sem expor seu tráfego à Internet pública**.

O PrivateLink utiliza ENI (Elastic Network Interface) que funcionam como um NIC(em Inglês, cartão de rede virtual) que é uma representação virtual de uma placa de rede física.

> ENIs podem ser anexadas e desanexadas de instâncias EC2, e a configuração da ENI será mantida.

![private_link](images/PrivateLink.png)

## **Client e Site to Site VPN**

![vpn](images/VPN.png)

## **AWS Direct Connect (DX)**

![aws-direct-connect.jpg](images/aws-direct-connect.jpg)

O **AWS Direct Connect** é um serviço de rede que fornece uma alternativa ao uso da Internet para conectar os locais no local do cliente à AWS.
Os dados são transmitidos por meio de uma conexão de rede privada entre a AWS e o centro de dados ou rede corporativa do cliente.

Cada conexão **AWS Direct Connect** pode ser configurada com uma ou mais **interfaces virtuais** (VIFs).

- As VIFs públicas permitem acesso a serviços públicos como S3, EC2 e DynamoDB.
- As VIFs privadas permitem acesso à sua VPC.

> _As tabelas de roteamento precisam ser atualizadas para apontar para uma conexão Direct Connect._

## AWS Transit Gateway

O AWS Transit Gateway conecta suas Amazon Virtual Private Clouds (VPCs) e redes on-premises por meio de um hub central. Essa conexão simplifica a rede e elimina os complexos relacionamentos de emparelhamento. O Transit Gateway atua como um roteador de nuvem altamente escalável.

<p float="left">
  <img src="images/AWS-Transit-Gateway-Architecture.png" width="400" />
  <img src="images/transitgateway.jpg" width="400" /> 
</p>

## Amazon Route 53

O Amazon Route 53 é o sistema de nome de domínio (**DNS**) da AWS, e possui três funções principais.

- **_Registro de domínio_**: Permite que você registre nomes de domínio),
- **_DNS roteamento_**: Traduz nomes em endereços IP usando uma rede global de servidores DNS autoritativos.
- **_Verificação de integridade_**: Envia solicitações automatizadas para sua aplicação para verificar se ela é alcançável, está disponível e funcional.

Você pode usar qualquer combinação dessas funções.

> **_Políticas de Roteamento_**

As políticas de roteamento determinam como o DNS do Route 53 responde às consultas.

A tabela abaixo destaca a principal função de cada tipo de política de roteamento:

| **POLÍTICA DE ROTEAMENTO** | **QUANDO USAR**                                                                                                 |
| -------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Simples                    | Resposta DNS simples fornecendo o endereço IP associado a um nome.                                              |
| Failover                   | Se o primário estiver inativo (com base em verificações de integridade), roteia para o destino secundário.      |
| Geolocalização             | Usa a localização geográfica em que você está (por exemplo, Europa) para roteá-lo para a região mais próxima.   |
| Geoproximidade             | Roteia para a região mais próxima em uma área geográfica.                                                       |
| Latência                   | Direciona com base na rota de menor latência para os recursos.                                                  |
| IP                         | Use quando quiser rotear o tráfego com base no local dos usuários e tiver os endereços IP de origem do tráfego. |
| Resposta Multivalor        | Retorna vários endereços IP e funciona como um balanceador de carga básico.                                     |
| Ponderada                  | Usa os pesos relativos atribuídos aos recursos para determinar para qual rotear.                                |

## AWS Global Accelerator

O AWS Global Accelerator é um serviço que melhora a **disponibilidade** e o **desempenho** de suas aplicações para usuários em todo o mundo.
Ele faz isso usando a _rede global altamente disponível da AWS_ e redirecionando o tráfego de usuários para a aplicação **mais próxima em termos de latência**. Isso resulta em uma melhoria significativa na experiência do usuário.

![global_acelerator](images/globalacelera.png)

## 3.3 Containers

### **Amazon Elastic Container Service (ECS)**

O Amazon Elastic Container Service (ECS) fornece um serviço de **gerenciamento de contêiner** altamente escalável e de alto desempenho que suporta contêineres Docker e permite executar facilmente aplicativos em um cluster gerenciado de instâncias Amazon EC2.

O Amazon ECS elimina a necessidade de instalar, operar e dimensionar sua própria **infraestrutura** de gerenciamento de cluster.

Um **_tipo de lançamento_** do Amazon ECS determina o **tipo de infraestrutura** em que suas tarefas e serviços são hospedados

> Existem dois tipos de lançamento:
>
> | **Amazon EC2**                                                     | **Amazon Fargate**                                                           |
> | ------------------------------------------------------------------ | ---------------------------------------------------------------------------- |
> | Você provisiona explicitamente instâncias EC2                      | O plano de controle solicita recursos e o Fargate provisiona automaticamente |
> | Você é responsável pela atualização, patching, cuidado do pool EC2 | O Fargate provisiona computação conforme necessário                          |
> | Você deve lidar com a otimização do cluster                        | O Fargate lida com a otimização do cluster                                   |
> | Mais controle granular sobre a infraestrutura                      | Controle limitado, pois a infraestrutura é automatizada                      |

### Amazon Elastic Container Registry (ECR)

O Registro de Contêiner Elástico (ECR) é um serviço gerenciado da AWS Docker Registry para armazenar, gerenciar e implantar imagens **Docker**.

### Amazon Elastic Kubernetes Service (EKS)

O Amazon Elastic Container Service for Kubernetes (EKS) é um **serviço gerenciado de Kubernetes** que facilita a execução do Kubernetes na AWS sem a necessidade de instalar, operar e manter seu próprio **plano de controle do Kubernetes.**

![docker_kubernetes](images/docker_kubernetes.jpg)

## 3.8 Integrações Cloud

### **Amazon SQS (Simple Queue Service)**

- **Mensageria Assíncrona:** Permite que diferentes componentes do sistema se comuniquem de forma assíncrona usando filas de mensagens.
- **Escalabilidade e Resiliência:** Suporta alta taxa de transferência, escalabilidade e resiliência a falhas.

### **Amazon SNS (Simple Notification Service)**

- **Notificação em Tempo Real:** Oferece um serviço de mensagens **publicador-assinante** que permite o envio de notificações em tempo real a vários destinatários.
- **Suporte a Diversos Protocolos:** Suporta HTTP/HTTPS, e-mail, SMS e integração com outros serviços AWS.

### **Amazon EventBridge**

- **Roteamento de Eventos:** Um barramento de eventos que permite a construção de aplicações orientadas a eventos, roteando eventos de diferentes fontes para destinos AWS.
- **Automação e Conectividade:** Facilita a automação de fluxos de trabalho e a conectividade entre serviços e aplicações.

<p float="left">

  <img src="images/sns_sqs.jpg" width="400" />
  <img src="images/sqssns_eventbridge.jpg" width="400" /> 
</p>

## 3.3 Computação e Serverless

### Amazon Batch

O AWS Batch permite executar facilmente centenas de milhares de trabalhos de computação em lote de maneira fácil e eficiente na AWS.

Você simplesmente empacota o código para seus trabalhos em lote, **especifica suas dependências** e envia seu trabalho em lote. O AWS Batch **provisiona dinamicamente** a quantidade e o tipo ideais de recursos de computação(**tipos de instâncias**) com base no volume e nos requisitos específicos de recursos dos trabalhos em lote enviados.

> **_Diferenças entre Lightsail e Beanstalk:_**

- **Lightsail**: Mínima configuração, aplicações web e sites simples, lançamento rápido.
- **Elastic Beanstalk**: Mais configuração, escalabilidade e dimensionamento automático na implementação de aplicações e serviços web.

## 4.2 Cobrança e custos

O **AWS Control Tower** fornece um local único para configurar um ambiente de várias contas bem projetado. Um processo que simplifica a criação e configuração de multiplas contas (**Organizations**) em grandes ambientes.

O **AWS Resource Acess Manager (RAM)** ajuda você a compartilhar seus recursos com **segurança** entre contas da AWS, dentro de sua organização ou unidades organizacionais (UOs) e com perfis e usuários do IAM para tipos de recursos compatíveis.

### AWS Resource Groups e Tag Editor

- As tags são pares de chave/valor que podem ser anexados aos recursos da AWS.
- Contêm metadados (dados sobre dados).
- Às vezes, as tags podem ser herdadas, por exemplo, recursos criados pelo Auto Scaling, CloudFormation ou Elastic Beanstalk.
- Os grupos de recursos facilitam a agrupação de recursos usando as tags atribuídas a eles. É possível agrupar recursos que compartilham uma ou mais tags.
- _Os grupos de recursos contêm informações gerais, como:_
  - Região.
  - Nome.
  - Verificações de saúde.
- _E informações específicas, como:_
  - Endereços IP públicos e privados (para EC2).
  - Configurações de porta (para ELB).
  - Motor do banco de dados (para RDS).

### AWS Service Catalog

O **AWS Service Catalog** é um serviço de gerenciamento de serviços que permite administradores de TI manter um controle firme sobre os serviços da AWS utilizados dentro de suas organizações. Especificando quais serviços os usuários podem lançar e implementar em conformidade com as politicas corporativas, auxiliando assim o controle de custos.

## 1.2 AWS Well-Architected Framework

A AWS Well-Architected ajuda arquitetos de nuvem a construir infraestruturas **seguras**, **resilientes**, **eficientes** e de **alta performance** para aplicações e workloads.
Baseado em seis pilares (**excelência operacional**, **segurança**, **confiabilidade**, **eficiência de performance**, **otimização de custos** e **sustentabilidade**).

> **_Pilares:_**

- **Excelência Operacional**: Foca na execução eficiente das operações diárias de sistemas baseados em nuvem. Para alcançar a excelência operacional, é preciso monitorar continuamente os recursos do sistema e automatizar processos a fim de reduzir a intervenção manual.
  - Definições
    - **Organização**
    - **Preparar**
    - **Operar**
    - **Evoluir**
- **Segurança**: Foca em proteger seus sistemas, dados e ativos contra ameaças internas e externas. Define políticas de seguranças, gestão de identidades, ACLs, SG a serem aplicadas em toda a organização.
  - Definições
    - **Segurança**
    - **Gerenciamento de identidade e acesso**
    - **Detecção**
    - **Proteção de infraestrutura**
    - **Proteção de dados**
    - **Resposta a incidentes**
- **Confiabilidade**: Foca em garantir que os sistemas estejam sempre disponíveis e funcionando corretamente, sejam tolerantes a falhas e recuperáveis de desastres.
- Definições
  - **Fundamentos**
  - **Arquitetura de carga de trabalho**
  - **Gerenciamento de mudanças**
  - **Gerenciamento de falhas**
- **Eficiência de performance**: Inclui a capacidade de usar recursos de computação com eficiência para atender aos requisitos do sistema à medida que a demanda muda, utilizando de caches e balanceadores de carga.
- Definições
  - **Seleção de arquitetura**
  - **Computação e hardware**
  - **Gerenciamento de dados**
  - **Rede e entrega de conteúdo**
  - **Processo e cultura**
- **Otimização de custos**: Foca na capacidade de executar sistemas para proporcionar valor comercial pelo menor preço, monitorando os custos e economizando recursos sem afetar o desempenho ou a confiabilidade do sistema.
- Definições
  - **Pratique o gerenciamento financeiro na nuvem**
  - **Reconhecimento de despesas e usos**
  - **Recursos econômicos**
  - **Gerenciar recursos de demanda e fornecimento**
  - **Otimizar ao longo do tempo**
- **Sustentabilidade**: É um reconhecimento do impacto ambiental da tecnologia em nuvem e visa ajudar os clientes a projetar, implementar e operar suas cargas de trabalho de forma mais sustentável.
- Definições
  - **Escolha de região**
  - **Padrões de comportamento do usuário**
  - **Padrões de software e arquitetura**
  - **Padrões de dados**
  - **Padrões de hardware**
  - **Processo de desenvolvimento de implantação**

## 1.3 CAF

O **AWS Cloud Adoption Framework (AWS CAF)** aproveita a experiência e as práticas recomendadas da AWS para ajudar você nos processos de migração para a Nuvem. 
O **AWS Well Architected** auxilia os Arquitetos de nuvem a construir ferramentas, seguras, resilientes, eficientes e de alta performance para aplicações e workloads.

Os recursos do AWS CAF fornecem orientações de práticas recomendadas que ajudam a melhorar a preparação para a nuvem.

![caf1](images/caf1.jpg)

![caf2](images/caf2.jpg)

## AWS EcoSystem

Juntamente com o AWS IQ(Serviço especialistas terceirizados certificados pela AWS, Freelance)

## AWS Systems Manager

O AWS Systems Manager permite **centralizar** dados operacionais de vários Serviços da AWS e **automatizar** tarefas em todos os recursos da AWS.

### AWS AppConfig

O AWS AppConfig é um **recurso** do Systems Manager, que auxilia na **pré-implantação de alterações de configurações em aplicações**, fornecendo um mecanismo para práticas de implantação, podendo evitar erros em alterações de configuração, implantar alterações em varias destinos e controlar a implantação de alterações em seus aplicativos.

## 2.2 Serviços de Segurança

### AWS Artifact

AWS Artifact fornece downloads sob demanda de documentos de segurança e conformidade, como certificações ISO, leis, normas, frameworks. Você pode enviar os documentos de segurança e conformidade (**_artefatos de auditoria_**) para seus auditores ou reguladores a fim de demonstrar a segurança e a conformidade da infraestrutura da AWS e dos serviços usados por você.
Você também pode usar esses documentos como diretrizes para avaliar sua própria arquitetura de nuvem e a eficácia dos controles internos da empresa.

### AWS GuardDuty

O Amazon GuardDuty combina ML e inteligência de ameaças integrada da AWS para oferecer um **serviço de detecção de ameaças que monitora**, analisa e processa fontes de dados da AWS e registros em seu ambiente. Como por exemplo:

- **Eventos do AWS CloudTrail:** GuardDuty analisa eventos do AWS CloudTrail para detecção de ameaças.
- **Proteção contra Malware no Amazon Elastic Block Store (EBS):** Lançou a proteção contra malware no Amazon EBS para escanear arquivos maliciosos em instâncias EC2 ou cargas de trabalho de contêineres usando volumes EBS.

S3 Buckets, VPC, Route 53 etc.

### AWS Shield

O **AWS Shield** é um serviço gerenciado de proteção contra negação de serviço distribuído (DDoS). Salvaguarda aplicativos da web em execução na AWS com detecção sempre ativa e mitigação automática em linha.

Ajuda a minimizar a indisponibilidade e latência do aplicativo.

### AWS CloudHSM

O **AWS CloudHSM** é um módulo de segurança de **hardware** (HSM) baseado em nuvem que permite gerar e usar facilmente suas próprias chaves de **criptografia** na Nuvem AWS.

### AWS Inspector

O Amazon Inspector é um **serviço automatizado de gerenciamento de vulnerabilidade** que verifica continuamente as workloads da AWS em busca de vulnerabilidades de software e exposição não intencional à rede.

### AWS Secrets Manager

O Secrets Manager ajuda você a **gerenciar o acesso a aplicações, serviços e recursos de TI**, permitindo alternar, gerenciar e recuperar facilmente credenciais de banco de dados, chaves de APIs. Usando as policies do IAM para gerenciar o acesso aos seus segredos.

### AWS Security Hub

O AWS Security Hub é um serviço de **gerenciamento do procedimento de segurança na nuvem** (CSPM) que executa verificações de práticas recomendadas de segurança, agrega alertas e possibilita a automação de verificações e correções.

### AWS Detective

O Amazon Detective simplifica o processo de investigação e ajuda as equipes de segurança a conduzir investigações mais rápidas e eficazes. Com as agregações de serviços de segurança, resumos e contexto de dados pré-construídos do Amazon Detective, você pode analisar e determinar rapidamente a natureza e a extensão de possíveis problemas de segurança.

### AWS Macie

O Amazon Macie é um serviço de segurança de dados que descobre dados confidenciais usando machine learning e correspondência de padrões, fornece visibilidade dos riscos de segurança dos dados e possibilita proteção automatizada contra esses riscos.

## Ferramentas do Desenvolvedor

- **AWS Cloud9** IDE hospedada na AWS com o CLI e acesso direto a serviços na nuvem.
- **AWS CLI**(**Command Line Interface**) ferramenta unificada para o gerenciamento e automação via scripts no terminal.
- **AWS CloudShell** é um shell disponível diretamente no Console AWS que fornece um ambiente pré-autenticado e pré-configurado para executar a interação com recursos da AWS.

### AWS CodeArtifact

AWS CodeArtifact é um **serviço de repositório de artefatos** seguro, altamente escalável e gerenciado que ajuda as organizações a armazenar e compartilhar pacotes de software para desenvolvimento de aplicativos. Você pode compartilhar pacotes privados com segurança entre organizações, ou buscar em repositorios publicos como o npm Registry. Compativel com ferramentas de compilação e gerenciadores de pacote, como Maven, Gradle, npm, yarn, etc.

### AWS CodeCommit

AWS CodeCommit é um **serviço de controle de código-fonte** totalmente gerenciado, seguro e altamente escalável que hospeda repositórios privados do Git.

### AWS CodeBuild

O AWS CodeBuild é um **serviço de integração contínua** totalmente gerenciado que compila código-fonte, executa testes e produz pacotes de software prontos para implantação.

### AWS CodeDeploy

AWS CodeDeploy é um **serviço de implantação totalmente gerenciado que automatiza implantações de software** em uma variedade de serviços de computação, como Amazon EC2, AWS Lambda e servidores locais, facilitando a liberação de novos recursos, e evitando inatividade.

### AWS CodePipeline

O AWS CodePipeline é um **serviço totalmente gerenciado de entrega contínua** que ajuda a automatizar pipelines de CI/CD para oferecer atualizações rápidas e confiáveis de aplicações e infraestruturas.

### AWS CodeStar

O AWS CodeStar **permite que você desenvolva, crie e implante rapidamente aplicações na AWS**. O AWS CodeStar disponibiliza uma interface de usuário unificada, permitindo que você gerencie facilmente suas atividades de desenvolvimento de software em um só lugar. Com o AWS CodeStar, é possível configurar toda a sua cadeia de ferramentas de [entrega contínua](https://aws.amazon.com/devops/continuous-delivery/) em questão de minutos, possibilitando que você comece o lançamento de códigos mais rapidamente.

### AWS X-Ray

AWS X-Ray ajuda os desenvolvedores a **analisar e depurar aplicativos distribuídos em produção**, fornece uma visão completa das solicitações à medida que elas percorrem sua aplicação e filtra dados visuais em cargas úteis, funções, rastreamentos, serviços, APIs e muito mais com movimentos sem código e com pouco código.

## 3.7 Serviços de ML/IA

### AWS Transcribe

- Adicione capacidades de transcrição de fala a aplicações.
- A fala gravada pode ser convertida em texto antes de ser utilizada em aplicações.
- Utiliza um processo de aprendizado profundo chamado Reconhecimento Automático de Fala (ASR) para converter fala em texto de maneira rápida e precisa.

### AWS Rekognition

- Adicione análise de imagem e vídeo às suas aplicações.
- Identifique objetos, pessoas, texto, cenários e atividades em imagens e vídeos.
- Processa vídeos armazenados em um bucket Amazon S3.
- Publique o status de conclusão em um tópico Amazon SNS.

