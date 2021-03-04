---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: facd5a3637dcb1a8a392171468dd890279ba0f74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957502"
---
# Set-AzVMDscExtension

## SYNOPSIS
Configura l'estensione DSC in una macchina virtuale.

## SINTASSI

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzVMDscExtension** configura l Windows PowerShell DSC (Desired State Configuration) in una macchina virtuale in un gruppo di risorse.

## ESEMPI

### Esempio 1: Impostare un'estensione DSC
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

Questo comando imposta l'estensione DSC nella macchina virtuale denominata VM07 in modo da scaricare Sample.ps1.zip dall'account di archiviazione denominato Stg e dal contenitore predefinito.
Il comando richiama la configurazione denominata ConfigName.
Il Sample.ps1.zip file è stato caricato in precedenza tramite **Publish-AzVMDscConfiguration.**

### Esempio 2: Impostare un'estensione DSC con dati di configurazione
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

Questo comando imposta l'estensione nella macchina virtuale denominata VM13 in modo che scarichi Sample.ps1.zip dall'account di archiviazione denominato Stg e dal contenitore denominato WindowsPowerShellDSC.
Comando che si chiama ConfigName e specifica i dati e gli argomenti di configurazione.
Il Sample.ps1.zip file è stato caricato in precedenza tramite **Publish-AzVMDscConfiguration.**

### Esempio 3: Impostare un'estensione DSC con dati di configurazione con aggiornamento automatico
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

Questo comando imposta l'estensione nella macchina virtuale denominata VM22 in modo che scarichi Sample.ps1.zip dall'account di archiviazione denominato Stg e dal contenitore denominato WindowsPowerShellDSC.
Il comando richiama la configurazione denominata ConfigName e specifica i dati e gli argomenti di configurazione.
Questo comando abilita anche l'aggiornamento automatico del gestore delle estensioni alla versione più recente.
Il Sample.ps1.zip è stato caricato in precedenza tramite **Publish-AzVMDscConfiguration.**

## PARAMETERS

### -ArchiveBlobName
Specifica il nome del file di configurazione caricato in precedenza dal cmdlet Publish-AzVMDscConfiguration configurazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveContainerName
Nome della specie del contenitore di archiviazione di Azure in cui si trova l'archivio di configurazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveResourceGroupName
Specifica il nome del gruppo di risorse che contiene l'account di archiviazione che contiene l'archivio di configurazione.
Questo parametro è facoltativo se l'account di archiviazione e la macchina virtuale si trovano entrambi nello stesso gruppo di risorse.

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

### -ArchiveStorageAccountName
Specifica il nome dell'account di archiviazione di Azure usato per scaricare ArchiveBlobName.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveStorageEndpointSuffix
Specifica il suffisso dell'endpoint di archiviazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoUpdate
Specifica la versione del gestore delle estensioni specificata dal *parametro Version.*
Per impostazione predefinita, il gestore dell'estensione non è autoupdated.
Usare il *parametro AutoUpdate* per abilitare l'aggiornamento automatico del gestore delle estensioni alla versione più recente come e quando è disponibile.

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

### -Configuration Argument
Specifica una tabella hash che contiene gli argomenti della funzione di configurazione.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationData
Specifica il percorso di un file psd1 che specifica i dati per la configurazione.

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

### -ConfigurationName
Specifica il nome della configurazione che viene richiamata dall'estensione DSC.

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

### -DataCollection
Specifica il tipo di raccolta dati.
I valori accettabili per questo parametro sono: Enable e Disable.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
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

### -Location
Specifica il percorso dell'estensione di risorsa.

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

### -Name
Specifica il nome della risorsa Gestione risorse di Azure che rappresenta l'estensione.
Il valore predefinito è Microsoft.Powershell.DSC.

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
Specifica il nome del gruppo di risorse della macchina virtuale.

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

### -Version
Specifica la versione dell'estensione DSC a cui Set-AzVMDscExtension applica le impostazioni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifica il nome della macchina virtuale in cui è installato il gestore dell'estensione DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WmfVersion
Specifica la versione WMF.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
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

### System.Collections.Hashtable

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Publish-AzVMDscConfiguration](./Publish-AzVMDscConfiguration.md)


