---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343576"
---
# <span data-ttu-id="ce527-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="ce527-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="ce527-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce527-102">SYNOPSIS</span></span>
<span data-ttu-id="ce527-103">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="ce527-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="ce527-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce527-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce527-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce527-105">DESCRIPTION</span></span>
<span data-ttu-id="ce527-106">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato, incluse le risorse utilizzate e le risorse rimanenti nel piano.</span><span class="sxs-lookup"><span data-stu-id="ce527-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="ce527-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce527-107">EXAMPLES</span></span>

### <span data-ttu-id="ce527-108">Esempio 1: ottenere la cronologia degli usi per un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="ce527-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="ce527-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce527-109">PARAMETERS</span></span>

### <span data-ttu-id="ce527-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce527-110">-DefaultProfile</span></span>
<span data-ttu-id="ce527-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ce527-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce527-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce527-112">-Name</span></span>
<span data-ttu-id="ce527-113">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ce527-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ce527-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce527-114">-ResourceGroupName</span></span>
<span data-ttu-id="ce527-115">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ce527-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ce527-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce527-116">CommonParameters</span></span>
<span data-ttu-id="ce527-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce527-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce527-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce527-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce527-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce527-119">INPUTS</span></span>

### <span data-ttu-id="ce527-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ce527-120">None</span></span>

## <span data-ttu-id="ce527-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce527-121">OUTPUTS</span></span>

### <span data-ttu-id="ce527-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="ce527-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="ce527-123">Note</span><span class="sxs-lookup"><span data-stu-id="ce527-123">NOTES</span></span>
<span data-ttu-id="ce527-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ce527-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ce527-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce527-125">RELATED LINKS</span></span>
