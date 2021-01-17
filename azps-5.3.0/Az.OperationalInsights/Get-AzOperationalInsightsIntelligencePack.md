---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488829"
---
# <span data-ttu-id="aa784-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="aa784-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="aa784-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa784-102">SYNOPSIS</span></span>
<span data-ttu-id="aa784-103">Ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="aa784-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="aa784-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa784-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa784-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa784-105">DESCRIPTION</span></span>
<span data-ttu-id="aa784-106">Il cmdlet **Get-AzOperationalInsightsIntelligencePack** ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="aa784-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="aa784-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa784-107">EXAMPLES</span></span>

### <span data-ttu-id="aa784-108">Esempio 1: ottenere i pacchetti di intelligence</span><span class="sxs-lookup"><span data-stu-id="aa784-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="aa784-109">Questo comando consente di ottenere i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="aa784-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="aa784-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa784-110">PARAMETERS</span></span>

### <span data-ttu-id="aa784-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa784-111">-DefaultProfile</span></span>
<span data-ttu-id="aa784-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="aa784-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa784-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa784-113">-ResourceGroupName</span></span>
<span data-ttu-id="aa784-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aa784-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="aa784-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aa784-115">-WorkspaceName</span></span>
<span data-ttu-id="aa784-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aa784-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa784-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa784-117">CommonParameters</span></span>
<span data-ttu-id="aa784-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa784-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa784-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa784-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa784-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa784-120">INPUTS</span></span>

### <span data-ttu-id="aa784-121">System. String</span><span class="sxs-lookup"><span data-stu-id="aa784-121">System.String</span></span>

## <span data-ttu-id="aa784-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa784-122">OUTPUTS</span></span>

### <span data-ttu-id="aa784-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="aa784-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="aa784-124">Note</span><span class="sxs-lookup"><span data-stu-id="aa784-124">NOTES</span></span>

## <span data-ttu-id="aa784-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa784-125">RELATED LINKS</span></span>

[<span data-ttu-id="aa784-126">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="aa784-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


