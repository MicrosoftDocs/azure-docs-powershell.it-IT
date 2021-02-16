---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179223"
---
# <span data-ttu-id="eb849-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="eb849-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="eb849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb849-102">SYNOPSIS</span></span>
<span data-ttu-id="eb849-103">Ottiene informazioni su un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eb849-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="eb849-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb849-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb849-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eb849-105">DESCRIPTION</span></span>
<span data-ttu-id="eb849-106">Il cmdlet **Get-AzOperationalInsightsWorkspace** ottiene informazioni su un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="eb849-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="eb849-107">Se si specifica il nome di un'area di lavoro, questo cmdlet ottiene informazioni sull'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eb849-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="eb849-108">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutte le aree di lavoro in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb849-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="eb849-109">Se non si specifica un nome e un gruppo di risorse, questo cmdlet riceve informazioni su tutte le aree di lavoro di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="eb849-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="eb849-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb849-110">EXAMPLES</span></span>

### <span data-ttu-id="eb849-111">Esempio 1: Ottenere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="eb849-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="eb849-112">Questo comando ottiene un'area di lavoro denominata MyWorkspace nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eb849-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="eb849-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb849-113">PARAMETERS</span></span>

### <span data-ttu-id="eb849-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb849-114">-DefaultProfile</span></span>
<span data-ttu-id="eb849-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="eb849-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb849-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eb849-116">-Name</span></span>
<span data-ttu-id="eb849-117">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eb849-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="eb849-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb849-118">-ResourceGroupName</span></span>
<span data-ttu-id="eb849-119">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="eb849-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="eb849-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb849-120">CommonParameters</span></span>
<span data-ttu-id="eb849-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb849-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb849-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb849-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb849-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="eb849-123">INPUTS</span></span>

### <span data-ttu-id="eb849-124">System.String</span><span class="sxs-lookup"><span data-stu-id="eb849-124">System.String</span></span>

## <span data-ttu-id="eb849-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb849-125">OUTPUTS</span></span>

### <span data-ttu-id="eb849-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="eb849-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="eb849-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="eb849-127">NOTES</span></span>

## <span data-ttu-id="eb849-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb849-128">RELATED LINKS</span></span>

[<span data-ttu-id="eb849-129">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="eb849-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


