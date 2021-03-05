---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: b5b14cbf816a7872abf431f787f9e3102006901c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003278"
---
# <span data-ttu-id="d105c-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="d105c-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="d105c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d105c-102">SYNOPSIS</span></span>
<span data-ttu-id="d105c-103">Recupera i dati di utilizzo per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d105c-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="d105c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d105c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d105c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d105c-105">DESCRIPTION</span></span>
<span data-ttu-id="d105c-106">Il cmdlet **Get-AzOperationalInsightsWorkspaceUsage** recupera i dati di utilizzo per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d105c-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="d105c-107">In questo modo viene esponga la quantità di dati analizzati dall'area di lavoro in un determinato periodo.</span><span class="sxs-lookup"><span data-stu-id="d105c-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="d105c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d105c-108">EXAMPLES</span></span>

### <span data-ttu-id="d105c-109">Esempio 1: Recuperare i dati di utilizzo in base al nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="d105c-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="d105c-110">Questo comando recupera i dettagli sull'utilizzo dell'area di lavoro denominata MyWorkspace nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="d105c-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="d105c-111">Esempio 2: Ottenere i dati di utilizzo usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="d105c-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="d105c-112">Questo comando recupera l'area di lavoro denominata MyWorkSpace usando il cmdlet Get-AzOperationalInsightsWorkspace e quindi passa l'area di lavoro al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="d105c-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="d105c-113">Il comando recupera i dettagli di utilizzo per quell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d105c-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="d105c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d105c-114">PARAMETERS</span></span>

### <span data-ttu-id="d105c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d105c-115">-DefaultProfile</span></span>
<span data-ttu-id="d105c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d105c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d105c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d105c-117">-Name</span></span>
<span data-ttu-id="d105c-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d105c-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="d105c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d105c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d105c-120">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="d105c-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="d105c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d105c-121">CommonParameters</span></span>
<span data-ttu-id="d105c-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d105c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d105c-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d105c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d105c-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="d105c-124">INPUTS</span></span>

### <span data-ttu-id="d105c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d105c-125">System.String</span></span>

## <span data-ttu-id="d105c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d105c-126">OUTPUTS</span></span>

### <span data-ttu-id="d105c-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="d105c-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="d105c-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="d105c-128">NOTES</span></span>

## <span data-ttu-id="d105c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d105c-129">RELATED LINKS</span></span>

[<span data-ttu-id="d105c-130">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="d105c-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="d105c-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d105c-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


