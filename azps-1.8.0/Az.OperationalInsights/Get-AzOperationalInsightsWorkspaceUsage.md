---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 04a62f4929e89dd4bff4d088d84325b0bdbb140b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685394"
---
# <span data-ttu-id="4baf3-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="4baf3-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="4baf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4baf3-102">SYNOPSIS</span></span>
<span data-ttu-id="4baf3-103">Ottiene i dati sull'utilizzo per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4baf3-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="4baf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4baf3-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4baf3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4baf3-105">DESCRIPTION</span></span>
<span data-ttu-id="4baf3-106">Il cmdlet **Get-AzOperationalInsightsWorkspaceUsage** recupera i dati sull'utilizzo di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4baf3-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="4baf3-107">Questo spiega la quantità di dati analizzati dall'area di lavoro per un determinato periodo.</span><span class="sxs-lookup"><span data-stu-id="4baf3-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="4baf3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4baf3-108">EXAMPLES</span></span>

### <span data-ttu-id="4baf3-109">Esempio 1: recuperare i dati sull'utilizzo per nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="4baf3-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="4baf3-110">Questo comando consente di ottenere i dettagli di utilizzo per l'area di lavoro denominata area di lavoro nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4baf3-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="4baf3-111">Esempio 2: ottenere i dati sull'utilizzo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="4baf3-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="4baf3-112">Questo comando ottiene l'area di lavoro denominata Workspace usando il cmdlet Get-AzOperationalInsightsWorkspace e quindi passa l'area di lavoro al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="4baf3-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="4baf3-113">Il comando ottiene i dettagli sull'utilizzo per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4baf3-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="4baf3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4baf3-114">PARAMETERS</span></span>

### <span data-ttu-id="4baf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4baf3-115">-DefaultProfile</span></span>
<span data-ttu-id="4baf3-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4baf3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4baf3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4baf3-117">-Name</span></span>
<span data-ttu-id="4baf3-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4baf3-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4baf3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4baf3-119">-ResourceGroupName</span></span>
<span data-ttu-id="4baf3-120">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="4baf3-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="4baf3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4baf3-121">CommonParameters</span></span>
<span data-ttu-id="4baf3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4baf3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4baf3-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4baf3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4baf3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4baf3-124">INPUTS</span></span>

### <span data-ttu-id="4baf3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4baf3-125">System.String</span></span>

## <span data-ttu-id="4baf3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4baf3-126">OUTPUTS</span></span>

### <span data-ttu-id="4baf3-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="4baf3-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="4baf3-128">Note</span><span class="sxs-lookup"><span data-stu-id="4baf3-128">NOTES</span></span>

## <span data-ttu-id="4baf3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4baf3-129">RELATED LINKS</span></span>

[<span data-ttu-id="4baf3-130">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="4baf3-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="4baf3-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4baf3-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


