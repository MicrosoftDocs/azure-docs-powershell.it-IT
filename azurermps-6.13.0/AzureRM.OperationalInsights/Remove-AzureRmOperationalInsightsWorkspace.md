---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 5a222b404aa931cec468ee5dfc66963f48b23ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509196"
---
# <span data-ttu-id="2ed2a-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2ed2a-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="2ed2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ed2a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed2a-103">Rimuove un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ed2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ed2a-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ed2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ed2a-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed2a-106">Il cmdlet **Remove-AzureRmOperationalInsightsWorkspace** Elimina un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="2ed2a-107">Se l'area di lavoro è stata collegata a un account esistente tramite il parametro *CustomerID* al momento della creazione, l'account originale non viene eliminato nel portale delle informazioni operative.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="2ed2a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ed2a-108">EXAMPLES</span></span>

### <span data-ttu-id="2ed2a-109">Esempio 1: rimuovere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="2ed2a-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="2ed2a-110">Questo comando rimuove l'area di lavoro denominata Workspace dal gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="2ed2a-111">Esempio 2: rimuovere un'area di lavoro usando la pipeline e senza conferma</span><span class="sxs-lookup"><span data-stu-id="2ed2a-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="2ed2a-112">Questo comando usa il cmdlet Get-AzureRmOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo passa al cmdlet **Remove-AzureRmOperationalInsightsWorkspace** usando l'operatore pipeline per rimuoverlo.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="2ed2a-113">Dato che il parametro *Force* è specificato, il comando non richiede prima di rimuovere l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="2ed2a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ed2a-114">PARAMETERS</span></span>

### <span data-ttu-id="2ed2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed2a-115">-DefaultProfile</span></span>
<span data-ttu-id="2ed2a-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2ed2a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ed2a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2ed2a-117">-Force</span></span>
<span data-ttu-id="2ed2a-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2ed2a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ed2a-119">-Name</span></span>
<span data-ttu-id="2ed2a-120">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="2ed2a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed2a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ed2a-122">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="2ed2a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ed2a-123">-Confirm</span></span>
<span data-ttu-id="2ed2a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ed2a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed2a-125">-WhatIf</span></span>
<span data-ttu-id="2ed2a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ed2a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ed2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed2a-128">CommonParameters</span></span>
<span data-ttu-id="2ed2a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed2a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed2a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed2a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ed2a-131">INPUTS</span></span>

### <span data-ttu-id="2ed2a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ed2a-132">System.String</span></span>

## <span data-ttu-id="2ed2a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ed2a-133">OUTPUTS</span></span>

### <span data-ttu-id="2ed2a-134">System. void</span><span class="sxs-lookup"><span data-stu-id="2ed2a-134">System.Void</span></span>

## <span data-ttu-id="2ed2a-135">Note</span><span class="sxs-lookup"><span data-stu-id="2ed2a-135">NOTES</span></span>

## <span data-ttu-id="2ed2a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ed2a-136">RELATED LINKS</span></span>

[<span data-ttu-id="2ed2a-137">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="2ed2a-137">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="2ed2a-138">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2ed2a-138">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


