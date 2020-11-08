---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189627"
---
# <span data-ttu-id="6345d-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="6345d-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="6345d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6345d-102">SYNOPSIS</span></span>
<span data-ttu-id="6345d-103">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="6345d-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="6345d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6345d-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6345d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6345d-105">DESCRIPTION</span></span>
<span data-ttu-id="6345d-106">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato, incluse le risorse utilizzate e le risorse rimanenti nel piano.</span><span class="sxs-lookup"><span data-stu-id="6345d-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="6345d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6345d-107">EXAMPLES</span></span>

### <span data-ttu-id="6345d-108">Esempio 1: ottenere la cronologia degli usi per un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="6345d-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="6345d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6345d-109">PARAMETERS</span></span>

### <span data-ttu-id="6345d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6345d-110">-DefaultProfile</span></span>
<span data-ttu-id="6345d-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6345d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6345d-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="6345d-112">-Name</span></span>
<span data-ttu-id="6345d-113">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6345d-113">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6345d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6345d-114">-ResourceGroupName</span></span>
<span data-ttu-id="6345d-115">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6345d-115">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6345d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6345d-116">CommonParameters</span></span>
<span data-ttu-id="6345d-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6345d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6345d-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6345d-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6345d-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6345d-119">INPUTS</span></span>

### <span data-ttu-id="6345d-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6345d-120">None</span></span>

## <span data-ttu-id="6345d-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6345d-121">OUTPUTS</span></span>

### <span data-ttu-id="6345d-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="6345d-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="6345d-123">Note</span><span class="sxs-lookup"><span data-stu-id="6345d-123">NOTES</span></span>
<span data-ttu-id="6345d-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="6345d-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6345d-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6345d-125">RELATED LINKS</span></span>
