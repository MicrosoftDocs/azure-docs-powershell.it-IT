---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: f3ab3c381e36c766e6d4bdb24476f6bd1cd69df3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989896"
---
# New-AzOperationalInsightsStorageInsight

## SYNOPSIS
Crea un approfondimento di archiviazione all'interno di un'area di lavoro.

## SINTASSI

### ByWorkspaceName (Impostazione predefinita)
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByWorkspaceObject
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzOperationalInsightsStorageInsight** crea una nuova istanza di Storage Insight in un'area di lavoro esistente.

## ESEMPI

### Esempio 1: Creare un approfondimento di archiviazione in base al nome
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

Il primo comando usa il cmdlet Get-AzStorageAccount per ottenere l'account di archiviazione denominato ContosoStorage e quindi lo archivia nella $Storage variabile.
Il secondo comando passa l'account di archiviazione di $Storage al cmdlet Get-AzStorageAccountKey usando l'operatore della pipeline per ottenere la chiave dell'account di archiviazione specificata e quindi la archivia nella variabile $StorageKey. Questo esempio recupera la prima chiave. Per recuperare l'altro, usare Valore[1] invece di Valore[0].
Il comando finale crea un'analisi dello spazio di archiviazione denominata MyStorageInsight nell'area di lavoro denominata MyWorkspace.
Queste informazioni di archiviazione utilizzano i dati della tabella WADWindowsEventLogsTable nella risorsa dell'account di archiviazione specificata.

### Esempio 2: Creare un approfondimento di archiviazione usando un oggetto area di lavoro
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

Il primo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata MyWorkspace e quindi la archivia nella $Workspace variabile.
Il secondo comando usa il cmdlet Get-AzStorageAccount per ottenere l'account di archiviazione specificato e quindi lo archivia nella $Storage variabile.
Il terzo comando passa l'account di archiviazione di $Storage al cmdlet Get-AzStorageAccountKey usando l'operatore della pipeline per ottenere la chiave specificata e quindi lo archivia nella variabile $StorageKey variabile. Questo esempio recupera la prima chiave. Per recuperare l'altro, usare Valore[1] invece di Valore[0].
Il comando finale crea un'analisi dello spazio di archiviazione denominata MyStorageInsight nell'area di lavoro definita in $Workspace.
Informazioni dettagliate di archiviazione utilizza i dati della tabella WADWindowsEventLogsTable nella risorsa dell'account di archiviazione specificata.

## PARAMETERS

### -Containers
Specifica l'elenco di contenitori che contengono i dati.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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
Specifica il nome dell'approfondimento di archiviazione.

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

### -ResourceGroupName
Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
Specifica la chiave di accesso per l'account di archiviazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountResourceId
Specifica la risorsa Azure di un account di archiviazione.
Può essere recuperata eseguendo il cmdlet Get-AzStorageAccount e accedendo al *parametro ID* del risultato.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tabelle
Specifica l'elenco di tabelle che forniscono i dati.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Area di lavoro
Specifica l'area di lavoro per il nuovo approfondimento archiviazione.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Specifica il nome di un'area di lavoro esistente.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

### System.String

### System.String[]

## OUTPUT

### Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight

## NOTE

## COLLEGAMENTI CORRELATI

[Cmdlet di Azure Operational Insights](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


