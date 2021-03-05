---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 4082e7fc36228953ea33f8f3252bab642ca50e2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001006"
---
# <span data-ttu-id="8f266-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f266-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="8f266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f266-102">SYNOPSIS</span></span>
<span data-ttu-id="8f266-103">Ottiene informazioni su un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8f266-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="8f266-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f266-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f266-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8f266-105">DESCRIPTION</span></span>
<span data-ttu-id="8f266-106">Il cmdlet **Get-AzOperationalInsightsWorkspace** ottiene informazioni su un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="8f266-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="8f266-107">Se si specifica il nome di un'area di lavoro, questo cmdlet ottiene informazioni sull'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8f266-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="8f266-108">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutte le aree di lavoro in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f266-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="8f266-109">Se non si specifica un nome e un gruppo di risorse, questo cmdlet riceve informazioni su tutte le aree di lavoro di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8f266-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="8f266-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f266-110">EXAMPLES</span></span>

### <span data-ttu-id="8f266-111">Esempio 1: Ottenere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="8f266-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="8f266-112">Questo comando ottiene un'area di lavoro denominata MyWorkspace nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8f266-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="8f266-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f266-113">PARAMETERS</span></span>

### <span data-ttu-id="8f266-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f266-114">-DefaultProfile</span></span>
<span data-ttu-id="8f266-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8f266-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f266-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8f266-116">-Name</span></span>
<span data-ttu-id="8f266-117">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8f266-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f266-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f266-118">-ResourceGroupName</span></span>
<span data-ttu-id="8f266-119">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="8f266-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f266-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f266-120">CommonParameters</span></span>
<span data-ttu-id="8f266-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f266-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f266-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f266-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f266-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="8f266-123">INPUTS</span></span>

### <span data-ttu-id="8f266-124">System.String</span><span class="sxs-lookup"><span data-stu-id="8f266-124">System.String</span></span>

## <span data-ttu-id="8f266-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f266-125">OUTPUTS</span></span>

### <span data-ttu-id="8f266-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f266-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="8f266-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="8f266-127">NOTES</span></span>

## <span data-ttu-id="8f266-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f266-128">RELATED LINKS</span></span>

[<span data-ttu-id="8f266-129">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="8f266-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


