---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 9d58d8385d3f1d02e3bd823f43403d7dcdacf4a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012942"
---
# <span data-ttu-id="f592f-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="f592f-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="f592f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f592f-102">SYNOPSIS</span></span>
<span data-ttu-id="f592f-103">Recupera le informazioni di riepilogo per una o più associazioni di impegno.</span><span class="sxs-lookup"><span data-stu-id="f592f-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="f592f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f592f-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f592f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f592f-105">DESCRIPTION</span></span>
<span data-ttu-id="f592f-106">Recupera le informazioni sull'associazione dell'impegno.</span><span class="sxs-lookup"><span data-stu-id="f592f-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="f592f-107">A seconda dei parametri passati, il cmdlet restituisce un'associazione di impegno specifica o una raccolta di associazioni di impegno per il piano di impegno specificato.</span><span class="sxs-lookup"><span data-stu-id="f592f-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="f592f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f592f-108">EXAMPLES</span></span>

### <span data-ttu-id="f592f-109">Esempio 1: Ottenere un'associazione con un impegno specifico</span><span class="sxs-lookup"><span data-stu-id="f592f-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="f592f-110">Esempio 2: Ottenere tutte le associazioni di impegno per il piano di impegno specificato</span><span class="sxs-lookup"><span data-stu-id="f592f-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="f592f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f592f-111">PARAMETERS</span></span>

### <span data-ttu-id="f592f-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="f592f-112">-CommitmentPlanName</span></span>
<span data-ttu-id="f592f-113">Nome del piano di impegno di Azure ML con una o più associazioni di impegno.</span><span class="sxs-lookup"><span data-stu-id="f592f-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="f592f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f592f-114">-DefaultProfile</span></span>
<span data-ttu-id="f592f-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f592f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f592f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f592f-116">-Name</span></span>
<span data-ttu-id="f592f-117">Nome dell'associazione di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f592f-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="f592f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f592f-118">-ResourceGroupName</span></span>
<span data-ttu-id="f592f-119">Nome del gruppo di risorse per l'associazione di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f592f-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="f592f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f592f-120">CommonParameters</span></span>
<span data-ttu-id="f592f-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f592f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f592f-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f592f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f592f-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="f592f-123">INPUTS</span></span>

### <span data-ttu-id="f592f-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f592f-124">None</span></span>

## <span data-ttu-id="f592f-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f592f-125">OUTPUTS</span></span>

### <span data-ttu-id="f592f-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f592f-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f592f-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="f592f-127">NOTES</span></span>
<span data-ttu-id="f592f-128">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="f592f-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f592f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f592f-129">RELATED LINKS</span></span>
