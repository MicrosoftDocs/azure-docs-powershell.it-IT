---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 481d1e26ad769101f06acda5573175bd06331fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521850"
---
# <span data-ttu-id="cabbc-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="cabbc-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="cabbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cabbc-102">SYNOPSIS</span></span>
<span data-ttu-id="cabbc-103">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="cabbc-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cabbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cabbc-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cabbc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cabbc-105">DESCRIPTION</span></span>
<span data-ttu-id="cabbc-106">Recupera le informazioni sulla cronologia degli usi per un piano di impegni specificato, incluse le risorse utilizzate e le risorse rimanenti nel piano.</span><span class="sxs-lookup"><span data-stu-id="cabbc-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="cabbc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cabbc-107">EXAMPLES</span></span>

### <span data-ttu-id="cabbc-108">Esempio 1: ottenere la cronologia degli usi per un piano di impegno specifico</span><span class="sxs-lookup"><span data-stu-id="cabbc-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="cabbc-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cabbc-109">PARAMETERS</span></span>

### <span data-ttu-id="cabbc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabbc-110">-DefaultProfile</span></span>
<span data-ttu-id="cabbc-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cabbc-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cabbc-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="cabbc-112">-Name</span></span>
<span data-ttu-id="cabbc-113">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="cabbc-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="cabbc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabbc-114">-ResourceGroupName</span></span>
<span data-ttu-id="cabbc-115">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="cabbc-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="cabbc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabbc-116">CommonParameters</span></span>
<span data-ttu-id="cabbc-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabbc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabbc-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cabbc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabbc-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cabbc-119">INPUTS</span></span>

### <span data-ttu-id="cabbc-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cabbc-120">None</span></span>

## <span data-ttu-id="cabbc-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cabbc-121">OUTPUTS</span></span>

### <span data-ttu-id="cabbc-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="cabbc-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="cabbc-123">Note</span><span class="sxs-lookup"><span data-stu-id="cabbc-123">NOTES</span></span>
<span data-ttu-id="cabbc-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="cabbc-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="cabbc-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cabbc-125">RELATED LINKS</span></span>
