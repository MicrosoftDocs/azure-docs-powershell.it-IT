---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 0e63b6926f635a4260e6e3c9d658afa410f29966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512463"
---
# <span data-ttu-id="909aa-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="909aa-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="909aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="909aa-102">SYNOPSIS</span></span>
<span data-ttu-id="909aa-103">Ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="909aa-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="909aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="909aa-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="909aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="909aa-105">DESCRIPTION</span></span>
<span data-ttu-id="909aa-106">Il cmdlet **Get-AzureRmOperationalInsightsIntelligencePacks** ottiene i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="909aa-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="909aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="909aa-107">EXAMPLES</span></span>

### <span data-ttu-id="909aa-108">Esempio 1: ottenere i pacchetti di intelligence</span><span class="sxs-lookup"><span data-stu-id="909aa-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="909aa-109">Questo comando consente di ottenere i pacchetti di intelligence disponibili.</span><span class="sxs-lookup"><span data-stu-id="909aa-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="909aa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="909aa-110">PARAMETERS</span></span>

### <span data-ttu-id="909aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="909aa-111">-DefaultProfile</span></span>
<span data-ttu-id="909aa-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="909aa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909aa-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="909aa-113">-ResourceGroupName</span></span>
<span data-ttu-id="909aa-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="909aa-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909aa-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="909aa-115">-WorkspaceName</span></span>
<span data-ttu-id="909aa-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="909aa-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909aa-117">CommonParameters</span></span>
<span data-ttu-id="909aa-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="909aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909aa-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="909aa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909aa-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="909aa-120">INPUTS</span></span>

### <span data-ttu-id="909aa-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="909aa-121">None</span></span>
<span data-ttu-id="909aa-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="909aa-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="909aa-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="909aa-123">OUTPUTS</span></span>

### <span data-ttu-id="909aa-124">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="909aa-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="909aa-125">Note</span><span class="sxs-lookup"><span data-stu-id="909aa-125">NOTES</span></span>

## <span data-ttu-id="909aa-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="909aa-126">RELATED LINKS</span></span>

[<span data-ttu-id="909aa-127">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="909aa-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


