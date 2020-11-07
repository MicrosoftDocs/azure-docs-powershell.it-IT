---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: 138d9d7510331a385246c99e57ce3f460899ad33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852293"
---
# <span data-ttu-id="f5f13-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="f5f13-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="f5f13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5f13-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f13-103">Rimuovere un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5f13-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f5f13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5f13-104">SYNTAX</span></span>

### <span data-ttu-id="f5f13-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5f13-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f13-106">Tubazioni</span><span class="sxs-lookup"><span data-stu-id="f5f13-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f13-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5f13-107">DESCRIPTION</span></span>
<span data-ttu-id="f5f13-108">Il cmdlet Remove-AzConsumptionBudget consente di rimuovere un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5f13-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f5f13-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5f13-109">EXAMPLES</span></span>

### <span data-ttu-id="f5f13-110">Esempio 1: rimuovere un preventivo con un nome preventivo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="f5f13-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="f5f13-111">Esempio 2: rimuovere un preventivo con un nome preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f5f13-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="f5f13-112">Esempio 3: rimuovere un preventivo tramite piping a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="f5f13-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="f5f13-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5f13-113">PARAMETERS</span></span>

### <span data-ttu-id="f5f13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f13-114">-DefaultProfile</span></span>
<span data-ttu-id="f5f13-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f13-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5f13-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5f13-116">-InputObject</span></span>
<span data-ttu-id="f5f13-117">Oggetto preventivo.</span><span class="sxs-lookup"><span data-stu-id="f5f13-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f13-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5f13-118">-Name</span></span>
<span data-ttu-id="f5f13-119">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="f5f13-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f13-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5f13-120">-PassThru</span></span>
<span data-ttu-id="f5f13-121">Il cmdlet restituisce vero se un preventivo è stato rimosso correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5f13-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="f5f13-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f13-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5f13-123">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="f5f13-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f13-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f5f13-124">-Confirm</span></span>
<span data-ttu-id="f5f13-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f13-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f13-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f13-126">-WhatIf</span></span>
<span data-ttu-id="f5f13-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5f13-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5f13-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5f13-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f13-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f13-129">CommonParameters</span></span>
<span data-ttu-id="f5f13-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f13-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f13-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f13-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f13-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5f13-132">INPUTS</span></span>

### <span data-ttu-id="f5f13-133">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="f5f13-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="f5f13-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5f13-134">OUTPUTS</span></span>

### <span data-ttu-id="f5f13-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5f13-135">System.Boolean</span></span>

## <span data-ttu-id="f5f13-136">Note</span><span class="sxs-lookup"><span data-stu-id="f5f13-136">NOTES</span></span>

## <span data-ttu-id="f5f13-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5f13-137">RELATED LINKS</span></span>
