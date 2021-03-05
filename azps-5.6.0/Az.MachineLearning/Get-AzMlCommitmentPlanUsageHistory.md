---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 8baf0e2af5ebc06e51c0f8b588fe04ff3106f892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009629"
---
# <span data-ttu-id="b550a-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="b550a-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="b550a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b550a-102">SYNOPSIS</span></span>
<span data-ttu-id="b550a-103">Recupera le informazioni della cronologia di utilizzo per un piano di impegno specificato.</span><span class="sxs-lookup"><span data-stu-id="b550a-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="b550a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b550a-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b550a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b550a-105">DESCRIPTION</span></span>
<span data-ttu-id="b550a-106">Recupera le informazioni sulla cronologia di utilizzo per un piano di impegno specificato, incluse le risorse usate e le risorse rimanenti al suo interno.</span><span class="sxs-lookup"><span data-stu-id="b550a-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="b550a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b550a-107">EXAMPLES</span></span>

### <span data-ttu-id="b550a-108">Esempio 1: Ottenere la cronologia di utilizzo per un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="b550a-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="b550a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b550a-109">PARAMETERS</span></span>

### <span data-ttu-id="b550a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b550a-110">-DefaultProfile</span></span>
<span data-ttu-id="b550a-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b550a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b550a-112">-Name</span><span class="sxs-lookup"><span data-stu-id="b550a-112">-Name</span></span>
<span data-ttu-id="b550a-113">Nome del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b550a-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b550a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b550a-114">-ResourceGroupName</span></span>
<span data-ttu-id="b550a-115">Nome del gruppo di risorse per il piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b550a-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b550a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b550a-116">CommonParameters</span></span>
<span data-ttu-id="b550a-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b550a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b550a-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b550a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b550a-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="b550a-119">INPUTS</span></span>

### <span data-ttu-id="b550a-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b550a-120">None</span></span>

## <span data-ttu-id="b550a-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b550a-121">OUTPUTS</span></span>

### <span data-ttu-id="b550a-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="b550a-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="b550a-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="b550a-123">NOTES</span></span>
<span data-ttu-id="b550a-124">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="b550a-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b550a-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b550a-125">RELATED LINKS</span></span>
