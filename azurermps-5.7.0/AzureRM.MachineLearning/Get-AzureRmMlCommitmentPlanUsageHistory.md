---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93688671"
---
# <span data-ttu-id="365e3-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="365e3-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="365e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="365e3-102">SYNOPSIS</span></span>
<span data-ttu-id="365e3-103">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="365e3-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="365e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="365e3-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="365e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="365e3-105">DESCRIPTION</span></span>
<span data-ttu-id="365e3-106">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato, incluse le risorse utilizzate e le risorse rimanenti nel piano.</span><span class="sxs-lookup"><span data-stu-id="365e3-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="365e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="365e3-107">EXAMPLES</span></span>

### <span data-ttu-id="365e3-108">--------------------------Esempio 1: ottenere la cronologia degli usi per un piano di impegni specifico--------------------------</span><span class="sxs-lookup"><span data-stu-id="365e3-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="365e3-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="365e3-109">PARAMETERS</span></span>

### <span data-ttu-id="365e3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365e3-110">-DefaultProfile</span></span>
<span data-ttu-id="365e3-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="365e3-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e3-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="365e3-112">-Name</span></span>
<span data-ttu-id="365e3-113">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="365e3-113">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365e3-114">-ResourceGroupName</span></span>
<span data-ttu-id="365e3-115">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="365e3-115">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365e3-116">CommonParameters</span></span>
<span data-ttu-id="365e3-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365e3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365e3-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="365e3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365e3-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="365e3-119">INPUTS</span></span>

### <span data-ttu-id="365e3-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="365e3-120">None</span></span>
<span data-ttu-id="365e3-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="365e3-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="365e3-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="365e3-122">OUTPUTS</span></span>

### <span data-ttu-id="365e3-123">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="365e3-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="365e3-124">Note</span><span class="sxs-lookup"><span data-stu-id="365e3-124">NOTES</span></span>
<span data-ttu-id="365e3-125">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="365e3-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="365e3-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="365e3-126">RELATED LINKS</span></span>

