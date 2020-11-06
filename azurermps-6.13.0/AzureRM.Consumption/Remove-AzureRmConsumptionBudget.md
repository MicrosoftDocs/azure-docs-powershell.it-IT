---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520246"
---
# <span data-ttu-id="f72cc-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="f72cc-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="f72cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f72cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f72cc-103">Rimuovere un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f72cc-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f72cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f72cc-104">SYNTAX</span></span>

### <span data-ttu-id="f72cc-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f72cc-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f72cc-106">Tubazioni</span><span class="sxs-lookup"><span data-stu-id="f72cc-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f72cc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f72cc-107">DESCRIPTION</span></span>
<span data-ttu-id="f72cc-108">Il cmdlet Remove-AzureRmConsumptionBudget consente di rimuovere un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f72cc-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f72cc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f72cc-109">EXAMPLES</span></span>

### <span data-ttu-id="f72cc-110">Esempio 1: rimuovere un preventivo con un nome preventivo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="f72cc-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="f72cc-111">Esempio 2: rimuovere un preventivo con un nome preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f72cc-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="f72cc-112">Esempio 3: rimuovere un preventivo tramite piping a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="f72cc-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="f72cc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f72cc-113">PARAMETERS</span></span>

### <span data-ttu-id="f72cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72cc-114">-DefaultProfile</span></span>
<span data-ttu-id="f72cc-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f72cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72cc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f72cc-116">-InputObject</span></span>
<span data-ttu-id="f72cc-117">Oggetto preventivo.</span><span class="sxs-lookup"><span data-stu-id="f72cc-117">Budget object.</span></span>

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

### <span data-ttu-id="f72cc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f72cc-118">-Name</span></span>
<span data-ttu-id="f72cc-119">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="f72cc-119">Name of a budget.</span></span>

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

### <span data-ttu-id="f72cc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f72cc-120">-PassThru</span></span>
<span data-ttu-id="f72cc-121">Il cmdlet restituisce vero se un preventivo è stato rimosso correttamente.</span><span class="sxs-lookup"><span data-stu-id="f72cc-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="f72cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f72cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="f72cc-123">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="f72cc-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="f72cc-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f72cc-124">-Confirm</span></span>
<span data-ttu-id="f72cc-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f72cc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f72cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f72cc-126">-WhatIf</span></span>
<span data-ttu-id="f72cc-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f72cc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f72cc-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f72cc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f72cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72cc-129">CommonParameters</span></span>
<span data-ttu-id="f72cc-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72cc-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72cc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72cc-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f72cc-132">INPUTS</span></span>

### <span data-ttu-id="f72cc-133">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="f72cc-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="f72cc-134">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f72cc-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f72cc-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f72cc-135">OUTPUTS</span></span>

### <span data-ttu-id="f72cc-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f72cc-136">System.Boolean</span></span>

## <span data-ttu-id="f72cc-137">Note</span><span class="sxs-lookup"><span data-stu-id="f72cc-137">NOTES</span></span>

## <span data-ttu-id="f72cc-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f72cc-138">RELATED LINKS</span></span>
