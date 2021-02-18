---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202358"
---
# <span data-ttu-id="e6b6e-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="e6b6e-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="e6b6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b6e-103">Recupera i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="e6b6e-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="e6b6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6b6e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b6e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b6e-106">Il cmdlet **Get-AzOperationalInsightsIntelligencePack** ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="e6b6e-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="e6b6e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6b6e-107">EXAMPLES</span></span>

### <span data-ttu-id="e6b6e-108">Esempio 1: Ottenere i pacchetti di intelligence</span><span class="sxs-lookup"><span data-stu-id="e6b6e-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="e6b6e-109">Questo comando recupera i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="e6b6e-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="e6b6e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6b6e-110">PARAMETERS</span></span>

### <span data-ttu-id="e6b6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b6e-111">-DefaultProfile</span></span>
<span data-ttu-id="e6b6e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e6b6e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6b6e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b6e-113">-ResourceGroupName</span></span>
<span data-ttu-id="e6b6e-114">Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e6b6e-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="e6b6e-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6b6e-115">-WorkspaceName</span></span>
<span data-ttu-id="e6b6e-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e6b6e-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e6b6e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b6e-117">CommonParameters</span></span>
<span data-ttu-id="e6b6e-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b6e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b6e-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b6e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b6e-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6b6e-120">INPUTS</span></span>

### <span data-ttu-id="e6b6e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e6b6e-121">System.String</span></span>

## <span data-ttu-id="e6b6e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6b6e-122">OUTPUTS</span></span>

### <span data-ttu-id="e6b6e-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="e6b6e-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="e6b6e-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6b6e-124">NOTES</span></span>

## <span data-ttu-id="e6b6e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6b6e-125">RELATED LINKS</span></span>

[<span data-ttu-id="e6b6e-126">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="e6b6e-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


