---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488822"
---
# <span data-ttu-id="4b524-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4b524-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="4b524-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b524-102">SYNOPSIS</span></span>
<span data-ttu-id="4b524-103">Ottiene i dettagli dei gruppi di gestione connessi a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4b524-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="4b524-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b524-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b524-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b524-105">DESCRIPTION</span></span>
<span data-ttu-id="4b524-106">Il cmdlet **Get-AzOperationalInsightsWorkspaceManagementGroup** elenca i gruppi di gestione connessi a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4b524-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="4b524-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b524-107">EXAMPLES</span></span>

### <span data-ttu-id="4b524-108">Esempio 1: ottenere i gruppi di gestione per nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="4b524-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="4b524-109">Questo comando consente di ottenere i gruppi di gestione per l'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4b524-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="4b524-110">Esempio 2: ottenere gruppi di gestione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="4b524-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="4b524-111">Questo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e quindi passa l'area di lavoro al cmdlet corrente, che ottiene i gruppi di gestione per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4b524-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="4b524-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b524-112">PARAMETERS</span></span>

### <span data-ttu-id="4b524-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b524-113">-DefaultProfile</span></span>
<span data-ttu-id="4b524-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4b524-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b524-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b524-115">-Name</span></span>
<span data-ttu-id="4b524-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4b524-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4b524-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b524-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b524-118">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="4b524-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="4b524-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b524-119">CommonParameters</span></span>
<span data-ttu-id="4b524-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b524-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b524-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b524-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b524-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b524-122">INPUTS</span></span>

### <span data-ttu-id="4b524-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4b524-123">System.String</span></span>

## <span data-ttu-id="4b524-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b524-124">OUTPUTS</span></span>

### <span data-ttu-id="4b524-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4b524-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="4b524-126">Note</span><span class="sxs-lookup"><span data-stu-id="4b524-126">NOTES</span></span>

## <span data-ttu-id="4b524-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b524-127">RELATED LINKS</span></span>

[<span data-ttu-id="4b524-128">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="4b524-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="4b524-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4b524-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


