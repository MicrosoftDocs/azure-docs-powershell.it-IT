---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: f0b081911d1bcd2a2b195d3185eb3b36505060c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686178"
---
# <span data-ttu-id="f8dd7-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f8dd7-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="f8dd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="f8dd7-103">Recupera le informazioni di riepilogo per uno o più piani di impegno.</span><span class="sxs-lookup"><span data-stu-id="f8dd7-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8dd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8dd7-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8dd7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="f8dd7-106">Recupera le informazioni sul piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="f8dd7-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="f8dd7-107">A seconda dei Paramenters passati, il cmdlet restituisce il piano di impegno specifico, una raccolta di piani di impegno per un gruppo di risorse specificato nell'abbonamento corrente o una raccolta di piani di impegno nell'ambito dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f8dd7-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="f8dd7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8dd7-108">EXAMPLES</span></span>

### <span data-ttu-id="f8dd7-109">Esempio 1: ottenere un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="f8dd7-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="f8dd7-110">Esempio 2: ottenere tutte le risorse del piano di impegno nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="f8dd7-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="f8dd7-111">Esempio 3: ottenere tutti i piani di impegno nell'abbonamento corrente e nel gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="f8dd7-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="f8dd7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8dd7-112">PARAMETERS</span></span>

### <span data-ttu-id="f8dd7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8dd7-113">-DefaultProfile</span></span>
<span data-ttu-id="f8dd7-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f8dd7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8dd7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8dd7-115">-Name</span></span>
<span data-ttu-id="f8dd7-116">Nome del piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="f8dd7-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="f8dd7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8dd7-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8dd7-118">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f8dd7-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f8dd7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8dd7-119">CommonParameters</span></span>
<span data-ttu-id="f8dd7-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8dd7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8dd7-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8dd7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8dd7-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8dd7-122">INPUTS</span></span>

### <span data-ttu-id="f8dd7-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f8dd7-123">None</span></span>

## <span data-ttu-id="f8dd7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8dd7-124">OUTPUTS</span></span>

### <span data-ttu-id="f8dd7-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f8dd7-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f8dd7-126">Note</span><span class="sxs-lookup"><span data-stu-id="f8dd7-126">NOTES</span></span>
<span data-ttu-id="f8dd7-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f8dd7-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f8dd7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8dd7-128">RELATED LINKS</span></span>
