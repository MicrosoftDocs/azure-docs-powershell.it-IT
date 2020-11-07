---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: 662c2b5ed487a13c557e85709ed7b850a28acb2e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674457"
---
# <span data-ttu-id="52b58-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="52b58-101">Get-AzEventHub</span></span>

## <span data-ttu-id="52b58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52b58-102">SYNOPSIS</span></span>
<span data-ttu-id="52b58-103">Ottiene i dettagli di un singolo hub di eventi o restituisce un elenco di hub eventi.</span><span class="sxs-lookup"><span data-stu-id="52b58-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="52b58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52b58-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b58-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52b58-105">DESCRIPTION</span></span>
<span data-ttu-id="52b58-106">Il cmdlet Get-AzEventHub restituisce i dettagli di un hub eventi o un elenco di tutti gli hub eventi nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="52b58-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="52b58-107">Se viene fornito il nome dell'hub eventi, vengono restituiti i dettagli di un singolo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="52b58-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="52b58-108">Se non viene specificato un nome Hub eventi, viene restituito un elenco di tutti gli hub eventi nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="52b58-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="52b58-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52b58-109">EXAMPLES</span></span>

### <span data-ttu-id="52b58-110">Esempio 1-EventHub specificato</span><span class="sxs-lookup"><span data-stu-id="52b58-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="52b58-111">Restituisce i dettagli dell'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="52b58-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="52b58-112">Esempio 2-elenco di EventHub nello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="52b58-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="52b58-113">Restituisce un elenco di hub eventi nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="52b58-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="52b58-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52b58-114">PARAMETERS</span></span>

### <span data-ttu-id="52b58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b58-115">-DefaultProfile</span></span>
<span data-ttu-id="52b58-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52b58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b58-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="52b58-117">-MaxCount</span></span>
<span data-ttu-id="52b58-118">Determinare il numero massimo di EventHubs da restituire.</span><span class="sxs-lookup"><span data-stu-id="52b58-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="52b58-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="52b58-119">-Name</span></span>
<span data-ttu-id="52b58-120">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="52b58-120">EventHub Name</span></span>

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

### <span data-ttu-id="52b58-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52b58-121">-Namespace</span></span>
<span data-ttu-id="52b58-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52b58-122">Namespace Name</span></span>

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

### <span data-ttu-id="52b58-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b58-123">-ResourceGroupName</span></span>
<span data-ttu-id="52b58-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="52b58-124">Resource Group Name</span></span>

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

### <span data-ttu-id="52b58-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b58-125">CommonParameters</span></span>
<span data-ttu-id="52b58-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b58-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b58-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b58-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b58-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52b58-128">INPUTS</span></span>

### <span data-ttu-id="52b58-129">System. String</span><span class="sxs-lookup"><span data-stu-id="52b58-129">System.String</span></span>

## <span data-ttu-id="52b58-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52b58-130">OUTPUTS</span></span>

### <span data-ttu-id="52b58-131">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="52b58-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="52b58-132">Note</span><span class="sxs-lookup"><span data-stu-id="52b58-132">NOTES</span></span>

## <span data-ttu-id="52b58-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52b58-133">RELATED LINKS</span></span>
