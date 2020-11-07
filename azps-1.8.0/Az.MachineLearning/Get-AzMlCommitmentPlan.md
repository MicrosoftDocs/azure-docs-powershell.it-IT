---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 0b66c75c3230754656b14e15eda66a4fb2912c4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835331"
---
# <span data-ttu-id="762f7-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="762f7-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="762f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="762f7-102">SYNOPSIS</span></span>
<span data-ttu-id="762f7-103">Recupera le informazioni di riepilogo per uno o più piani di impegno.</span><span class="sxs-lookup"><span data-stu-id="762f7-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="762f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="762f7-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="762f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="762f7-105">DESCRIPTION</span></span>
<span data-ttu-id="762f7-106">Recupera le informazioni sul piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="762f7-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="762f7-107">A seconda dei Paramenters passati, il cmdlet restituisce il piano di impegno specifico, una raccolta di piani di impegno per un gruppo di risorse specificato nell'abbonamento corrente o una raccolta di piani di impegno nell'ambito dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="762f7-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="762f7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="762f7-108">EXAMPLES</span></span>

### <span data-ttu-id="762f7-109">Esempio 1: ottenere un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="762f7-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="762f7-110">Esempio 2: ottenere tutte le risorse del piano di impegno nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="762f7-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="762f7-111">Esempio 3: ottenere tutti i piani di impegno nell'abbonamento corrente e nel gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="762f7-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="762f7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="762f7-112">PARAMETERS</span></span>

### <span data-ttu-id="762f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762f7-113">-DefaultProfile</span></span>
<span data-ttu-id="762f7-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="762f7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="762f7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="762f7-115">-Name</span></span>
<span data-ttu-id="762f7-116">Nome del piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="762f7-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="762f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="762f7-118">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="762f7-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="762f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762f7-119">CommonParameters</span></span>
<span data-ttu-id="762f7-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762f7-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="762f7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762f7-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="762f7-122">INPUTS</span></span>

### <span data-ttu-id="762f7-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="762f7-123">None</span></span>

## <span data-ttu-id="762f7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="762f7-124">OUTPUTS</span></span>

### <span data-ttu-id="762f7-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="762f7-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="762f7-126">Note</span><span class="sxs-lookup"><span data-stu-id="762f7-126">NOTES</span></span>
<span data-ttu-id="762f7-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="762f7-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="762f7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="762f7-128">RELATED LINKS</span></span>
