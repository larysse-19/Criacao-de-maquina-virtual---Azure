# Criacao-de-maquina-virtual---Azure
https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal 

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

Limpar os recursos
Excluir recursos
Quando o grupo de recursos, a máquina virtual e todos os recursos relacionados não forem mais necessários, exclua-os.

Na página Visão geral da VM, selecione o link Grupo de recursos.
Selecione Excluir grupo de recursos na parte superior da página do grupo de recursos.
Uma página abrirá um aviso de que você está prestes a excluir recursos. Digite o nome do grupo de recursos e selecione Excluir para concluir a exclusão dos recursos e do grupo de recursos.
Desligamento automático
Se a VM ainda for necessária, o Azure fornecerá um recurso de desligamento automático para máquinas virtuais a fim de ajudar a gerenciar custos e garantir que você não seja cobrado por recursos não utilizados.

Na seção Operações da VM, selecione a opção Desligamento automático.
Uma página será aberta na qual você poderá configurar o tempo para o desligamento automático. Selecione a opção Ativado para habilitar e, em seguida, defina uma hora que seja adequada para você.
Depois de definir a hora, selecione Salvar na parte superior para habilitar a configuração de Desligamento automático.
 Observação

Lembre-se de configurar o fuso horário corretamente para corresponder aos seus requisitos, pois o UTC (Tempo Universal Coordenado) é a configuração padrão na lista suspensa de fuso horário.

Para obter mais informações, confira Desligamento automático.
