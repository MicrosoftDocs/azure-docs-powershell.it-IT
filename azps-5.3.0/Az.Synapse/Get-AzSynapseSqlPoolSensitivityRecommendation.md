---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383820"
---
# Get-AzSynapseSqlPoolSensitivityRecommendation

## Sinossi
Ottiene i tipi di informazioni e le etichette di sensitività consigliati delle colonne nel pool SQL.

## SINTASSI

### SqlPoolObjectParameterSet (impostazione predefinita)
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SqlPoolParameterSet
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet Get-AzSynapseSqlPoolSensitivityRecommendation restituisce i tipi di informazioni e le etichette di sensitività consigliati delle colonne nel pool SQL.

## ESEMPI

### Esempio 1: ottenere i tipi di informazioni e le etichette di sensitività consigliati di un pool di SQL sinapsi di Azure.
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### Esempio 2: ottenere i tipi di informazioni e le etichette di sensitività consigliati di un pool di SQL sinapsi di Azure tramite piping.
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## PARAMETRI

### -AsJob
Esegui cmdlet in background

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

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sqlpoolname
Nome del pool di sinapsi SQL.

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlPoolObject
Oggetto di input del pool SQL, in genere passato alla pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Nome dell'area di lavoro sinapsi.

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool

## OUTPUT

### Microsoft. Azure. Commands. sinapsi. Models. DataClassification. SqlPoolSensitivityClassificationModel

## Note

## COLLEGAMENTI CORRELATI
