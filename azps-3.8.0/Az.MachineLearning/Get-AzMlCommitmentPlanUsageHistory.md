---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022201"
---
# <span data-ttu-id="259c3-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="259c3-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="259c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="259c3-102">SYNOPSIS</span></span>
<span data-ttu-id="259c3-103">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="259c3-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="259c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="259c3-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="259c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="259c3-105">DESCRIPTION</span></span>
<span data-ttu-id="259c3-106">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato, incluse le risorse utilizzate e le risorse rimanenti nel piano.</span><span class="sxs-lookup"><span data-stu-id="259c3-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="259c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="259c3-107">EXAMPLES</span></span>

### <span data-ttu-id="259c3-108">Esempio 1: ottenere la cronologia degli usi per un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="259c3-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="259c3-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="259c3-109">PARAMETERS</span></span>

### <span data-ttu-id="259c3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259c3-110">-DefaultProfile</span></span>
<span data-ttu-id="259c3-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="259c3-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="259c3-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="259c3-112">-Name</span></span>
<span data-ttu-id="259c3-113">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="259c3-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="259c3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259c3-114">-ResourceGroupName</span></span>
<span data-ttu-id="259c3-115">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="259c3-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="259c3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259c3-116">CommonParameters</span></span>
<span data-ttu-id="259c3-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="259c3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259c3-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="259c3-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259c3-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="259c3-119">INPUTS</span></span>

### <span data-ttu-id="259c3-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="259c3-120">None</span></span>

## <span data-ttu-id="259c3-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="259c3-121">OUTPUTS</span></span>

### <span data-ttu-id="259c3-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="259c3-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="259c3-123">Note</span><span class="sxs-lookup"><span data-stu-id="259c3-123">NOTES</span></span>
<span data-ttu-id="259c3-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="259c3-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="259c3-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="259c3-125">RELATED LINKS</span></span>
