---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191548"
---
# <span data-ttu-id="fae02-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="fae02-101">Get-AzEventHub</span></span>

## <span data-ttu-id="fae02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fae02-102">SYNOPSIS</span></span>
<span data-ttu-id="fae02-103">Ottiene i dettagli di un singolo hub di eventi o restituisce un elenco di hub eventi.</span><span class="sxs-lookup"><span data-stu-id="fae02-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="fae02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fae02-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae02-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fae02-105">DESCRIPTION</span></span>
<span data-ttu-id="fae02-106">Il cmdlet Get-AzEventHub restituisce i dettagli di un hub eventi o un elenco di tutti gli hub eventi nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="fae02-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="fae02-107">Se viene fornito il nome dell'hub eventi, vengono restituiti i dettagli di un singolo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="fae02-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="fae02-108">Se non viene specificato un nome Hub eventi, viene restituito un elenco di tutti gli hub eventi nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="fae02-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="fae02-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fae02-109">EXAMPLES</span></span>

### <span data-ttu-id="fae02-110">Esempio 1: specificato EventHub</span><span class="sxs-lookup"><span data-stu-id="fae02-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="fae02-111">Restituisce i dettagli dell'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="fae02-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="fae02-112">Esempio 2: elenco di EventHub nello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="fae02-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="fae02-113">Restituisce un elenco di hub eventi nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="fae02-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="fae02-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fae02-114">PARAMETERS</span></span>

### <span data-ttu-id="fae02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae02-115">-DefaultProfile</span></span>
<span data-ttu-id="fae02-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fae02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae02-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fae02-117">-MaxCount</span></span>
<span data-ttu-id="fae02-118">Determinare il numero massimo di EventHubs da restituire.</span><span class="sxs-lookup"><span data-stu-id="fae02-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="fae02-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fae02-119">-Name</span></span>
<span data-ttu-id="fae02-120">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="fae02-120">EventHub Name</span></span>

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

### <span data-ttu-id="fae02-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fae02-121">-Namespace</span></span>
<span data-ttu-id="fae02-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fae02-122">Namespace Name</span></span>

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

### <span data-ttu-id="fae02-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae02-123">-ResourceGroupName</span></span>
<span data-ttu-id="fae02-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="fae02-124">Resource Group Name</span></span>

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

### <span data-ttu-id="fae02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae02-125">CommonParameters</span></span>
<span data-ttu-id="fae02-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae02-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae02-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae02-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fae02-128">INPUTS</span></span>

### <span data-ttu-id="fae02-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fae02-129">System.String</span></span>

## <span data-ttu-id="fae02-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fae02-130">OUTPUTS</span></span>

### <span data-ttu-id="fae02-131">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="fae02-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="fae02-132">Note</span><span class="sxs-lookup"><span data-stu-id="fae02-132">NOTES</span></span>

## <span data-ttu-id="fae02-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fae02-133">RELATED LINKS</span></span>
