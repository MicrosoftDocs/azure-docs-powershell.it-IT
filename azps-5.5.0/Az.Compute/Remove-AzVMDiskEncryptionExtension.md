---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177550"
---
# Remove-AzVMDiskEncryptionExtension

## SYNOPSIS
Rimuove l'estensione di crittografia disco da una macchina virtuale.

## SINTASSI

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzVMDiskEncryptionExtension** rimuove l'estensione di crittografia del disco e la configurazione dell'estensione associata da una macchina virtuale. Se non viene specificato alcun nome di estensione, questo cmdlet rimuove l'estensione con nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o AzureDiskEncryptionForLinux per le macchine virtuali basate su Linux. 

Questo cmdlet non riesce se la crittografia nella macchina virtuale non è stata prima disabilitata.  Per disabilitare la crittografia in una macchina virtuale, usare [Disable-AzVMDiskEncryption.](./Disable-AzVMDiskEncryption.md) 

## ESEMPI

### Esempio 1: Rimuovere l'estensione di crittografia disco da una macchina virtuale.
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

Questo comando rimuove l'estensione con il nome predefinito AzureDiskEncryption per una macchina virtuale che esegue il sistema operativo Windows o AzureDiskEncryptionForLinux per macchina virtuale basata su Linux denominata MyTestVM.

### Esempio 2: Rimuovere una specifica estensione di crittografia disco da una macchina virtuale.
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

Questo comando rimuove l'estensione di crittografia denominata MyDiskEncryptionExtension dalla macchina virtuale myTestVM.

## PARAMETERS

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

### -Force
Forza l'esecuzione del comando senza chiedere conferma all'utente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifica il nome della risorsa Gestione risorse di Azure che rappresenta l'estensione.
Il cmdlet Set-AzVMDiskEncryptionExtension imposta questo nome su AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows e le macchine virtuali AzureDiskEncryptionForLinux per Linux.
Specificare questo parametro solo se è stato modificato il nome predefinito nel cmdlet **Set-AzVMDiskEncryptionExtension** o se è stato usato un nome di risorsa diverso in un modello di Gestione risorse.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione. Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse per la macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifica il nome della macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVMDiskEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Set-AzVMDiskEncryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


