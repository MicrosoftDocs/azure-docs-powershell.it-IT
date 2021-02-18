---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: d02338c34584a68ece2ad3a90887a765f8142347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202318"
---
# <span data-ttu-id="d10e6-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d10e6-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="d10e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d10e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d10e6-103">Rimuove un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d10e6-103">Removes a workspace.</span></span>

## <span data-ttu-id="d10e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d10e6-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d10e6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d10e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d10e6-106">Il cmdlet **Remove-AzOperationalInsightsWorkspace** elimina un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="d10e6-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="d10e6-107">Se questa area di lavoro era collegata a un account esistente tramite il parametro *CustomerId* al momento della creazione, l'account originale non viene eliminato nel portale di Analisi operativa.</span><span class="sxs-lookup"><span data-stu-id="d10e6-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="d10e6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d10e6-108">EXAMPLES</span></span>

### <span data-ttu-id="d10e6-109">Esempio 1: Rimuovere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="d10e6-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="d10e6-110">Questo comando rimuove l'area di lavoro denominata MyWorkspace dal gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d10e6-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="d10e6-111">Esempio 2: Rimuovere un'area di lavoro tramite la pipeline e senza conferma</span><span class="sxs-lookup"><span data-stu-id="d10e6-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="d10e6-112">Questo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata MyWorkspace e quindi la passa al cmdlet **Remove-AzOperationalInsightsWorkspace** usando l'operatore della pipeline per rimuoverla.</span><span class="sxs-lookup"><span data-stu-id="d10e6-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="d10e6-113">Poiché è *specificato il parametro Force,* il comando non richiede conferma prima di rimuovere l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d10e6-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="d10e6-114">Esempio 3: Forzare l'eliminazione dell'area di lavoro (non può essere recuperata)</span><span class="sxs-lookup"><span data-stu-id="d10e6-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="d10e6-115">Forzare l'eliminazione di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d10e6-115">Force delete a workspace.</span></span>

## <span data-ttu-id="d10e6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d10e6-116">PARAMETERS</span></span>

### <span data-ttu-id="d10e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10e6-117">-DefaultProfile</span></span>
<span data-ttu-id="d10e6-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d10e6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d10e6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d10e6-119">-Force</span></span>
<span data-ttu-id="d10e6-120">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="d10e6-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d10e6-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="d10e6-121">-ForceDelete</span></span>
<span data-ttu-id="d10e6-122">Forzare l'eliminazione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d10e6-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="d10e6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d10e6-123">-Name</span></span>
<span data-ttu-id="d10e6-124">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d10e6-124">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10e6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d10e6-125">-ResourceGroupName</span></span>
<span data-ttu-id="d10e6-126">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="d10e6-126">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10e6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d10e6-127">-Confirm</span></span>
<span data-ttu-id="d10e6-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d10e6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10e6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10e6-129">-WhatIf</span></span>
<span data-ttu-id="d10e6-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d10e6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d10e6-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d10e6-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10e6-132">CommonParameters</span></span>
<span data-ttu-id="d10e6-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d10e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10e6-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d10e6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10e6-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="d10e6-135">INPUTS</span></span>

### <span data-ttu-id="d10e6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d10e6-136">System.String</span></span>

## <span data-ttu-id="d10e6-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d10e6-137">OUTPUTS</span></span>

### <span data-ttu-id="d10e6-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="d10e6-138">System.Void</span></span>

## <span data-ttu-id="d10e6-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="d10e6-139">NOTES</span></span>

## <span data-ttu-id="d10e6-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d10e6-140">RELATED LINKS</span></span>

[<span data-ttu-id="d10e6-141">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="d10e6-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="d10e6-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d10e6-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


