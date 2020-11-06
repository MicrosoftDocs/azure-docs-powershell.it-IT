---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521682"
---
# <span data-ttu-id="86909-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="86909-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="86909-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86909-102">SYNOPSIS</span></span>
<span data-ttu-id="86909-103">Ottiene i dettagli di un singolo hub di eventi o restituisce un elenco di hub eventi.</span><span class="sxs-lookup"><span data-stu-id="86909-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86909-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86909-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="86909-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86909-105">DESCRIPTION</span></span>
<span data-ttu-id="86909-106">Il cmdlet Get-AzureRmEventHub restituisce i dettagli di un hub eventi o un elenco di tutti gli hub eventi nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="86909-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="86909-107">Se viene fornito il nome dell'hub eventi, vengono restituiti i dettagli di un singolo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="86909-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="86909-108">Se non viene specificato un nome Hub eventi, viene restituito un elenco di tutti gli hub eventi nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="86909-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="86909-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86909-109">EXAMPLES</span></span>

### <span data-ttu-id="86909-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86909-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="86909-111">Restituisce i dettagli dell'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="86909-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="86909-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="86909-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="86909-113">Restituisce un elenco di hub eventi nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="86909-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="86909-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86909-114">PARAMETERS</span></span>

### <span data-ttu-id="86909-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86909-115">-ResourceGroupName</span></span>
<span data-ttu-id="86909-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86909-116">Resource group name.</span></span>

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

### <span data-ttu-id="86909-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="86909-117">-Name</span></span>
<span data-ttu-id="86909-118">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="86909-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86909-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="86909-119">-Namespace</span></span>
<span data-ttu-id="86909-120">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="86909-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="86909-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86909-121">INPUTS</span></span>

### <span data-ttu-id="86909-122">System. String</span><span class="sxs-lookup"><span data-stu-id="86909-122">System.String</span></span>

## <span data-ttu-id="86909-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86909-123">OUTPUTS</span></span>

### <span data-ttu-id="86909-124">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="86909-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="86909-125">Note</span><span class="sxs-lookup"><span data-stu-id="86909-125">NOTES</span></span>

## <span data-ttu-id="86909-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86909-126">RELATED LINKS</span></span>

