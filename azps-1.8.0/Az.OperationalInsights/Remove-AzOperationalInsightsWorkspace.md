---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 9758c0dda8d392100e57909edca310f14d3746af
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685387"
---
# <span data-ttu-id="fe0f1-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="fe0f1-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="fe0f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0f1-103">Rimuove un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-103">Removes a workspace.</span></span>

## <span data-ttu-id="fe0f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe0f1-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe0f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe0f1-105">DESCRIPTION</span></span>
<span data-ttu-id="fe0f1-106">Il cmdlet **Remove-AzOperationalInsightsWorkspace** Elimina un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="fe0f1-107">Se l'area di lavoro è stata collegata a un account esistente tramite il parametro *CustomerID* al momento della creazione, l'account originale non viene eliminato nel portale delle informazioni operative.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="fe0f1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe0f1-108">EXAMPLES</span></span>

### <span data-ttu-id="fe0f1-109">Esempio 1: rimuovere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="fe0f1-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="fe0f1-110">Questo comando rimuove l'area di lavoro denominata Workspace dal gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="fe0f1-111">Esempio 2: rimuovere un'area di lavoro usando la pipeline e senza conferma</span><span class="sxs-lookup"><span data-stu-id="fe0f1-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="fe0f1-112">Questo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo passa al cmdlet **Remove-AzOperationalInsightsWorkspace** usando l'operatore pipeline per rimuoverlo.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="fe0f1-113">Dato che il parametro *Force* è specificato, il comando non richiede prima di rimuovere l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="fe0f1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe0f1-114">PARAMETERS</span></span>

### <span data-ttu-id="fe0f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0f1-115">-DefaultProfile</span></span>
<span data-ttu-id="fe0f1-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fe0f1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe0f1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fe0f1-117">-Force</span></span>
<span data-ttu-id="fe0f1-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe0f1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe0f1-119">-Name</span></span>
<span data-ttu-id="fe0f1-120">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="fe0f1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0f1-121">-ResourceGroupName</span></span>
<span data-ttu-id="fe0f1-122">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="fe0f1-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe0f1-123">-Confirm</span></span>
<span data-ttu-id="fe0f1-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0f1-125">-WhatIf</span></span>
<span data-ttu-id="fe0f1-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe0f1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0f1-128">CommonParameters</span></span>
<span data-ttu-id="fe0f1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0f1-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0f1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0f1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe0f1-131">INPUTS</span></span>

### <span data-ttu-id="fe0f1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fe0f1-132">System.String</span></span>

## <span data-ttu-id="fe0f1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe0f1-133">OUTPUTS</span></span>

### <span data-ttu-id="fe0f1-134">System. void</span><span class="sxs-lookup"><span data-stu-id="fe0f1-134">System.Void</span></span>

## <span data-ttu-id="fe0f1-135">Note</span><span class="sxs-lookup"><span data-stu-id="fe0f1-135">NOTES</span></span>

## <span data-ttu-id="fe0f1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe0f1-136">RELATED LINKS</span></span>

[<span data-ttu-id="fe0f1-137">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="fe0f1-137">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="fe0f1-138">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="fe0f1-138">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


