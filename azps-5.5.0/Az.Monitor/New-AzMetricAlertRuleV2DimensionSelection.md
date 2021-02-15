---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 500a0bed47fad0174e3e7efb3ee27e2bb98a9894
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190119"
---
# <span data-ttu-id="6d5e1-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6d5e1-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="6d5e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5e1-103">Crea un oggetto di selezione della dimensione locale che può essere usato per creare criteri di avviso metrica.</span><span class="sxs-lookup"><span data-stu-id="6d5e1-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="6d5e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d5e1-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d5e1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d5e1-105">DESCRIPTION</span></span>
<span data-ttu-id="6d5e1-106">Il cmdlet **New-AzMetricAlertRuleV2DimensionSelection** crea un oggetto di selezione della dimensione locale per facilitare la costruzione dei criteri di avviso della metrica usando il cmdlet [New-AzMetricAlertRuleV2Criteria.](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="6d5e1-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="6d5e1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d5e1-107">EXAMPLES</span></span>

### <span data-ttu-id="6d5e1-108">Esempio 1: Creare un oggetto di selezione della dimensione</span><span class="sxs-lookup"><span data-stu-id="6d5e1-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="6d5e1-109">Questo comando crea un oggetto di selezione della dimensione che specifica che è necessario selezionare {1,3,4} i valori per la dimensione "LUN"</span><span class="sxs-lookup"><span data-stu-id="6d5e1-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="6d5e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d5e1-110">PARAMETERS</span></span>

### <span data-ttu-id="6d5e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5e1-111">-DefaultProfile</span></span>
<span data-ttu-id="6d5e1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5e1-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="6d5e1-113">-DimensionName</span></span>
<span data-ttu-id="6d5e1-114">Nome della dimensione</span><span class="sxs-lookup"><span data-stu-id="6d5e1-114">The Dimension name</span></span>

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

### <span data-ttu-id="6d5e1-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="6d5e1-115">-ValuesToExclude</span></span>
<span data-ttu-id="6d5e1-116">Valore ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="6d5e1-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="6d5e1-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="6d5e1-117">-ValuesToInclude</span></span>
<span data-ttu-id="6d5e1-118">La proprietà IncludeValues</span><span class="sxs-lookup"><span data-stu-id="6d5e1-118">The IncludeValues</span></span>

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

### <span data-ttu-id="6d5e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5e1-119">CommonParameters</span></span>
<span data-ttu-id="6d5e1-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d5e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5e1-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d5e1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5e1-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d5e1-122">INPUTS</span></span>

### <span data-ttu-id="6d5e1-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6d5e1-123">System.String</span></span>

### <span data-ttu-id="6d5e1-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6d5e1-124">System.String[]</span></span>

## <span data-ttu-id="6d5e1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d5e1-125">OUTPUTS</span></span>

### <span data-ttu-id="6d5e1-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="6d5e1-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="6d5e1-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d5e1-127">NOTES</span></span>

## <span data-ttu-id="6d5e1-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d5e1-128">RELATED LINKS</span></span>
