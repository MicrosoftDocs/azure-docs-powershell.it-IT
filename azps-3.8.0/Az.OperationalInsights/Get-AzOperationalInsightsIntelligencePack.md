---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: b628f0050ab0aa4b16864b510f4426b940226ec5
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030735"
---
# <span data-ttu-id="d0e69-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="d0e69-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="d0e69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0e69-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e69-103">Ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="d0e69-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="d0e69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0e69-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0e69-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0e69-105">DESCRIPTION</span></span>
<span data-ttu-id="d0e69-106">Il cmdlet **Get-AzOperationalInsightsIntelligencePack** ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="d0e69-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="d0e69-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0e69-107">EXAMPLES</span></span>

### <span data-ttu-id="d0e69-108">Esempio 1: ottenere i pacchetti di intelligence</span><span class="sxs-lookup"><span data-stu-id="d0e69-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="d0e69-109">Questo comando consente di ottenere i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="d0e69-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="d0e69-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0e69-110">PARAMETERS</span></span>

### <span data-ttu-id="d0e69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e69-111">-DefaultProfile</span></span>
<span data-ttu-id="d0e69-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d0e69-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0e69-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e69-113">-ResourceGroupName</span></span>
<span data-ttu-id="d0e69-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d0e69-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d0e69-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d0e69-115">-WorkspaceName</span></span>
<span data-ttu-id="d0e69-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d0e69-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="d0e69-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e69-117">CommonParameters</span></span>
<span data-ttu-id="d0e69-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e69-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e69-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e69-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e69-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0e69-120">INPUTS</span></span>

### <span data-ttu-id="d0e69-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d0e69-121">System.String</span></span>

## <span data-ttu-id="d0e69-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0e69-122">OUTPUTS</span></span>

### <span data-ttu-id="d0e69-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="d0e69-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="d0e69-124">Note</span><span class="sxs-lookup"><span data-stu-id="d0e69-124">NOTES</span></span>

## <span data-ttu-id="d0e69-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0e69-125">RELATED LINKS</span></span>

[<span data-ttu-id="d0e69-126">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="d0e69-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


