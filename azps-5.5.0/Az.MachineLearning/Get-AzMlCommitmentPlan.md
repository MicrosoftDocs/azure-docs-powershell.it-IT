---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180342"
---
# <span data-ttu-id="10341-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="10341-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="10341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10341-102">SYNOPSIS</span></span>
<span data-ttu-id="10341-103">Recupera le informazioni di riepilogo per uno o più piani di impegno.</span><span class="sxs-lookup"><span data-stu-id="10341-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="10341-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10341-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10341-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10341-105">DESCRIPTION</span></span>
<span data-ttu-id="10341-106">Recupera le informazioni sul piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="10341-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="10341-107">A seconda dei parametri passati, il cmdlet restituisce un piano di impegno specifico, una raccolta di piani di impegno per un determinato gruppo di risorse all'interno della sottoscrizione corrente o una raccolta di piani di impegno all'interno della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="10341-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="10341-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10341-108">EXAMPLES</span></span>

### <span data-ttu-id="10341-109">Esempio 1: Ottenere un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="10341-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="10341-110">Esempio 2: Ottenere tutte le risorse del piano di impegno nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="10341-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="10341-111">Esempio 3: Ottenere tutti i piani di impegno nella sottoscrizione corrente e nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="10341-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="10341-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10341-112">PARAMETERS</span></span>

### <span data-ttu-id="10341-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10341-113">-DefaultProfile</span></span>
<span data-ttu-id="10341-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="10341-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10341-115">-Name</span><span class="sxs-lookup"><span data-stu-id="10341-115">-Name</span></span>
<span data-ttu-id="10341-116">Nome del piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="10341-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="10341-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10341-117">-ResourceGroupName</span></span>
<span data-ttu-id="10341-118">Nome del gruppo di risorse per il piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="10341-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="10341-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10341-119">CommonParameters</span></span>
<span data-ttu-id="10341-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10341-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10341-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10341-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10341-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="10341-122">INPUTS</span></span>

### <span data-ttu-id="10341-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="10341-123">None</span></span>

## <span data-ttu-id="10341-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10341-124">OUTPUTS</span></span>

### <span data-ttu-id="10341-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="10341-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="10341-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="10341-126">NOTES</span></span>
<span data-ttu-id="10341-127">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="10341-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="10341-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10341-128">RELATED LINKS</span></span>
