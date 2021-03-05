---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: b3ea89f2470052a0d5858da199ee5285b3d5ea18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965822"
---
# <span data-ttu-id="e8024-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e8024-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="e8024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8024-102">SYNOPSIS</span></span>
<span data-ttu-id="e8024-103">Recupera le informazioni di riepilogo per uno o più piani di impegno.</span><span class="sxs-lookup"><span data-stu-id="e8024-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="e8024-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8024-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8024-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8024-105">DESCRIPTION</span></span>
<span data-ttu-id="e8024-106">Recupera le informazioni sul piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="e8024-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="e8024-107">A seconda dei parametri passati, il cmdlet restituisce un piano di impegno specifico, una raccolta di piani di impegno per un determinato gruppo di risorse all'interno della sottoscrizione corrente o una raccolta di piani di impegno all'interno della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e8024-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="e8024-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8024-108">EXAMPLES</span></span>

### <span data-ttu-id="e8024-109">Esempio 1: Ottenere un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="e8024-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="e8024-110">Esempio 2: Ottenere tutte le risorse del piano di impegno nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="e8024-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="e8024-111">Esempio 3: Ottenere tutti i piani di impegno nella sottoscrizione corrente e nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e8024-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="e8024-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8024-112">PARAMETERS</span></span>

### <span data-ttu-id="e8024-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8024-113">-DefaultProfile</span></span>
<span data-ttu-id="e8024-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8024-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8024-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e8024-115">-Name</span></span>
<span data-ttu-id="e8024-116">Nome del piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="e8024-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="e8024-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8024-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8024-118">Nome del gruppo di risorse per il piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e8024-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e8024-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8024-119">CommonParameters</span></span>
<span data-ttu-id="e8024-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8024-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8024-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8024-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8024-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8024-122">INPUTS</span></span>

### <span data-ttu-id="e8024-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e8024-123">None</span></span>

## <span data-ttu-id="e8024-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8024-124">OUTPUTS</span></span>

### <span data-ttu-id="e8024-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e8024-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="e8024-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8024-126">NOTES</span></span>
<span data-ttu-id="e8024-127">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="e8024-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e8024-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8024-128">RELATED LINKS</span></span>
