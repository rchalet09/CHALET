# CHALET
REPOSITORIO DESAFIO DIO XP INC IA E CLOUD

# DIO - XP Inc. - Cloud com Inteligência Artificial

### 📝 DESAFIO DIO "beneficios-da-nuvem-laboratorio"
    Criando máquinas Virtuais na Azure
    
- INTERFACE WEB DO AZURE


Digite máquinas virtuais na pesquisa da interface WEB.

Em Serviços, selecione Máquinas virtuais.

Na página Máquinas virtuais, clique em Criar e selecione Máquina virtual do Azure. "A página Criar uma máquina virtual é aberta".

Em Detalhes da instância, insira myVM no Nome da máquina virtual digite o nome escolhido para a instância, e após escolha o sistema operacional desejado (Ubuntu,Windows Server 2022 Datacenter), e o tipo de máquina desejado (X32, X64, um núcleo, etc).

2 Verifique a Região e Zona de disponibilidade onde a instância será criada.

3 Em Conta de administrador, forneça um nome de usuário, como azureuser e uma senha. A senha deve ter no mínimo 12 caracteres

4 Em Regras de porta de entrada, escolha Permitir portas selecionadas e, em seguida, selecione RDP (3389) e HTTP (80) na lista suspensa.

5 Deixe os padrões restantes e, em seguida, selecione o botão Examinar + criar na parte inferior da página.


- ATRAVÉS DO CLI (COMMAND LINE INTERFACE).

1  Para abrir o Cloud Shell, basta selecionar Experimentar no canto superior direito de um bloco de código. Você também pode iniciar o Cloud Shell em uma guia separada do navegador indo até <https://shell.azure.com/bash>. Selecione Copiar para copiar os blocos de código, cole o código no Cloud Shell e depois pressione Enter para executá-lo.

2  Crie um grupo de recursos com o comando az group create. Um grupo de recursos do Azure é um contêiner lógico no qual os recursos do Azure são implantados e gerenciados. O seguinte exemplo cria um grupo de recursos chamado myResourceGroup na localização Oeste dos EUA 3. Substitua o valor das variáveis conforme necessário.

(Cada serviço ou objeto no Azure é associado a um grupo de recursos)

Código a ser inserido no prompt do CLI do AZURE:

resourcegroup="myResourceGroupCLI"
location="westus3"
az group create --name $resourcegroup --location $location

**Criar máquina virtual**

Crie uma VM com az vm create. O exemplo a seguir cria uma VM chamada myVM. Este exemplo usa azureuser para um nome de usuário administrativo. Substitua os valores das variáveis conforme necessário.

Você será solicitado a fornecer uma senha que atenda aos requisitos de senha para as VMs do Azure.

Usando o exemplo abaixo, você será solicitado a inserir uma senha na linha de comando. Você também pode adicionar o parâmetro --admin-password com um valor para sua senha. O nome de usuário e a senha serão usados quando você se conectar à VM.

Código a ser inserido no prompt do CLI do AZURE:

vmname="myVM"
username="azureuser"
az vm create --resource-group $resourcegroup --name $vmname --image Win2022AzureEditionCore --public-ip-sku Standard --admin-username $username

Saída 

{
  "fqdns": "",
  "id": "/subscriptions/<guid>/resourceGroups/myResourceGroup/providers/Microsoft.Compute/virtualMachines/myVM",
  "location": "westus3",
  "macAddress": "00-0D-3A-23-9A-49",
  "powerState": "VM running",
  "privateIpAddress": "10.0.0.4",
  "publicIpAddress": "52.174.34.95",
  "resourceGroup": "myResourceGroupCLI"
  "zones": ""
}

Após a criação da Máquina Virtual, diversas alterações podem ser feitas nela como configurações, liberação de portas e alterações de regras, entretanto a alteração do tipo de máquina e do IP Público exigem sua exclusão e recriação. 
  
- ATRAVÉS DO POWERSHELL.

VMs com o Azure PowerShell

Iniciar o Azure Cloud Shell

O Azure Cloud Shell é um shell gratuito e interativo que poderá ser usado para executar as etapas deste artigo. Ele tem ferramentas do Azure instaladas e configuradas para usar com sua conta.

1 Para abrir o Cloud Shell, basta selecionar Experimentar no canto superior direito de um bloco de código. Você também pode iniciar o Cloud Shell em uma guia separada do navegador indo até <https://shell.azure.com/powershell>. Selecione Copiar para copiar os blocos de código, cole o código no Cloud Shell e depois pressione Enter para executá-lo.

2 Criar grupo de recursos
Crie um grupo de recursos com o comando New-AzResourceGroup.

Um grupo de recursos do Azure é um contêiner lógico no qual os recursos do Azure são implantados e gerenciados. Você deve criar um grupo de recursos antes de criar uma máquina virtual. No exemplo a seguir, um grupo de recursos chamado myResourceGroupVM é criado na região EastUS:


Código a ser inserido no prompt do PowerShell do AZURE:


New-AzResourceGroup -ResourceGroupName "myResourceGroupVM" -Location "EastUS"

Criar uma máquina virtual
Há várias opções disponíveis ao criar uma VM, como a imagem do sistema operacional, a configuração de rede e as credenciais administrativas. Este exemplo cria uma VM, denominada myVM, que executa a versão padrão do Windows Server 2016 Datacenter.

Defina o nome de usuário e a senha necessários para a conta de administrador na VM com Get-Credential:

Código a ser inserido no prompt do PowerShell do AZURE:

$cred = Get-Credential

Crie a VM com New-AzVM.

Código a ser inserido no prompt do PowerShell do AZURE:

New-AzVm `
    -ResourceGroupName "myResourceGroupVM" `
    -Name "myVM" `
    -Location "EastUS" `
    -VirtualNetworkName "myVnet" `
    -SubnetName "mySubnet" `
    -SecurityGroupName "myNetworkSecurityGroup" `
    -PublicIpAddressName "myPublicIpAddress" `
    -Credential $cred





# Hi there, I'm CHALET! 👋

Welcome to my GitHub profile! I'm a passionate developer and tech enthusiast who loves exploring new technologies, building innovative projects, and contributing to the open-source community.




---

## 🚀 About Me
- 🛠️ **Skills:** [List your skills—e.g., Python, JavaScript, React, Node.js, etc.]
- 🔭 **Currently Working On:** [Briefly describe your current project or area of focus]
- 🌱 **Learning:** [Mention any new technology or skill you're currently learning]
- 💬 **Ask Me About:** [Topics you're knowledgeable about and open to discussing]
- 📧 **Contact Me:** [Add your email or preferred contact method]
- 🌐 **Portfolio:** [Link to your personal website or portfolio]

---

## 📊 GitHub Stats

![rchalet09's GitHub Stats](https://github-readme-stats.vercel.app/api?username=rchalet09&show_icons=true&theme=radical)

---

## 📈 Top Languages

![rchalet09's Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=rchalet09&layout=compact&theme=radical)

---

## 🌟 Featured Projects

### [Project Name](#)
**Description:** [Brief description of what this project does and its importance.]

### [Another Project Name](#)
**Description:** [Provide details about another cool project.]

Feel free to explore my repositories and connect with me for collaborations!

---

### 📝 Fun Facts
- 🎮 I enjoy gaming in my free time.
- ✈️ I love traveling and exploring new places.
- 📚 Avid reader and constant learner.


---

Thank you for visiting my profile! 😊
