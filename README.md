# 20533EEnvironment
Instruções p/ os alunos montarem do ambiente do curso

- Crie uma vm windows 10 e adicione um disco (50gb ssd tá bom)

- Baixe os Módulos PowerShell do Azure (azure.com/downloads | Command Line Tools | PowerShell | WindowsInstall)

- Adicione o disco através do Gerenciador de disco do Windows 10

- Crie um volume como F: e de preferência GPT (https://pplware.sapo.pt/gadgets/hardware/qual-a-diferena-entre-mbr-e-gpt/)

- Baixe o repositório do curso (https://github.com/MicrosoftLearning/20533-ImplementingMicrosoftAzureInfrastructureSolutions/archive/master.zip) e extraia só o conteúdo da pasta AllFiles para F:

- Execute no Power Shell o comando "Set-ExecutionPolicy –ExecutionPolicy Bypass –Force" para executar scripts "não seguros" (https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6)

- Instale o PowerShell Community Extensions p/ ter algumas extensões usadas nos labs: https://github.com/Pscx/Pscx (caso dê erro que já exista, rode o update-module ao invés do install-module)

- Reinicie a máquina

- Importe os módulos do curso: <br>
	import-module "F:\Modules\Add-20533EEnvironment\Add-20533EEnvironment.psm1"<br>
	import-module "F:\Modules\Remove-20533EEnvironment\Remove-20533EEnvironment.psm1"<br>
	import-module "F:\Modules\Select-20533ELocationARM\Select-20533ELocationARM.psm1"<br>
	import-module "F:\Modules\Select-20533ESubscriptionARM\Select-20533ESubscriptionARM.psm1"<br>
	import-module "F:\Modules\Set-20533EEnvironment\Set-20533EEnvironment.psm1"<br>
	import-module "F:\Modules\Set-20533EVMSize\Set-20533EVMSize.psm1"<br>

- Teste executando a montagem do lab1:<br>
	Add-20533EEnvironment (Lab1 | eastus)

- Instale o Azure cli:<br>
	- Na página de downloads do Azure (https://azure.microsoft.com/en-us/downloads/), em Azure command-line interface, clique em Install
