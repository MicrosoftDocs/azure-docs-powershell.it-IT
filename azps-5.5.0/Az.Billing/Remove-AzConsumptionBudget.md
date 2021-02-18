---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200935"
---
# <span data-ttu-id="fecc8-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="fecc8-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="fecc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fecc8-102">SYNOPSIS</span></span>
<span data-ttu-id="fecc8-103">Rimuovere un preventivo in una sottoscrizione o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fecc8-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="fecc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fecc8-104">SYNTAX</span></span>

### <span data-ttu-id="fecc8-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fecc8-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecc8-106">Piping</span><span class="sxs-lookup"><span data-stu-id="fecc8-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fecc8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fecc8-107">DESCRIPTION</span></span>
<span data-ttu-id="fecc8-108">Il cmdlet Remove-AzConsumptionBudget rimuove un preventivo in una sottoscrizione o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fecc8-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="fecc8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fecc8-109">EXAMPLES</span></span>

### <span data-ttu-id="fecc8-110">Esempio 1: Rimuovere un budget con un nome di budget a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="fecc8-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="fecc8-111">Esempio 2: Rimuovere un preventivo con un nome di preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fecc8-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="fecc8-112">Esempio 3: Rimuovere un budget tramite piping a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="fecc8-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="fecc8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fecc8-113">PARAMETERS</span></span>

### <span data-ttu-id="fecc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fecc8-114">-DefaultProfile</span></span>
<span data-ttu-id="fecc8-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fecc8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fecc8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fecc8-116">-InputObject</span></span>
<span data-ttu-id="fecc8-117">Oggetto Budget.</span><span class="sxs-lookup"><span data-stu-id="fecc8-117">Budget object.</span></span>

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

### <span data-ttu-id="fecc8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fecc8-118">-Name</span></span>
<span data-ttu-id="fecc8-119">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="fecc8-119">Name of a budget.</span></span>

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

### <span data-ttu-id="fecc8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fecc8-120">-PassThru</span></span>
<span data-ttu-id="fecc8-121">Il cmdlet restituisce true se un budget è stato rimosso correttamente.</span><span class="sxs-lookup"><span data-stu-id="fecc8-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="fecc8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fecc8-122">-ResourceGroupName</span></span>
<span data-ttu-id="fecc8-123">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="fecc8-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="fecc8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fecc8-124">-Confirm</span></span>
<span data-ttu-id="fecc8-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fecc8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fecc8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fecc8-126">-WhatIf</span></span>
<span data-ttu-id="fecc8-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fecc8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fecc8-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fecc8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fecc8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecc8-129">CommonParameters</span></span>
<span data-ttu-id="fecc8-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fecc8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecc8-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fecc8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecc8-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="fecc8-132">INPUTS</span></span>

### <span data-ttu-id="fecc8-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="fecc8-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="fecc8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fecc8-134">OUTPUTS</span></span>

### <span data-ttu-id="fecc8-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fecc8-135">System.Boolean</span></span>

## <span data-ttu-id="fecc8-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="fecc8-136">NOTES</span></span>

## <span data-ttu-id="fecc8-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fecc8-137">RELATED LINKS</span></span>
