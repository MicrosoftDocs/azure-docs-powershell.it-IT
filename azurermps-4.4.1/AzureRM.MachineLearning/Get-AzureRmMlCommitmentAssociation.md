---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 63c0184b9104b939073c4d58313777e8940d0f93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519164"
---
# <span data-ttu-id="5593e-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="5593e-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="5593e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5593e-102">SYNOPSIS</span></span>
<span data-ttu-id="5593e-103">Recupera le informazioni di riepilogo per una o più associazioni di impegni.</span><span class="sxs-lookup"><span data-stu-id="5593e-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5593e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5593e-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5593e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5593e-105">DESCRIPTION</span></span>
<span data-ttu-id="5593e-106">Recupera le informazioni sull'associazione di impegni.</span><span class="sxs-lookup"><span data-stu-id="5593e-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="5593e-107">A seconda dei paramenti passati, il cmdlet restituisce una specifica associazione di impegni o una raccolta di associazioni di impegni per il piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="5593e-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="5593e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5593e-108">EXAMPLES</span></span>

### <span data-ttu-id="5593e-109">--------------------------Esempio 1: ottenere una specifica associazione di impegni--------------------------</span><span class="sxs-lookup"><span data-stu-id="5593e-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
<span data-ttu-id="5593e-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5593e-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="5593e-111">--------------------------Esempio 2: ottenere tutte le associazioni di impegni per il piano di impegno specificato--------------------------</span><span class="sxs-lookup"><span data-stu-id="5593e-111">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
<span data-ttu-id="5593e-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5593e-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="5593e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5593e-113">PARAMETERS</span></span>

### <span data-ttu-id="5593e-114">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="5593e-114">-CommitmentPlanName</span></span>
<span data-ttu-id="5593e-115">Il nome del piano di impegni di Azure ML che include una o più associazioni di impegni.</span><span class="sxs-lookup"><span data-stu-id="5593e-115">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="5593e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5593e-116">-Name</span></span>
<span data-ttu-id="5593e-117">Nome dell'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5593e-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="5593e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5593e-118">-ResourceGroupName</span></span>
<span data-ttu-id="5593e-119">Nome del gruppo di risorse per l'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5593e-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="5593e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5593e-120">-DefaultProfile</span></span>
<span data-ttu-id="5593e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5593e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5593e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5593e-122">CommonParameters</span></span>
<span data-ttu-id="5593e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5593e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5593e-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5593e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5593e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5593e-125">INPUTS</span></span>

## <span data-ttu-id="5593e-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5593e-126">OUTPUTS</span></span>

### <span data-ttu-id="5593e-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5593e-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="5593e-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="5593e-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="5593e-129">Note</span><span class="sxs-lookup"><span data-stu-id="5593e-129">NOTES</span></span>
<span data-ttu-id="5593e-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5593e-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5593e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5593e-131">RELATED LINKS</span></span>

