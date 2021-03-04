---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 0fa0069686a34fbd1ee60d31df96386a5d7959d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981853"
---
# Get-AzSynapseDataFlow

## SYNOPSIS
Ottiene informazioni sui flussi di dati nell'area di lavoro.

## SINTASSI

### GetByName (impostazione predefinita)
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByObject
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzSynapseDataFlow** ottiene informazioni sui flussi di dati nell'area di lavoro.
Se si specifica il nome di un flusso di dati, questo cmdlet riceve informazioni sul flusso di dati.
Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i flussi di dati nell'area di lavoro.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

Questo comando recupera informazioni su tutti i flussi di dati nell'area di lavoro denominata ContosoWorkspace.

### Esempio 2
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

Questo comando recupera informazioni sul flusso di dati denominato ContosoDataFlow nell'area di lavoro ContosoWorkspace.

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

### -Name
Nome del flusso di dati.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nome dell'area di lavoro Synapse.

```yaml
Type: System.String
Parameter Sets: GetByName
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
Parameter Sets: GetByObject
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

## OUTPUT

### Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource

## NOTE

## COLLEGAMENTI CORRELATI
