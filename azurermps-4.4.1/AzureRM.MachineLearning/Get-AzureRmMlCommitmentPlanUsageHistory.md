---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688287"
---
# <span data-ttu-id="890d4-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="890d4-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="890d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="890d4-102">SYNOPSIS</span></span>
<span data-ttu-id="890d4-103">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="890d4-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="890d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="890d4-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="890d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="890d4-105">DESCRIPTION</span></span>
<span data-ttu-id="890d4-106">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato, incluse le risorse utilizzate e le risorse rimanenti nel piano.</span><span class="sxs-lookup"><span data-stu-id="890d4-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="890d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="890d4-107">EXAMPLES</span></span>

### <span data-ttu-id="890d4-108">--------------------------Esempio 1: ottenere la cronologia degli usi per un piano di impegni specifico--------------------------</span><span class="sxs-lookup"><span data-stu-id="890d4-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="890d4-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="890d4-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="890d4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="890d4-110">PARAMETERS</span></span>

### <span data-ttu-id="890d4-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="890d4-111">-Name</span></span>
<span data-ttu-id="890d4-112">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="890d4-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="890d4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="890d4-113">-ResourceGroupName</span></span>
<span data-ttu-id="890d4-114">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="890d4-114">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="890d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890d4-115">-DefaultProfile</span></span>
<span data-ttu-id="890d4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="890d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="890d4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890d4-117">CommonParameters</span></span>
<span data-ttu-id="890d4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890d4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890d4-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="890d4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890d4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="890d4-120">INPUTS</span></span>

## <span data-ttu-id="890d4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="890d4-121">OUTPUTS</span></span>

### <span data-ttu-id="890d4-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="890d4-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="890d4-123">Note</span><span class="sxs-lookup"><span data-stu-id="890d4-123">NOTES</span></span>
<span data-ttu-id="890d4-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="890d4-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="890d4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="890d4-125">RELATED LINKS</span></span>

