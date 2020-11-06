---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 3f7ed1a36cc95296ee7fdeec45c5039063032d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510392"
---
# <span data-ttu-id="31f7d-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="31f7d-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="31f7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="31f7d-103">Rimuove un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="31f7d-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31f7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31f7d-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31f7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="31f7d-106">Il cmdlet **Remove-AzureRmOperationalInsightsWorkspace** Elimina un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="31f7d-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="31f7d-107">Se l'area di lavoro è stata collegata a un account esistente tramite il parametro *CustomerID* al momento della creazione, l'account originale non viene eliminato nel portale delle informazioni operative.</span><span class="sxs-lookup"><span data-stu-id="31f7d-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="31f7d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31f7d-108">EXAMPLES</span></span>

### <span data-ttu-id="31f7d-109">Esempio 1: rimuovere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="31f7d-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="31f7d-110">Questo comando rimuove l'area di lavoro denominata Workspace dal gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31f7d-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="31f7d-111">Esempio 2: rimuovere un'area di lavoro usando la pipeline e senza conferma</span><span class="sxs-lookup"><span data-stu-id="31f7d-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="31f7d-112">Questo comando usa il cmdlet Get-AzureRmOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo passa al cmdlet **Remove-AzureRmOperationalInsightsWorkspace** usando l'operatore pipeline per rimuoverlo.</span><span class="sxs-lookup"><span data-stu-id="31f7d-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="31f7d-113">Dato che il parametro *Force* è specificato, il comando non richiede prima di rimuovere l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="31f7d-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="31f7d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31f7d-114">PARAMETERS</span></span>

### <span data-ttu-id="31f7d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="31f7d-115">-Force</span></span>
<span data-ttu-id="31f7d-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="31f7d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31f7d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="31f7d-117">-Name</span></span>
<span data-ttu-id="31f7d-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="31f7d-118">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="31f7d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f7d-119">-ResourceGroupName</span></span>
<span data-ttu-id="31f7d-120">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="31f7d-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="31f7d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31f7d-121">-Confirm</span></span>
<span data-ttu-id="31f7d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31f7d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31f7d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f7d-123">-WhatIf</span></span>
<span data-ttu-id="31f7d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31f7d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f7d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31f7d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31f7d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f7d-126">-DefaultProfile</span></span>
<span data-ttu-id="31f7d-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31f7d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31f7d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f7d-128">CommonParameters</span></span>
<span data-ttu-id="31f7d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f7d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f7d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f7d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f7d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31f7d-131">INPUTS</span></span>

## <span data-ttu-id="31f7d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31f7d-132">OUTPUTS</span></span>

## <span data-ttu-id="31f7d-133">Note</span><span class="sxs-lookup"><span data-stu-id="31f7d-133">NOTES</span></span>

## <span data-ttu-id="31f7d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31f7d-134">RELATED LINKS</span></span>

[<span data-ttu-id="31f7d-135">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="31f7d-135">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="31f7d-136">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="31f7d-136">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


