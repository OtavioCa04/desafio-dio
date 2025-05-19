# Desafio DIO - Criação de Máquina Virtual no Microsoft Azure

## Objetivo

Este repositório foi criado como parte do desafio proposto pela DIO para a prática de criação e configuração de uma Máquina Virtual (VM) na plataforma Microsoft Azure. O objetivo principal é documentar o processo de criação da VM, registrar aprendizados e fornecer um guia de referência para futuras implementações.

## Etapas Realizadas

### 1. Acesso ao Portal do Azure

Acesse o portal oficial do Microsoft Azure em:  
https://portal.azure.com

É necessário estar logado com uma conta Microsoft com acesso ao Azure (pode ser uma conta gratuita para testes).

---

### 2. Criação de um Grupo de Recursos

Antes de criar a máquina virtual, criei um **grupo de recursos** para organizar os recursos relacionados.

- Naveguei até "Grupos de Recursos" no menu lateral
- Cliquei em "Criar"
- Informei:
  - Nome: `grupo-vm-estudos`
  - Região: `Brazil South`
- Cliquei em "Revisar + criar" e depois em "Criar"

---

### 3. Criação da Máquina Virtual

Em seguida, criei a VM:

- Acessei a opção "Máquinas Virtuais" no menu lateral
- Cliquei em "Criar"
- Preenchi as informações básicas:

  - **Assinatura**: Padrão
  - **Grupo de recursos**: `grupo-vm-estudos`
  - **Nome da máquina virtual**: `vm-estudos-dio`
  - **Região**: `Brazil South`
  - **Imagem**: Windows Server 2019 Datacenter (padrão, mas pode ser outra imagem)
  - **Tamanho**: Standard_B1s (1 vCPU, 1 GiB RAM)
  - **Nome de usuário**: `azureuser`
  - **Senha**: ******** (uma senha forte)
  - **Portas de entrada públicas**: RDP (porta 3389)

- Cliquei em "Próximo" até a aba "Revisar + criar"
- Verifiquei as configurações e cliquei em "Criar"

---

### 4. Aguardando a Provisão da Máquina

O Azure iniciou o processo de provisionamento da máquina virtual. Após alguns minutos, a implantação foi concluída com sucesso.

---

### 5. Acesso Remoto à Máquina Virtual

Com a VM criada:

- Acessei a aba "Visão geral" da VM
- Cliquei em "Conectar"
- Escolhi a opção "RDP"
- Baixei o arquivo `.rdp` e abri no meu computador
- Inserção do nome de usuário e senha definidos anteriormente
- Conexão estabelecida com sucesso via Área de Trabalho Remota

---

### 6. Testes Realizados

Dentro da VM:

- Confirmei o acesso à internet
- Acessei o navegador e atualizei o sistema
- Instalei um software leve para teste (como o Notepad++)

---

## Aprendizados e Dicas

- O Azure permite provisionamento rápido e simples de recursos em nuvem com alta disponibilidade.
- Sempre organize os recursos usando grupos de recursos para facilitar a gestão.
- Escolher a **região correta** é importante para reduzir latência e evitar custos desnecessários.
- A **porta 3389 (RDP)** deve estar habilitada para conexões de Área de Trabalho Remota (em sistemas Windows).
- É possível aplicar regras de firewall (NSG) para maior controle de acesso.

---

## Considerações Finais

A criação e configuração de uma máquina virtual no Azure é uma habilidade essencial para profissionais que desejam trabalhar com computação em nuvem. Essa prática serviu como base para compreender conceitos como IaaS (Infrastructure as a Service), provisionamento de recursos e segurança em ambientes de nuvem pública.

---

## Referências

- Documentação Oficial Microsoft Azure:  
  https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal

- Documentação GitHub Markdown:  
  https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github

- Curso da DIO: Introdução à Computação em Nuvem com Azure

