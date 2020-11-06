---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacemanagementgroups
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 215e3007de3b3760d974512cdffdd669f32447ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510844"
---
# <span data-ttu-id="95a78-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="95a78-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="95a78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95a78-102">SYNOPSIS</span></span>
<span data-ttu-id="95a78-103">Ottiene i dettagli dei gruppi di gestione connessi a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="95a78-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95a78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95a78-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95a78-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95a78-105">DESCRIPTION</span></span>
<span data-ttu-id="95a78-106">Il cmdlet **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** elenca i gruppi di gestione connessi a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="95a78-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="95a78-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95a78-107">EXAMPLES</span></span>

### <span data-ttu-id="95a78-108">Esempio 1: ottenere i gruppi di gestione per nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="95a78-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="95a78-109">Questo comando consente di ottenere i gruppi di gestione per l'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="95a78-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="95a78-110">Esempio 2: ottenere gruppi di gestione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="95a78-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="95a78-111">Questo comando usa il cmdlet Get-AzureRmOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e quindi passa l'area di lavoro al cmdlet corrente, che ottiene i gruppi di gestione per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="95a78-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="95a78-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95a78-112">PARAMETERS</span></span>

### <span data-ttu-id="95a78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a78-113">-DefaultProfile</span></span>
<span data-ttu-id="95a78-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="95a78-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95a78-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="95a78-115">-Name</span></span>
<span data-ttu-id="95a78-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="95a78-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="95a78-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a78-117">-ResourceGroupName</span></span>
<span data-ttu-id="95a78-118">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="95a78-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="95a78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a78-119">CommonParameters</span></span>
<span data-ttu-id="95a78-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a78-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a78-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a78-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95a78-122">INPUTS</span></span>

### <span data-ttu-id="95a78-123">System. String</span><span class="sxs-lookup"><span data-stu-id="95a78-123">System.String</span></span>

## <span data-ttu-id="95a78-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95a78-124">OUTPUTS</span></span>

### <span data-ttu-id="95a78-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="95a78-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="95a78-126">Note</span><span class="sxs-lookup"><span data-stu-id="95a78-126">NOTES</span></span>

## <span data-ttu-id="95a78-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95a78-127">RELATED LINKS</span></span>

[<span data-ttu-id="95a78-128">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="95a78-128">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="95a78-129">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="95a78-129">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


