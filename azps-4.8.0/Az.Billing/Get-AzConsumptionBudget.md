---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190546"
---
# <span data-ttu-id="e751d-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="e751d-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="e751d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e751d-102">SYNOPSIS</span></span>
<span data-ttu-id="e751d-103">Ottenere un elenco di budget in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e751d-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="e751d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e751d-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="e751d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e751d-105">DESCRIPTION</span></span>
<span data-ttu-id="e751d-106">Il cmdlet Get-AzConsumptionBudget ottiene un elenco di budget in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e751d-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="e751d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e751d-107">EXAMPLES</span></span>

### <span data-ttu-id="e751d-108">Esempio 1: ottenere un elenco di budget a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="e751d-108">Example 1: Get a list of budgets at subscription level</span></span>
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

### <span data-ttu-id="e751d-109">Esempio 2: ottenere un elenco di budget a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e751d-109">Example 2: Get a list of budgets at resource group level</span></span>
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

### <span data-ttu-id="e751d-110">Esempio 3: ottenere un preventivo con il nome del preventivo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="e751d-110">Example 3: Get a budget with the budget name at subscription level</span></span>
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

### <span data-ttu-id="e751d-111">Esempio 4: ottenere un preventivo con il nome del preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e751d-111">Example 4: Get a budget with the budget name at resource group level</span></span>
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

## <span data-ttu-id="e751d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e751d-112">PARAMETERS</span></span>

### <span data-ttu-id="e751d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e751d-113">-DefaultProfile</span></span>
<span data-ttu-id="e751d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e751d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e751d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e751d-115">-Name</span></span>
<span data-ttu-id="e751d-116">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="e751d-116">Name of a budget.</span></span>

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

### <span data-ttu-id="e751d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e751d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e751d-118">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="e751d-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="e751d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e751d-119">CommonParameters</span></span>
<span data-ttu-id="e751d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e751d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e751d-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e751d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e751d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e751d-122">INPUTS</span></span>

### <span data-ttu-id="e751d-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e751d-123">None</span></span>

## <span data-ttu-id="e751d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e751d-124">OUTPUTS</span></span>

### <span data-ttu-id="e751d-125">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="e751d-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="e751d-126">Note</span><span class="sxs-lookup"><span data-stu-id="e751d-126">NOTES</span></span>

## <span data-ttu-id="e751d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e751d-127">RELATED LINKS</span></span>