# Criacao-de-maquina-virtual---Azure

Digite máquinas virtuais na pesquisa.

Em Serviços, selecione Máquinas virtuais.

Na página Máquinas virtuais, clique em Criar e selecione Máquina virtual do Azure. A página Criar uma máquina virtual é aberta.

Em Detalhes da instância, insira myVM no Nome da máquina virtual e escolha Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2 na Imagem. Deixe os outros padrões.

Em Conta de administrador, forneça um nome de usuário, como azureuser e uma senha. A senha deve ter no mínimo 12 caracteres e atender a requisitos de complexidade definidos.

Em Regras de porta de entrada, escolha Permitir portas selecionadas e, em seguida, selecione RDP (3389) e HTTP (80) na lista suspensa.

Deixe os padrões restantes e, em seguida, selecione o botão Examinar + criar na parte inferior da página.

Após a execução da validação, selecione o botão Criar na parte inferior da página

Após a conclusão da implantação, selecione Ir para o recurso.

Conectar-se à máquina virtual
Inicie uma conexão da área de trabalho remota para a máquina virtual. Estas instruções ensinam a se conectar aàsua VM de um computador com Windows. Em um Mac, você precisa de um cliente RDP, como este Cliente de Área de Trabalho Remota da Mac App Store.

Selecione Conectar>RDP na página de visão geral de sua máquina virtual.

Captura de tela da página de visão geral da máquina virtual mostrando o local do botão Conectar.

Na guia Conectar-se ao RDP, mantenha as opções padrão para se conectar por endereço IP pela porta 3389 e clique em Baixar arquivo RDP.

Abra o arquivo RDP baixado e clique em Conectar quando solicitado.

Na janela Segurança do Windows, selecione Mais opções e Usar uma conta diferente. Digite o nome de usuário como localhost\nome de usuário, insira a senha que você criou para a máquina virtual e clique em OK.

Você pode receber um aviso do certificado durante o processo de logon. Clique em Sim ou em Continuar para criar a conexão.

Instalar servidor Web
Para ver a VM em ação, instale o servidor Web do IIS. Abra um prompt do PowerShell na VM e execute o seguinte comando:

PowerShell

Copiar
Install-WindowsFeature -name Web-Server -IncludeManagementTools
Quando terminar, feche a conexão RDP com a VM.
