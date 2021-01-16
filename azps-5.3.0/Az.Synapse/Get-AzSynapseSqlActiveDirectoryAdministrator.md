---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383960"
---
# Get-AzSynapseSqlActiveDirectoryAdministrator

## Sinossi
Ottiene informazioni su un amministratore di Azure AD per l'area di lavoro di analisi sinapsi.

## SINTASSI

### GetByNameParameterSet (impostazione predefinita)
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByInputObjectParameterSet
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** ottiene le informazioni su un amministratore di Azure Active Directory (Azure ad) per un'area di lavoro di analisi di Azure sinapsi nell'abbonamento corrente.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

Questo comando consente di ottenere informazioni su un amministratore di Azure AD per un'area di lavoro denominata ContosoWorkspace.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
oggetto di input dell'area di lavoro, in genere passato alla pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identificatore delle risorse dell'area di lavoro sinapsi.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nome dell'area di lavoro sinapsi.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace

## OUTPUT

### Microsoft. Azure. Commands. sinapsi. Models. PSWorkspaceAadAdminInfo

## Note

## COLLEGAMENTI CORRELATI
