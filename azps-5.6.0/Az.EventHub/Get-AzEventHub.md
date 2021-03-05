---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: d69e30ff993d2e07c7711d36d8e5ec889bc0f7c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007902"
---
# <span data-ttu-id="e7230-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="e7230-101">Get-AzEventHub</span></span>

## <span data-ttu-id="e7230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7230-102">SYNOPSIS</span></span>
<span data-ttu-id="e7230-103">Ottiene i dettagli di un singolo hub eventi o un elenco di hub eventi.</span><span class="sxs-lookup"><span data-stu-id="e7230-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="e7230-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7230-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7230-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e7230-105">DESCRIPTION</span></span>
<span data-ttu-id="e7230-106">Il Get-AzEventHub cmdlet restituisce i dettagli di un hub eventi o un elenco di tutti gli hub eventi nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="e7230-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="e7230-107">Se viene fornito il nome dell'hub eventi, vengono restituiti i dettagli di un singolo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="e7230-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="e7230-108">Se non viene fornito il nome di un hub eventi, viene restituito un elenco di tutti gli hub eventi nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="e7230-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="e7230-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7230-109">EXAMPLES</span></span>

### <span data-ttu-id="e7230-110">Esempio 1: eventhub specificato</span><span class="sxs-lookup"><span data-stu-id="e7230-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="e7230-111">Restituisce i dettagli dell'hub eventi \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="e7230-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="e7230-112">Esempio 2: Elenco di EventHub nello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="e7230-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="e7230-113">Restituisce un elenco di hub eventi nello spazio dei nomi \` \` MyHostName.</span><span class="sxs-lookup"><span data-stu-id="e7230-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="e7230-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7230-114">PARAMETERS</span></span>

### <span data-ttu-id="e7230-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7230-115">-DefaultProfile</span></span>
<span data-ttu-id="e7230-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7230-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7230-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e7230-117">-MaxCount</span></span>
<span data-ttu-id="e7230-118">Determinare il numero massimo di EventHub da restituire.</span><span class="sxs-lookup"><span data-stu-id="e7230-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7230-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e7230-119">-Name</span></span>
<span data-ttu-id="e7230-120">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="e7230-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7230-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e7230-121">-Namespace</span></span>
<span data-ttu-id="e7230-122">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e7230-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7230-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7230-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7230-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e7230-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e7230-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7230-125">CommonParameters</span></span>
<span data-ttu-id="e7230-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7230-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7230-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7230-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7230-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="e7230-128">INPUTS</span></span>

### <span data-ttu-id="e7230-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e7230-129">System.String</span></span>

## <span data-ttu-id="e7230-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7230-130">OUTPUTS</span></span>

### <span data-ttu-id="e7230-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e7230-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="e7230-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="e7230-132">NOTES</span></span>

## <span data-ttu-id="e7230-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7230-133">RELATED LINKS</span></span>
