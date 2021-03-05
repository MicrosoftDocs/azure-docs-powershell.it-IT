---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: ce554f3591f022bdbc375c12a50ea9dae85b8baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998813"
---
# New-AzCosmosDBGremlinIndexingPolicy

## SYNOPSIS
Crea un nuovo oggettoDb IndexingPolicy.

## SINTASSI

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzCosmosDBGremlinIndexingPolicy** crea un nuovo oggetto di tipo PSIndexingPolicy.

## ESEMPI

### Esempio 1
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

{{ Aggiungi la descrizione di esempio qui }}

## PARAMETERS

### -Automatico
Bool per indicare se il criterio di indicizzazione è automatico

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CompositePath
Matrice di matrice di oggetti di tipo Microsoft.Azure.Commands.FosDB.PSCompositePath

```yaml
Type: PSCompositePath[][]
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedPath
Matrice di stringhe contenenti excludedPath(specifica un percorso all'interno di un documento JSON da escludere nel servizio DB di Azure Azure.  .

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludedPath
Matrice di stringhe contenenti includedPath (specifica un percorso all'interno di un documento JSON da includere negli elementi del servizio DB di Azure Vengonos).

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IndexingMode
Indica la modalità di indicizzazione.
I valori possibili includono: 'Coerente', 'Lazi', 'Nessuno'

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SpatialSpec
Matrice di oggetti di tipo Microsoft.Azure.Commands.BulsDB.PSSpatialSpec

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.EnterpriseDb.Models.PSIndexingPolicy

## NOTE

## COLLEGAMENTI CORRELATI
