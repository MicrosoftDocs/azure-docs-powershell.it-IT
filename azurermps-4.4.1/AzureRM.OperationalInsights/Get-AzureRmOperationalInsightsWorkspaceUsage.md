---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: dfbf5833bd045c40315cb06d2e954688229ac557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516156"
---
# <span data-ttu-id="86f4a-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="86f4a-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="86f4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="86f4a-103">Ottiene i dati sull'utilizzo per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="86f4a-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86f4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86f4a-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86f4a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="86f4a-106">Il cmdlet **Get-AzureRmOperationalInsightsWorkspaceUsage** recupera i dati sull'utilizzo di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="86f4a-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="86f4a-107">Questo spiega la quantità di dati analizzati dall'area di lavoro per un determinato periodo.</span><span class="sxs-lookup"><span data-stu-id="86f4a-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="86f4a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86f4a-108">EXAMPLES</span></span>

### <span data-ttu-id="86f4a-109">Esempio 1: recuperare i dati sull'utilizzo per nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="86f4a-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="86f4a-110">Questo comando consente di ottenere i dettagli di utilizzo per l'area di lavoro denominata area di lavoro nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="86f4a-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="86f4a-111">Esempio 2: ottenere i dati sull'utilizzo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="86f4a-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="86f4a-112">Questo comando ottiene l'area di lavoro denominata Workspace usando il cmdlet Get-AzureRmOperationalInsightsWorkspace e quindi passa l'area di lavoro al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="86f4a-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="86f4a-113">Il comando ottiene i dettagli sull'utilizzo per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="86f4a-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="86f4a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86f4a-114">PARAMETERS</span></span>

### <span data-ttu-id="86f4a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="86f4a-115">-Name</span></span>
<span data-ttu-id="86f4a-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="86f4a-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="86f4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="86f4a-118">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="86f4a-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="86f4a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f4a-119">-DefaultProfile</span></span>
<span data-ttu-id="86f4a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86f4a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f4a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f4a-121">CommonParameters</span></span>
<span data-ttu-id="86f4a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f4a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f4a-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f4a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f4a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86f4a-124">INPUTS</span></span>

## <span data-ttu-id="86f4a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86f4a-125">OUTPUTS</span></span>

### <span data-ttu-id="86f4a-126">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSUsageMetric]</span><span class="sxs-lookup"><span data-stu-id="86f4a-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric]</span></span>

## <span data-ttu-id="86f4a-127">Note</span><span class="sxs-lookup"><span data-stu-id="86f4a-127">NOTES</span></span>

## <span data-ttu-id="86f4a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86f4a-128">RELATED LINKS</span></span>

[<span data-ttu-id="86f4a-129">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="86f4a-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="86f4a-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="86f4a-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


