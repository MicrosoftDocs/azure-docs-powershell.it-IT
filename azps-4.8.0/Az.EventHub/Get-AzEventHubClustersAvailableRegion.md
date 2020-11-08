---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192492"
---
# <span data-ttu-id="773fd-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="773fd-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="773fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="773fd-102">SYNOPSIS</span></span>
<span data-ttu-id="773fd-103">Ottiene i dettagli di un singolo cluster Eventhub o dell'elenco di cluster nel gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="773fd-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="773fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="773fd-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="773fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="773fd-105">DESCRIPTION</span></span>
<span data-ttu-id="773fd-106">L'elenco dei cmdlet Get-AzEventHubClustersAvailableRegion delle aree geografiche in cui sono disponibili le specifiche per la creazione.</span><span class="sxs-lookup"><span data-stu-id="773fd-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="773fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="773fd-107">EXAMPLES</span></span>

### <span data-ttu-id="773fd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="773fd-108">Example 1</span></span>
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

<span data-ttu-id="773fd-109">Viene restituito l'elenco delle aree geografiche in cui</span><span class="sxs-lookup"><span data-stu-id="773fd-109">List of regions is returned where</span></span>

## <span data-ttu-id="773fd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="773fd-110">PARAMETERS</span></span>

### <span data-ttu-id="773fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773fd-111">-DefaultProfile</span></span>
<span data-ttu-id="773fd-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="773fd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="773fd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773fd-113">CommonParameters</span></span>
<span data-ttu-id="773fd-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="773fd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773fd-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="773fd-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773fd-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="773fd-116">INPUTS</span></span>

### <span data-ttu-id="773fd-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="773fd-117">None</span></span>

## <span data-ttu-id="773fd-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="773fd-118">OUTPUTS</span></span>

### <span data-ttu-id="773fd-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubsAvailableCluster, Microsoft. Azure. PowerShell. Cmdlets. EventHub, Version = 1.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="773fd-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="773fd-120">Note</span><span class="sxs-lookup"><span data-stu-id="773fd-120">NOTES</span></span>

## <span data-ttu-id="773fd-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="773fd-121">RELATED LINKS</span></span>
