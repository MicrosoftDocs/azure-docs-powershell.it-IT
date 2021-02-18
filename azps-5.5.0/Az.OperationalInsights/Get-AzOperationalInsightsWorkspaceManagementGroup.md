---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206363"
---
# <span data-ttu-id="aeebd-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="aeebd-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="aeebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeebd-102">SYNOPSIS</span></span>
<span data-ttu-id="aeebd-103">Recupera i dettagli dei gruppi di gestione connessi a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aeebd-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="aeebd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aeebd-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeebd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aeebd-105">DESCRIPTION</span></span>
<span data-ttu-id="aeebd-106">Il cmdlet **Get-AzOperationalInsightsWorkspaceManagementGroup** elenca i gruppi di gestione connessi a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aeebd-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="aeebd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aeebd-107">EXAMPLES</span></span>

### <span data-ttu-id="aeebd-108">Esempio 1: Ottenere i gruppi di gestione in base al nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="aeebd-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="aeebd-109">Questo comando recupera i gruppi di gestione per l'area di lavoro denominata MyWorkspace nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aeebd-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="aeebd-110">Esempio 2: Ottenere gruppi di gestione con la pipeline</span><span class="sxs-lookup"><span data-stu-id="aeebd-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="aeebd-111">Questo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata MyWorkspace e quindi passa l'area di lavoro al cmdlet corrente, che recupera i gruppi di gestione per quell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aeebd-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="aeebd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeebd-112">PARAMETERS</span></span>

### <span data-ttu-id="aeebd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeebd-113">-DefaultProfile</span></span>
<span data-ttu-id="aeebd-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="aeebd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeebd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="aeebd-115">-Name</span></span>
<span data-ttu-id="aeebd-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aeebd-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeebd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeebd-117">-ResourceGroupName</span></span>
<span data-ttu-id="aeebd-118">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="aeebd-118">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeebd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeebd-119">CommonParameters</span></span>
<span data-ttu-id="aeebd-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeebd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeebd-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeebd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeebd-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="aeebd-122">INPUTS</span></span>

### <span data-ttu-id="aeebd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="aeebd-123">System.String</span></span>

## <span data-ttu-id="aeebd-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aeebd-124">OUTPUTS</span></span>

### <span data-ttu-id="aeebd-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="aeebd-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="aeebd-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="aeebd-126">NOTES</span></span>

## <span data-ttu-id="aeebd-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aeebd-127">RELATED LINKS</span></span>

[<span data-ttu-id="aeebd-128">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="aeebd-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="aeebd-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="aeebd-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


