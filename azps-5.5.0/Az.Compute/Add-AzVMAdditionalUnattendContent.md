---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205002"
---
# Add-AzVMAdditionalUnattendContent

## SYNOPSIS
Aggiunge informazioni al file di risposte di Installazione automatica di Windows.

## SINTASSI

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzVMAdditionalUnattendContent** aggiunge informazioni al file di risposte di Installazione automatica di Windows.
Specificare altre informazioni di formato XML codificato in base 64 che questo cmdlet aggiunge al file unattend.xml base.

## ESEMPI

### Esempio 1: Aggiungere contenuto unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Il primo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.
Il secondo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.
Il terzo comando crea un oggetto credenziali usando il cmdlet Get-Credential e quindi archivia il risultato nella $Credential variabile.
Il comando chiede di specificare un nome utente e una password.
Per altre informazioni, digitare `Get-Help Get-Credential` .
Il quarto comando usa il cmdlet **Set-AzVMOperatingSystem** per configurare la macchina virtuale archiviata in $VirtualMachine.
Il quinto comando assegna contenuto alla $AucContent variabile.
Il contenuto include una password.
Il comando finale aggiunge il contenuto archiviato in $AucContent al file unattend.xml finale.

## PARAMETERS

### -Content
Specifica il contenuto in formato XML codificato in base 64.
Questo cmdlet aggiunge il contenuto al file unattend.xml file.
Il contenuto XML deve essere inferiore a 4 KB e deve includere l'elemento radice per l'impostazione o la caratteristica inserita dal cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### -SettingName
Specifica il nome dell'impostazione a cui si applica il contenuto.
I valori accettabili per questo parametro sono:
- FirstLogonCommands
- AutoLogon

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto della macchina virtuale modificato dal cmdlet.
Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzVM.](./Get-AzVM.md)
Creare un oggetto macchina virtuale usando il cmdlet [New-AzVMConfig.](./New-AzVMConfig.md)

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzVMConfig](./New-AzVMConfig.md)
