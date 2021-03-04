---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 633881b298059c35a54591bb1ff93d4e93a267d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954717"
---
# <span data-ttu-id="632d3-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="632d3-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="632d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="632d3-102">SYNOPSIS</span></span>
<span data-ttu-id="632d3-103">Recupera i dettagli di un singolo cluster Eventhub o dell'elenco di cluster nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="632d3-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="632d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="632d3-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="632d3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="632d3-105">DESCRIPTION</span></span>
<span data-ttu-id="632d3-106">Elenco Get-AzEventHubClustersAvailableRegion cmdlet di aree geografiche in cui sono disponibili elementi dedicati per la creazione.</span><span class="sxs-lookup"><span data-stu-id="632d3-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="632d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="632d3-107">EXAMPLES</span></span>

### <span data-ttu-id="632d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="632d3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="632d3-109">Viene restituito un elenco di aree geografiche dove</span><span class="sxs-lookup"><span data-stu-id="632d3-109">List of regions is returned where</span></span>

## <span data-ttu-id="632d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="632d3-110">PARAMETERS</span></span>

### <span data-ttu-id="632d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632d3-111">-DefaultProfile</span></span>
<span data-ttu-id="632d3-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="632d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="632d3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632d3-113">CommonParameters</span></span>
<span data-ttu-id="632d3-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="632d3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632d3-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="632d3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632d3-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="632d3-116">INPUTS</span></span>

### <span data-ttu-id="632d3-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="632d3-117">None</span></span>

## <span data-ttu-id="632d3-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="632d3-118">OUTPUTS</span></span>

### <span data-ttu-id="632d3-119">System.Collections.generic.I Paese'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="632d3-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="632d3-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="632d3-120">NOTES</span></span>

## <span data-ttu-id="632d3-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="632d3-121">RELATED LINKS</span></span>
