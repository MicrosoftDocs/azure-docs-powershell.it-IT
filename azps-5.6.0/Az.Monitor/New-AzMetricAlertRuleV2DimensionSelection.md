---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 244e71148557ef46ea3305f7dc2826eb06e3b50d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962894"
---
# <span data-ttu-id="d958c-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d958c-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="d958c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d958c-102">SYNOPSIS</span></span>
<span data-ttu-id="d958c-103">Crea un oggetto di selezione della dimensione locale che può essere usato per creare criteri di avviso metrica.</span><span class="sxs-lookup"><span data-stu-id="d958c-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="d958c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d958c-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d958c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d958c-105">DESCRIPTION</span></span>
<span data-ttu-id="d958c-106">Il cmdlet **New-AzMetricAlertRuleV2DimensionSelection** crea un oggetto di selezione della dimensione locale per facilitare la costruzione dei criteri di avviso della metrica usando il cmdlet [New-AzMetricAlertRuleV2Criteria.](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="d958c-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="d958c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d958c-107">EXAMPLES</span></span>

### <span data-ttu-id="d958c-108">Esempio 1: Creare un oggetto di selezione della dimensione</span><span class="sxs-lookup"><span data-stu-id="d958c-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="d958c-109">Questo comando crea un oggetto di selezione della dimensione che specifica che i valori {1,3,4} devono essere selezionati per la dimensione "LUN"</span><span class="sxs-lookup"><span data-stu-id="d958c-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="d958c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d958c-110">PARAMETERS</span></span>

### <span data-ttu-id="d958c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d958c-111">-DefaultProfile</span></span>
<span data-ttu-id="d958c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d958c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d958c-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="d958c-113">-DimensionName</span></span>
<span data-ttu-id="d958c-114">Nome della dimensione</span><span class="sxs-lookup"><span data-stu-id="d958c-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d958c-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="d958c-115">-ValuesToExclude</span></span>
<span data-ttu-id="d958c-116">Valore ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="d958c-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d958c-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="d958c-117">-ValuesToInclude</span></span>
<span data-ttu-id="d958c-118">La proprietà IncludeValues</span><span class="sxs-lookup"><span data-stu-id="d958c-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d958c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d958c-119">CommonParameters</span></span>
<span data-ttu-id="d958c-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d958c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d958c-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d958c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d958c-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="d958c-122">INPUTS</span></span>

### <span data-ttu-id="d958c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d958c-123">System.String</span></span>

### <span data-ttu-id="d958c-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d958c-124">System.String[]</span></span>

## <span data-ttu-id="d958c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d958c-125">OUTPUTS</span></span>

### <span data-ttu-id="d958c-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="d958c-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="d958c-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="d958c-127">NOTES</span></span>

## <span data-ttu-id="d958c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d958c-128">RELATED LINKS</span></span>
