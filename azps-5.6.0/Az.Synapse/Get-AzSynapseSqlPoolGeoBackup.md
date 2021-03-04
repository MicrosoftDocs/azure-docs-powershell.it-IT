---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957869"
---
# Get-AzSynapseSqlPoolGeoBackup

## SYNOPSIS
Ottiene un backup geo-ridondante di un pool Sql.

## SINTASSI

### GetByNameParameterSet (impostazione predefinita)
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SqlPoolGeoBackupResourceId
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzSynapseSqlPoolGeoBackup** ottiene un backup geo-ridondante specificato di un pool di SQL o di tutti i backup geo-ridondanti disponibili in un'area di lavoro specificata.
Un backup geo-ridondante è una risorsa ripristinabile che usa file di dati da una posizione geografica separata.
È possibile usare Geo-Restore per ripristinare un backup geo-ridondante in caso di un'interruzione regionale e ripristinare il pool sql in una nuova area geografica.

## ESEMPI

### Esempio 1: Ottenere un backup geo-ridondante specificato
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
Il cmdlet recupera il backup geografico per un pool SQL.

### Esempio 2: Ottenere tutti i backup geo-ridondanti in un'area di lavoro
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
Questo comando recupera tutti i backup geo-ridondanti disponibili in un'area di lavoro specificata.

### Esempio 3: Ottenere tutti i backup geo-ridondanti in un'area di lavoro usando i filtri
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
Questo comando recupera tutti i backup geo-ridondanti disponibili in un'area di lavoro specificata che inizia con "Contoso".

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
Pool Synapse Sql.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Immettere un ID risorsa di backup geografico del pool Sql.

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -WorkspaceName
Nome dell'area di lavoro Synapse.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup

## OUTPUT

### Microsoft.Azure.Commands.Synapse.Models.PSBackupModel

## NOTE

## COLLEGAMENTI CORRELATI
