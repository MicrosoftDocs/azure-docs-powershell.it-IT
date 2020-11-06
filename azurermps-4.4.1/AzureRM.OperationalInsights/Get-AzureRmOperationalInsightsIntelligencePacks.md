---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 56bc2dd74f17daa9a56eac8ebd5128e6f074fe13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513135"
---
# <span data-ttu-id="310f7-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="310f7-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="310f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="310f7-102">SYNOPSIS</span></span>
<span data-ttu-id="310f7-103">Ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="310f7-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="310f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="310f7-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="310f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="310f7-105">DESCRIPTION</span></span>
<span data-ttu-id="310f7-106">Il cmdlet **Get-AzureRmOperationalInsightsIntelligencePacks** ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="310f7-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="310f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="310f7-107">EXAMPLES</span></span>

### <span data-ttu-id="310f7-108">Esempio 1: ottenere i pacchetti di intelligence</span><span class="sxs-lookup"><span data-stu-id="310f7-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="310f7-109">Questo comando consente di ottenere i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="310f7-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="310f7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="310f7-110">PARAMETERS</span></span>

### <span data-ttu-id="310f7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310f7-111">-ResourceGroupName</span></span>
<span data-ttu-id="310f7-112">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="310f7-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="310f7-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="310f7-113">-WorkspaceName</span></span>
<span data-ttu-id="310f7-114">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="310f7-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="310f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310f7-115">-DefaultProfile</span></span>
<span data-ttu-id="310f7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="310f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="310f7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310f7-117">CommonParameters</span></span>
<span data-ttu-id="310f7-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="310f7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310f7-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310f7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310f7-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="310f7-120">INPUTS</span></span>

## <span data-ttu-id="310f7-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="310f7-121">OUTPUTS</span></span>

### <span data-ttu-id="310f7-122">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="310f7-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="310f7-123">Note</span><span class="sxs-lookup"><span data-stu-id="310f7-123">NOTES</span></span>

## <span data-ttu-id="310f7-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="310f7-124">RELATED LINKS</span></span>

[<span data-ttu-id="310f7-125">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="310f7-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


