---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 3be16cd371543848d650711241dbcb8828a5ba32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521031"
---
# <span data-ttu-id="fb16b-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="fb16b-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="fb16b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb16b-102">SYNOPSIS</span></span>
<span data-ttu-id="fb16b-103">Recupera le informazioni di riepilogo per una o più associazioni di impegni.</span><span class="sxs-lookup"><span data-stu-id="fb16b-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb16b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb16b-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb16b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb16b-105">DESCRIPTION</span></span>
<span data-ttu-id="fb16b-106">Recupera le informazioni sull'associazione di impegni.</span><span class="sxs-lookup"><span data-stu-id="fb16b-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="fb16b-107">A seconda dei paramenti passati, il cmdlet restituisce una specifica associazione di impegni o una raccolta di associazioni di impegni per il piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="fb16b-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="fb16b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb16b-108">EXAMPLES</span></span>

### <span data-ttu-id="fb16b-109">--------------------------Esempio 1: ottenere una specifica associazione di impegni--------------------------</span><span class="sxs-lookup"><span data-stu-id="fb16b-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="fb16b-110">--------------------------Esempio 2: ottenere tutte le associazioni di impegni per il piano di impegno specificato--------------------------</span><span class="sxs-lookup"><span data-stu-id="fb16b-110">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="fb16b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb16b-111">PARAMETERS</span></span>

### <span data-ttu-id="fb16b-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="fb16b-112">-CommitmentPlanName</span></span>
<span data-ttu-id="fb16b-113">Il nome del piano di impegni di Azure ML che include una o più associazioni di impegni.</span><span class="sxs-lookup"><span data-stu-id="fb16b-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="fb16b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb16b-114">-DefaultProfile</span></span>
<span data-ttu-id="fb16b-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fb16b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb16b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb16b-116">-Name</span></span>
<span data-ttu-id="fb16b-117">Nome dell'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="fb16b-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb16b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb16b-118">-ResourceGroupName</span></span>
<span data-ttu-id="fb16b-119">Nome del gruppo di risorse per l'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="fb16b-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="fb16b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb16b-120">CommonParameters</span></span>
<span data-ttu-id="fb16b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb16b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb16b-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb16b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb16b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb16b-123">INPUTS</span></span>

### <span data-ttu-id="fb16b-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fb16b-124">None</span></span>
<span data-ttu-id="fb16b-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fb16b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb16b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb16b-126">OUTPUTS</span></span>

### <span data-ttu-id="fb16b-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="fb16b-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="fb16b-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="fb16b-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="fb16b-129">Note</span><span class="sxs-lookup"><span data-stu-id="fb16b-129">NOTES</span></span>
<span data-ttu-id="fb16b-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fb16b-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fb16b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb16b-131">RELATED LINKS</span></span>

