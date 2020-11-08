---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203574"
---
# <span data-ttu-id="c18c4-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="c18c4-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="c18c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c18c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c18c4-103">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="c18c4-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="c18c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c18c4-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c18c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c18c4-105">DESCRIPTION</span></span>
<span data-ttu-id="c18c4-106">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato, incluse le risorse utilizzate e le risorse rimanenti nel piano.</span><span class="sxs-lookup"><span data-stu-id="c18c4-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="c18c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c18c4-107">EXAMPLES</span></span>

### <span data-ttu-id="c18c4-108">Esempio 1: ottenere la cronologia degli usi per un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="c18c4-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="c18c4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c18c4-109">PARAMETERS</span></span>

### <span data-ttu-id="c18c4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18c4-110">-DefaultProfile</span></span>
<span data-ttu-id="c18c4-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c18c4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c18c4-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="c18c4-112">-Name</span></span>
<span data-ttu-id="c18c4-113">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c18c4-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c18c4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c18c4-114">-ResourceGroupName</span></span>
<span data-ttu-id="c18c4-115">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c18c4-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c18c4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18c4-116">CommonParameters</span></span>
<span data-ttu-id="c18c4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c18c4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18c4-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c18c4-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18c4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c18c4-119">INPUTS</span></span>

### <span data-ttu-id="c18c4-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c18c4-120">None</span></span>

## <span data-ttu-id="c18c4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c18c4-121">OUTPUTS</span></span>

### <span data-ttu-id="c18c4-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="c18c4-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="c18c4-123">Note</span><span class="sxs-lookup"><span data-stu-id="c18c4-123">NOTES</span></span>
<span data-ttu-id="c18c4-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="c18c4-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c18c4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c18c4-125">RELATED LINKS</span></span>
