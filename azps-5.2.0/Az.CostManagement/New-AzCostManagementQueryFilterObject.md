---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336616"
---
# New-AzCostManagementQueryFilterObject

## Sinossi
Creare un oggetto in memoria per QueryFilter

## SINTASSI

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## Descrizione
Creare un oggetto in memoria per QueryFilter

## ESEMPI

### Esempio 1: creare un oggetto Filter di query per l'esportazione di gestione dei costi
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

Questo comando crea un oggetto Filter di query per l'esportazione di gestione dei costi.

## PARAMETRI

### -E
Espressione "e" logica.
Devono avere almeno 2 elementi.
Per costruire, vedere la sezione Note per le proprietà e creare una tabella hash.

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

### -Dimensioni
Ha un'espressione di confronto per le dimensioni.
Per costruire, vedere la sezione Note per le proprietà delle dimensioni e creare una tabella hash.

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
Espressione "NOT" logica.
Per costruire, vedere la sezione Note per le proprietà NOT e creare una tabella hash.

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
Espressione "OR" logica.
Devono avere almeno 2 elementi.
Per creare una tabella hash, vedere la sezione Note o proprietà.

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
Per costruire, vedere la sezione Note per le proprietà dei TAG e creare una tabella hash.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

## OUTPUT

### Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. QueryFilter

## Note

ALIAS

PROPRIETÀ COMPLESSE DI PARAMETRI

Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


E <IQueryFilter [] >: l'espressione "e" logica. Devono avere almeno 2 elementi.
  - `[And <IQueryFilter[]>]`: L'espressione "e" logica. Devono avere almeno 2 elementi.
  - `[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione
    - `Name <String>`: Nome della colonna da usare in confronto.
    - `Operator <OperatorType>`: L'operatore da usare per il confronto.
    - `Value <String[]>`: Matrice di valori da usare per il confronto
  - `[Not <IQueryFilter>]`: Espressione "NOT" logica.
  - `[Or <IQueryFilter[]>]`: L'espressione "OR" logica. Devono avere almeno 2 elementi.
  - `[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag

DIMENSIONI <IQueryComparisonExpression> : contiene un'espressione di confronto per le dimensioni.
  - `Name <String>`: Nome della colonna da usare in confronto.
  - `Operator <OperatorType>`: L'operatore da usare per il confronto.
  - `Value <String[]>`: Matrice di valori da usare per il confronto

NOT <IQueryFilter> : l'espressione "not" logica.
  - `[And <IQueryFilter[]>]`: L'espressione "e" logica. Devono avere almeno 2 elementi.
  - `[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione
    - `Name <String>`: Nome della colonna da usare in confronto.
    - `Operator <OperatorType>`: L'operatore da usare per il confronto.
    - `Value <String[]>`: Matrice di valori da usare per il confronto
  - `[Not <IQueryFilter>]`: Espressione "NOT" logica.
  - `[Or <IQueryFilter[]>]`: L'espressione "OR" logica. Devono avere almeno 2 elementi.
  - `[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag

O <IQueryFilter [] >: l'espressione "OR" logica. Devono avere almeno 2 elementi.
  - `[And <IQueryFilter[]>]`: L'espressione "e" logica. Devono avere almeno 2 elementi.
  - `[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione
    - `Name <String>`: Nome della colonna da usare in confronto.
    - `Operator <OperatorType>`: L'operatore da usare per il confronto.
    - `Value <String[]>`: Matrice di valori da usare per il confronto
  - `[Not <IQueryFilter>]`: Espressione "NOT" logica.
  - `[Or <IQueryFilter[]>]`: L'espressione "OR" logica. Devono avere almeno 2 elementi.
  - `[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag

TAG <IQueryComparisonExpression> : contiene un'espressione di confronto per un tag.
  - `Name <String>`: Nome della colonna da usare in confronto.
  - `Operator <OperatorType>`: L'operatore da usare per il confronto.
  - `Value <String[]>`: Matrice di valori da usare per il confronto

## COLLEGAMENTI CORRELATI

