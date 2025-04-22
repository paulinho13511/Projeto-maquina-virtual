# Projeto-maquina-virtual
Visão geral do repositório

Links para as seções

Objetivo do projeto

resumos/conceitos-basicos.md

Microsoft Azure é uma plataforma de computação em nuvem da Microsoft.

Recursos: componentes como VMs, redes, discos.

Grupo de recursos: container para recursos relacionados.

Portal Azure: interface gráfica para gestão dos serviços.

resumos/tipos-de-maquinas-virtuais.md

Tipos comuns:

B (baixo custo, uso intermitente)

D (uso geral)

E (otimizado para memória)

F (otimizado para CPU)

Tamanhos determinam CPU, RAM e armazenamento.

resumos/redes-e-seguranca.md

VNet: rede virtual isolada.

Subnet: subdivisão da VNet.

NSG (Network Security Group): regras de firewall.

IP Público: acesso externo.

IP Privado: comunicação interna.

Conexão por RDP (Windows) ou SSH (Linux).

resumos/armazenamento.md

Tipos de disco:

HDD: custo mais baixo

SSD: maior desempenho

Disco do SO e discos de dados adicionais.

Opções de armazenamento premium para aplicações críticas.

passo-a-passo/criando-maquina-virtual.md

Acesse o portal https://portal.azure.com

Crie um grupo de recursos.

Clique em "Criar um recurso" > "Computação" > "Máquina Virtual"

Preencha:

Nome da VM

Região

Imagem (ex: Ubuntu, Windows Server)

Tamanho da VM

Autenticação (usuário/senha ou chave SSH)

Configure rede e regras de firewall (permitir RDP/SSH).

Revise e crie.

Acesse a VM pelo IP público.

dicas/boas-praticas.md

Padronize nomes de recursos (ex: vm-web-01, rg-projeto-x).

Use tags para organização.

Desligue VMs quando não estiver usando para economizar.

Automatize tarefas com scripts (Azure CLI, PowerShell).

dicas/comandos-uteis.md

![image](https://github.com/user-attachments/assets/ce489bec-2d78-4fd6-8b75-7aa2a0093440)


az login
az group create --name MeuGrupo --location eastus
az vm create \
  --resource-group MeuGrupo \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys


Connect-AzAccount
New-AzResourceGroup -Name MeuGrupo -Location "East US"
New-AzVM -ResourceGroupName MeuGrupo -Name MinhaVM -Image UbuntuLTS
