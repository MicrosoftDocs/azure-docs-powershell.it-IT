---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189629"
---
# <span data-ttu-id="ab588-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab588-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="ab588-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab588-102">SYNOPSIS</span></span>
<span data-ttu-id="ab588-103">Recupera le informazioni di riepilogo per uno o più piani di impegno.</span><span class="sxs-lookup"><span data-stu-id="ab588-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="ab588-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab588-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab588-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab588-105">DESCRIPTION</span></span>
<span data-ttu-id="ab588-106">Recupera le informazioni sul piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="ab588-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="ab588-107">A seconda dei parametri passati, il cmdlet restituisce il piano di impegno specifico, una raccolta di piani di impegno per un gruppo di risorse specificato nell'abbonamento corrente o una raccolta di piani di impegno nell'ambito dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ab588-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="ab588-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab588-108">EXAMPLES</span></span>

### <span data-ttu-id="ab588-109">Esempio 1: ottenere un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="ab588-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="ab588-110">Esempio 2: ottenere tutte le risorse del piano di impegno nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="ab588-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="ab588-111">Esempio 3: ottenere tutti i piani di impegno nell'abbonamento corrente e nel gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="ab588-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="ab588-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab588-112">PARAMETERS</span></span>

### <span data-ttu-id="ab588-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab588-113">-DefaultProfile</span></span>
<span data-ttu-id="ab588-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab588-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab588-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab588-115">-Name</span></span>
<span data-ttu-id="ab588-116">Nome del piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="ab588-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="ab588-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab588-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab588-118">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ab588-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ab588-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab588-119">CommonParameters</span></span>
<span data-ttu-id="ab588-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab588-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab588-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab588-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab588-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab588-122">INPUTS</span></span>

### <span data-ttu-id="ab588-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ab588-123">None</span></span>

## <span data-ttu-id="ab588-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab588-124">OUTPUTS</span></span>

### <span data-ttu-id="ab588-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab588-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="ab588-126">Note</span><span class="sxs-lookup"><span data-stu-id="ab588-126">NOTES</span></span>
<span data-ttu-id="ab588-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ab588-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ab588-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab588-128">RELATED LINKS</span></span>
