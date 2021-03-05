---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: 70f7f9c43612f1fd1248e019d970d157fadab000
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986213"
---
# <span data-ttu-id="1b6e9-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="1b6e9-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="1b6e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6e9-103">Ottenere un elenco dei preventivi in una sottoscrizione o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1b6e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b6e9-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="1b6e9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b6e9-105">DESCRIPTION</span></span>
<span data-ttu-id="1b6e9-106">Il Get-AzConsumptionBudget cmdlet ottiene un elenco di preventivi in una sottoscrizione o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1b6e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b6e9-107">EXAMPLES</span></span>

### <span data-ttu-id="1b6e9-108">Esempio 1: Ottenere un elenco dei budget a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="1b6e9-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1b6e9-109">Esempio 2: Ottenere un elenco di preventivi a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1b6e9-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1b6e9-110">Esempio 3: Ottenere un budget con il nome del budget a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="1b6e9-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1b6e9-111">Esempio 4: Creare un preventivo con il nome del preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1b6e9-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="1b6e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b6e9-112">PARAMETERS</span></span>

### <span data-ttu-id="1b6e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6e9-113">-DefaultProfile</span></span>
<span data-ttu-id="1b6e9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b6e9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1b6e9-115">-Name</span></span>
<span data-ttu-id="1b6e9-116">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-116">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b6e9-118">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-118">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6e9-119">CommonParameters</span></span>
<span data-ttu-id="1b6e9-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6e9-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6e9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6e9-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b6e9-122">INPUTS</span></span>

### <span data-ttu-id="1b6e9-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b6e9-123">None</span></span>

## <span data-ttu-id="1b6e9-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b6e9-124">OUTPUTS</span></span>

### <span data-ttu-id="1b6e9-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="1b6e9-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="1b6e9-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b6e9-126">NOTES</span></span>

## <span data-ttu-id="1b6e9-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b6e9-127">RELATED LINKS</span></span>
