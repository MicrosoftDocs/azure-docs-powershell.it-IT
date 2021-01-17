---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386060"
---
# <span data-ttu-id="d55e3-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="d55e3-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="d55e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d55e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d55e3-103">Recupera le informazioni di riepilogo per una o più associazioni di impegni.</span><span class="sxs-lookup"><span data-stu-id="d55e3-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="d55e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d55e3-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d55e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d55e3-105">DESCRIPTION</span></span>
<span data-ttu-id="d55e3-106">Recupera le informazioni sull'associazione di impegni.</span><span class="sxs-lookup"><span data-stu-id="d55e3-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="d55e3-107">A seconda dei parametri passati, il cmdlet restituisce una specifica associazione di impegni o una raccolta di associazioni di impegni per il piano di impegni specificato.</span><span class="sxs-lookup"><span data-stu-id="d55e3-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="d55e3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d55e3-108">EXAMPLES</span></span>

### <span data-ttu-id="d55e3-109">Esempio 1: ottenere una specifica associazione di impegni</span><span class="sxs-lookup"><span data-stu-id="d55e3-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="d55e3-110">Esempio 2: ottenere tutte le associazioni di impegno per il piano di impegno specificato</span><span class="sxs-lookup"><span data-stu-id="d55e3-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="d55e3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d55e3-111">PARAMETERS</span></span>

### <span data-ttu-id="d55e3-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="d55e3-112">-CommitmentPlanName</span></span>
<span data-ttu-id="d55e3-113">Il nome del piano di impegni di Azure ML che include una o più associazioni di impegni.</span><span class="sxs-lookup"><span data-stu-id="d55e3-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="d55e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55e3-114">-DefaultProfile</span></span>
<span data-ttu-id="d55e3-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d55e3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d55e3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d55e3-116">-Name</span></span>
<span data-ttu-id="d55e3-117">Nome dell'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d55e3-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="d55e3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d55e3-118">-ResourceGroupName</span></span>
<span data-ttu-id="d55e3-119">Nome del gruppo di risorse per l'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d55e3-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="d55e3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55e3-120">CommonParameters</span></span>
<span data-ttu-id="d55e3-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55e3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55e3-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d55e3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55e3-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d55e3-123">INPUTS</span></span>

### <span data-ttu-id="d55e3-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d55e3-124">None</span></span>

## <span data-ttu-id="d55e3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d55e3-125">OUTPUTS</span></span>

### <span data-ttu-id="d55e3-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d55e3-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="d55e3-127">Note</span><span class="sxs-lookup"><span data-stu-id="d55e3-127">NOTES</span></span>
<span data-ttu-id="d55e3-128">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d55e3-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d55e3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d55e3-129">RELATED LINKS</span></span>
