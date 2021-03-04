---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990442"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
Imposta le proprietà del sistema operativo per una macchina virtuale.

## SINTASSI

### Windows (impostazione predefinita)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzVMOperatingSystem** imposta le proprietà del sistema operativo per una macchina virtuale.
È possibile specificare le credenziali di accesso, il nome del computer e il tipo di sistema operativo.

## ESEMPI

### Esempio 1: Impostare le proprietà del sistema operativo per una nuova macchina virtuale
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

Il primo comando converte una password in una stringa sicura e quindi la archivia nella $SecurePassword variabile.
Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .
Il secondo comando crea le credenziali per l'utente FullerP e la password archiviate in $SecurePassword, quindi archivia le credenziali nella variabile $Credential utente.
Per altre informazioni, digitare `Get-Help New-Object` .
Il terzo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.
Il quarto comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.
I quattro comandi seguenti assegnano valori alle variabili da usare nel comando seguente.
Queste stringhe possono essere specificate direttamente nel comando **Set-AzVMOperatingSystem,** quindi questo approccio viene usato solo per la leggibilità.
Tuttavia, è possibile usare un approccio come questo negli script.
Il comando finale imposta le proprietà del sistema operativo per la macchina virtuale archiviata in $VirtualMachine.
Il comando usa le credenziali archiviate in $Credential.
Per alcuni parametri il comando usa le variabili assegnate nei comandi precedenti.

### Esempio 2: Impostare le proprietà del sistema operativo per una nuova macchina virtuale con le patch a scelta rapida abilitate
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

Il primo comando converte una password in una stringa sicura e quindi la archivia nella $SecurePassword variabile.
Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .
Il secondo comando crea le credenziali per l'utente FullerP e la password archiviate in $SecurePassword, quindi archivia le credenziali nella variabile $Credential utente.
Per altre informazioni, digitare `Get-Help New-Object` .
Il terzo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.
Il quarto comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.
I quattro comandi seguenti assegnano valori alle variabili da usare nel comando seguente.
Queste stringhe possono essere specificate direttamente nel comando **Set-AzVMOperatingSystem,** quindi questo approccio viene usato solo per la leggibilità.
Tuttavia, è possibile usare un approccio come questo negli script.
Il comando finale imposta le proprietà del sistema operativo per la macchina virtuale archiviata in $VirtualMachine.
Il comando usa le credenziali archiviate in $Credential.
Per alcuni parametri il comando usa le variabili assegnate nei comandi precedenti.
Il comando abilita l'accesso a scelta rapida nella macchina virtuale.

### Esempio 3: Impostare le proprietà del sistema operativo per una nuova macchina virtuale Linux
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

Il primo comando converte una password in una stringa sicura e quindi la archivia nella $SecurePassword variabile.
Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .
Il secondo comando crea le credenziali per l'utente FullerP e la password archiviate in $SecurePassword, quindi archivia le credenziali nella variabile $Credential utente.
Per altre informazioni, digitare `Get-Help New-Object` .
Il terzo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.
Il quarto comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.
I due comandi seguenti assegnano valori alle variabili da usare nel comando seguente.
Il comando finale imposta le proprietà del sistema operativo per la macchina virtuale archiviata in $VirtualMachine.
Il comando usa le credenziali archiviate in $Credential.
Per alcuni parametri il comando usa le variabili assegnate nei comandi precedenti.
Il comando imposta il valore della modalità patch nella macchina virtuale su "AutomaticByPlatform".

## PARAMETERS

### -ComputerName
Specifica il nome del computer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Specifica il nome utente e la password della macchina virtuale come **oggetto PSCredential.**
Per ottenere le credenziali, usare il cmdlet Get-Credential.
Per altre informazioni, digitare `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Specifica una stringa da passare alla macchina virtuale. Per altre informazioni, vedere [Dati personalizzati nelle macchine virtuali di Azure.](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)
**Nota: non è consigliabile archiviare informazioni riservate in dati personalizzati.**


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Indica che questo cmdlet disabilita l'autenticazione tramite password.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
Disabilitare provisioning agente VM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
Indica che questo cmdlet abilita l'aggiornamento automatico.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableHotpatching
Consente ai clienti di applicare patch alle macchine virtuali Azure senza dover riavviare il computer. Per enableHotpatching, "provisionVMAgent" deve essere impostato su true e "patchMode" deve essere impostato su "AutomaticByPlatform".

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Indica che il tipo di sistema operativo è Linux.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
Specifica la modalità di distribuzione delle patch in-guest alla macchina virtuale IaaS.<br><br>
I valori possibili sono:<br>
**Manuale:** è possibile controllare l'applicazione delle patch a una macchina virtuale. A questo scopo, applicare manualmente le patch all'interno della macchina virtuale. In questa modalità gli aggiornamenti automatici sono disabilitati; la proprietà WindowsConfiguration.enableAutomaticUpdates deve essere false<br>
**AutomaticByOS:** la macchina virtuale verrà aggiornata automaticamente dal sistema operativo. La proprietà WindowsConfiguration.enableAutomaticUpdates deve essere true. <br >
**AutomaticByPlatform:** la macchina virtuale verrà aggiornata automaticamente dal sistema operativo. Le proprietà provisionVMAgent e WindowsConfiguration.enableAutomaticUpdates devono essere true

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Indica che le impostazioni richiedono l'installazione dell'agente della macchina virtuale nella macchina virtuale.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Specifica il fuso orario della macchina virtuale. ad esempio Ora \" solare \" Pacifico. <br>
I valori possibili possono essere [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) da fusi orari restituiti da [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto della macchina virtuale locale su cui impostare le proprietà del sistema operativo.
Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.
Creare un oggetto macchina virtuale usando il cmdlet New-AzVMConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
Indica che il tipo di sistema operativo è Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
Specifica l'URI di un certificato WinRM.
Questa cartella deve essere archiviata in un Vault delle chiavi.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
Indica che il sistema operativo usa HTTP WinRM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
Indica che questo sistema operativo usa HTTPS WinRM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


