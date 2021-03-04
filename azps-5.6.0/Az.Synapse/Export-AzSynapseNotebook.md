---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: 110d72f0a73a6a710e014a08c64cadf3b8be7d0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981869"
---
# Export-AzSynapseNotebook

## SYNOPSIS
Esporta notbook.

## SINTASSI

### ExportByName (impostazione predefinita)
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExportByObject
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExportByInputObject
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Export-AzSynapseNotebook** esporta un blocco appunti Azure Synapse in un file del blocco appunti (con estensione ipynb). Il nome del blocco appunti diventa il nome del file esportato. Se si specifica il nome di un blocco appunti, il cmdlet esporta il blocco appunti. Se non si specifica un nome, il cmdlet esporta tutti i blocchi appunti nell'area di lavoro.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

Esporta tutti i blocchi appunti nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti".

### Esempio 2
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti".

### Esempio 3
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti" tramite pipeline.

### Esempio 4
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti" tramite pipeline.

## PARAMETERS

### -AsJob
Eseguire il cmdlet in background

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

### -InputObject
Oggetto blocco appunti.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome del blocco appunti.

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFolder
La cartella in cui deve essere inserito il blocco appunti.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nome dell'area di lavoro Synapse.

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceObject
Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource

## OUTPUT

### System.IO.FileInfo

## NOTE

## COLLEGAMENTI CORRELATI
