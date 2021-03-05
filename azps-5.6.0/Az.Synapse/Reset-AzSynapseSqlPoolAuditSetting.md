---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 8b47466c2f40ff769c1755ea1d59873a120e5d5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010142"
---
# Reset-AzSynapseSqlPoolAuditSetting

## SYNOPSIS
Rimuove le impostazioni di controllo di un pool di SQL Azure Synapse Analytics.

## SINTASSI

### RemoveByNameParameterSet (impostazione predefinita)
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByParentObjectParameterSet
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByInputObjectParameterSet
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Reset-AzSynapseSqlPoolAuditSetting** rimuove le impostazioni di controllo di un pool di SQL Azure Synapse Analytics.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

Questo comando rimuove le impostazioni di controllo di un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.

### Esempio 2
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

Questo comando rimuove le impostazioni di controllo di un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace tramite pipeline.

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
SQL di input del pool, in genere passato attraverso la pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome del pool SQL Synapse.

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Questo cmdlet non restituisce un oggetto per impostazione predefinita.
Se questa opzione è specificata, restituisce true se ha esito positivo.

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
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identificatore di risorsa del pool SQL synapse.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
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
Parameter Sets: RemoveByNameParameterSet
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
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool

## OUTPUT

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI
