---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 57741aa1f06816e8fac1bbb6722ea4d3c6f66761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018353"
---
# <span data-ttu-id="2f335-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2f335-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="2f335-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f335-102">SYNOPSIS</span></span>
<span data-ttu-id="2f335-103">Crea un oggetto di selezione della dimensione locale che può essere usato per creare criteri di avviso metrici.</span><span class="sxs-lookup"><span data-stu-id="2f335-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="2f335-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f335-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f335-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f335-105">DESCRIPTION</span></span>
<span data-ttu-id="2f335-106">Il cmdlet **New-AzMetricAlertRuleV2DimensionSelection** crea un oggetto di selezione della dimensione locale per facilitare la costruzione di criteri di avviso metrico usando il cmdlet **New-AzMetricAlertRuleV2Criteria** .</span><span class="sxs-lookup"><span data-stu-id="2f335-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="2f335-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f335-107">EXAMPLES</span></span>

### <span data-ttu-id="2f335-108">Esempio 1: creare un oggetto selezione dimensione</span><span class="sxs-lookup"><span data-stu-id="2f335-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="2f335-109">Questo comando crea un oggetto selezione dimensione che specifica che i valori {1,3,4} devono essere selezionati per la dimensione "lun"</span><span class="sxs-lookup"><span data-stu-id="2f335-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="2f335-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f335-110">PARAMETERS</span></span>

### <span data-ttu-id="2f335-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f335-111">-DefaultProfile</span></span>
<span data-ttu-id="2f335-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f335-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f335-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="2f335-113">-DimensionName</span></span>
<span data-ttu-id="2f335-114">Il nome della dimensione</span><span class="sxs-lookup"><span data-stu-id="2f335-114">The Dimension name</span></span>

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

### <span data-ttu-id="2f335-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="2f335-115">-ValuesToExclude</span></span>
<span data-ttu-id="2f335-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="2f335-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="2f335-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="2f335-117">-ValuesToInclude</span></span>
<span data-ttu-id="2f335-118">IncludeValues</span><span class="sxs-lookup"><span data-stu-id="2f335-118">The IncludeValues</span></span>

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

### <span data-ttu-id="2f335-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f335-119">CommonParameters</span></span>
<span data-ttu-id="2f335-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f335-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f335-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f335-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f335-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f335-122">INPUTS</span></span>

### <span data-ttu-id="2f335-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2f335-123">System.String</span></span>

### <span data-ttu-id="2f335-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="2f335-124">System.String[]</span></span>

## <span data-ttu-id="2f335-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f335-125">OUTPUTS</span></span>

### <span data-ttu-id="2f335-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="2f335-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="2f335-127">Note</span><span class="sxs-lookup"><span data-stu-id="2f335-127">NOTES</span></span>

## <span data-ttu-id="2f335-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f335-128">RELATED LINKS</span></span>
