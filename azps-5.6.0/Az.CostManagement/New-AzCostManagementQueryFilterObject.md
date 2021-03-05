---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010653"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Creare un oggetto in memoria per QueryFilter

## SINTASSI

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## DESCRIZIONE
Creare un oggetto in memoria per QueryFilter

## ESEMPI

### Esempio 1: Creare un oggetto filtro della query per l'esportazione della gestione dei costi
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

Questo comando crea un oggetto filtro della query per l'esportazione della gestione dei costi.

## PARAMETERS

### -And
Espressione logica "AND".
Devono contenere almeno 2 elementi.
Per creare, vedere la sezione NOTE relativa alle proprietà AND e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dimensions
Ha un'espressione di confronto per le dimensioni.
Per creare, vedere la sezione NOTE relativa alle proprietà DIMENSIONS e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Not
Espressione logica "NON".
Per creare, vedere la sezione NOTE per le proprietà NOT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Oppure
Espressione logica "OR".
Devono contenere almeno 2 elementi.
Per creare, vedere la sezione NOTE relativa alle proprietà OR e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Ha un'espressione di confronto per un tag.
Per creare, vedere la sezione NOTE relativa alle proprietà TAG e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
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

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


AND <IQueryFilter[]>: espressione logica "AND". Devono contenere almeno 2 elementi.
  - `[And <IQueryFilter[]>]`: Espressione logica "AND". Devono contenere almeno 2 elementi.
  - `[Dimensions <IQueryComparisonExpression>]`: include un'espressione di confronto per una dimensione
    - `Name <String>`: nome della colonna da usare nel confronto.
    - `Value <String[]>`: matrice di valori da utilizzare per il confronto
  - `[Not <IQueryFilter>]`: Espressione logica "NON".
  - `[Or <IQueryFilter[]>]`: Espressione logica "OR". Devono contenere almeno 2 elementi.
  - `[Tag <IQueryComparisonExpression>]`: include un'espressione di confronto per un tag

DIMENSIONS: <IQueryComparisonExpression> ha un'espressione di confronto per le dimensioni.
  - `Name <String>`: nome della colonna da usare nel confronto.
  - `Value <String[]>`: matrice di valori da utilizzare per il confronto

NOT: <IQueryFilter> espressione logica "NON".
  - `[And <IQueryFilter[]>]`: Espressione logica "AND". Devono contenere almeno 2 elementi.
  - `[Dimensions <IQueryComparisonExpression>]`: include un'espressione di confronto per una dimensione
    - `Name <String>`: nome della colonna da usare nel confronto.
    - `Value <String[]>`: matrice di valori da utilizzare per il confronto
  - `[Not <IQueryFilter>]`: Espressione logica "NON".
  - `[Or <IQueryFilter[]>]`: Espressione logica "OR". Devono contenere almeno 2 elementi.
  - `[Tag <IQueryComparisonExpression>]`: include un'espressione di confronto per un tag

OR <IQueryFilter[]>: espressione logica "OR". Devono contenere almeno 2 elementi.
  - `[And <IQueryFilter[]>]`: Espressione logica "AND". Devono contenere almeno 2 elementi.
  - `[Dimensions <IQueryComparisonExpression>]`: include un'espressione di confronto per una dimensione
    - `Name <String>`: nome della colonna da usare nel confronto.
    - `Value <String[]>`: matrice di valori da utilizzare per il confronto
  - `[Not <IQueryFilter>]`: Espressione logica "NON".
  - `[Or <IQueryFilter[]>]`: Espressione logica "OR". Devono contenere almeno 2 elementi.
  - `[Tag <IQueryComparisonExpression>]`: include un'espressione di confronto per un tag

TAG: <IQueryComparisonExpression> include un'espressione di confronto per un tag.
  - `Name <String>`: nome della colonna da usare nel confronto.
  - `Value <String[]>`: matrice di valori da utilizzare per il confronto

## COLLEGAMENTI CORRELATI

