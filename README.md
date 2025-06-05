# Criacao-de-maquina-virtual---Azure
https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal 

🔍 Visão geral simplificada: o que são máquinas virtuais (VMs)?
Máquinas virtuais (VMs) são computadores criados dentro de um servidor físico, como se fossem “computadores virtuais” rodando dentro de outro. Você pode acessá-las remotamente e usá-las como usaria qualquer outro computador, com sistema operacional, internet, programas etc. No caso do Azure, essas máquinas estão "na nuvem", ou seja, você não precisa ter um computador físico para usá-las — o Azure fornece os recursos de forma online.

🎯 Para que servem as máquinas virtuais?
Elas são usadas para várias finalidades, como:

Hospedar sites e aplicativos

Rodar sistemas operacionais de teste (sem afetar o seu computador)

Treinar softwares de inteligência artificial

Executar bancos de dados

Simular ambientes de trabalho

Criar ambientes para estudo e aprendizado de TI

Economizar com infraestrutura, já que você só paga pelo que usar.

🧱 Explicação de cada etapa e escolha feita no tutorial
Vamos entender, passo a passo, por que cada escolha foi feita ao criar a máquina virtual:

1. Nome da máquina virtual: myVM
Por que é importante?: Serve para identificar sua VM dentro do Azure. Você pode dar qualquer nome.

Sugestão: use nomes que indiquem o propósito, como site-loja, teste-dados, etc.

2. Imagem: Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2
O que é?: É o sistema operacional que a VM vai usar.

Por que escolher essa imagem?:

É uma versão otimizada para servidores na nuvem.

Boa para aplicações de rede, bancos de dados, sites e serviços web.

Você também poderia escolher Linux, Ubuntu, Debian, dependendo da sua necessidade.

3. Zonas de disponibilidade (opcional)
O que é?: São “zonas” diferentes dentro de um mesmo datacenter.

Serve para quê?: Garantir que sua VM fique disponível mesmo se uma zona falhar.

Para quem vale a pena?: Projetos críticos que não podem parar, como e-commerce ou aplicativos de banco.

4. Conta de administrador (nome de usuário e senha)
Por que isso?: Você precisa de acesso para configurar e operar a VM.

Regras da senha:

Mínimo 12 caracteres

Letras, números e símbolos

Isso protege a segurança da VM

5. Regras de porta de entrada: RDP (3389) e HTTP (80)
RDP (3389):

Permite acessar a VM remotamente como se fosse seu PC

Útil para ver e controlar o sistema com interface gráfica (como o Windows)

HTTP (80):

Libera o tráfego da web

Necessário se você for hospedar um site ou servidor web, como o IIS

6. Examinar + criar
Por que isso?: O Azure revisa se todos os dados estão corretos.

Só depois da validação é possível criar a VM.

7. Conectar-se via RDP
Por que isso?: Para usar o sistema operacional da VM remotamente, como se você estivesse na frente de um computador com Windows.

O acesso é feito por endereço IP e precisa do nome de usuário e senha criados.

8. Instalar o servidor Web (IIS)
Comando: Install-WindowsFeature -name Web-Server -IncludeManagementTools

O que isso faz?

Instala o Internet Information Services (IIS), que é um servidor web da Microsoft.

Ele permite que a VM hospede um site ou aplicação web.

Depois disso, ao digitar o IP no navegador, você vê a página de boas-vindas do IIS.

9. Limpar os recursos (excluir)
Por que isso?:

Quando a VM não for mais necessária, você pode apagar tudo para evitar cobranças.

O Azure cobra por tempo de uso, então é importante não deixar VMs ligadas sem uso.
