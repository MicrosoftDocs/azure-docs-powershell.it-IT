---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: 1c34c4a6e7d9621d1afc0cf06d841eceb2b34cb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675631"
---
# <span data-ttu-id="85213-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="85213-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="85213-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85213-102">SYNOPSIS</span></span>
<span data-ttu-id="85213-103">Ottenere un elenco di budget in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85213-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="85213-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85213-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="85213-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85213-105">DESCRIPTION</span></span>
<span data-ttu-id="85213-106">Il cmdlet Get-AzConsumptionBudget ottiene un elenco di budget in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85213-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="85213-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85213-107">EXAMPLES</span></span>

### <span data-ttu-id="85213-108">Esempio 1: ottenere un elenco di budget a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="85213-108">Example 1: Get a list of budgets at subscription level</span></span>
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

### <span data-ttu-id="85213-109">Esempio 2: ottenere un elenco di budget a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="85213-109">Example 2: Get a list of budgets at resource group level</span></span>
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

### <span data-ttu-id="85213-110">Esempio 3: ottenere un preventivo con il nome del preventivo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="85213-110">Example 3: Get a budget with the budget name at subscription level</span></span>
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

### <span data-ttu-id="85213-111">Esempio 4: ottenere un preventivo con il nome del preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="85213-111">Example 4: Get a budget with the budget name at resource group level</span></span>
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

## <span data-ttu-id="85213-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85213-112">PARAMETERS</span></span>

### <span data-ttu-id="85213-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85213-113">-DefaultProfile</span></span>
<span data-ttu-id="85213-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85213-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85213-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="85213-115">-Name</span></span>
<span data-ttu-id="85213-116">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="85213-116">Name of a budget.</span></span>

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

### <span data-ttu-id="85213-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85213-117">-ResourceGroupName</span></span>
<span data-ttu-id="85213-118">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="85213-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="85213-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85213-119">CommonParameters</span></span>
<span data-ttu-id="85213-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85213-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85213-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85213-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85213-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85213-122">INPUTS</span></span>

### <span data-ttu-id="85213-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="85213-123">None</span></span>

## <span data-ttu-id="85213-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85213-124">OUTPUTS</span></span>

### <span data-ttu-id="85213-125">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="85213-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="85213-126">Note</span><span class="sxs-lookup"><span data-stu-id="85213-126">NOTES</span></span>

## <span data-ttu-id="85213-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85213-127">RELATED LINKS</span></span>
