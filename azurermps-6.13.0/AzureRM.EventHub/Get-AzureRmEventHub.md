---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: 6ae26d1d5061989ac93756812cf48494e9101978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686404"
---
# <span data-ttu-id="11409-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="11409-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="11409-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11409-102">SYNOPSIS</span></span>
<span data-ttu-id="11409-103">Ottiene i dettagli di un singolo hub di eventi o restituisce un elenco di hub eventi.</span><span class="sxs-lookup"><span data-stu-id="11409-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11409-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11409-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11409-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11409-105">DESCRIPTION</span></span>
<span data-ttu-id="11409-106">Il cmdlet Get-AzureRmEventHub restituisce i dettagli di un hub eventi o un elenco di tutti gli hub eventi nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="11409-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="11409-107">Se viene fornito il nome dell'hub eventi, vengono restituiti i dettagli di un singolo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="11409-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="11409-108">Se non viene specificato un nome Hub eventi, viene restituito un elenco di tutti gli hub eventi nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="11409-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="11409-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11409-109">EXAMPLES</span></span>

### <span data-ttu-id="11409-110">Esempio 1-EventHub specificato</span><span class="sxs-lookup"><span data-stu-id="11409-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="11409-111">Restituisce i dettagli dell'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="11409-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="11409-112">Esempio 2-elenco di EventHub nello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="11409-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="11409-113">Restituisce un elenco di hub eventi nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="11409-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="11409-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11409-114">PARAMETERS</span></span>

### <span data-ttu-id="11409-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11409-115">-DefaultProfile</span></span>
<span data-ttu-id="11409-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11409-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11409-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="11409-117">-MaxCount</span></span>
<span data-ttu-id="11409-118">Determinare il numero massimo di EventHubs da restituire.</span><span class="sxs-lookup"><span data-stu-id="11409-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="11409-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="11409-119">-Name</span></span>
<span data-ttu-id="11409-120">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="11409-120">EventHub Name</span></span>

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

### <span data-ttu-id="11409-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="11409-121">-Namespace</span></span>
<span data-ttu-id="11409-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="11409-122">Namespace Name</span></span>

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

### <span data-ttu-id="11409-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11409-123">-ResourceGroupName</span></span>
<span data-ttu-id="11409-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="11409-124">Resource Group Name</span></span>

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

### <span data-ttu-id="11409-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11409-125">CommonParameters</span></span>
<span data-ttu-id="11409-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11409-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11409-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11409-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11409-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11409-128">INPUTS</span></span>

### <span data-ttu-id="11409-129">System. String</span><span class="sxs-lookup"><span data-stu-id="11409-129">System.String</span></span>

## <span data-ttu-id="11409-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11409-130">OUTPUTS</span></span>

### <span data-ttu-id="11409-131">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="11409-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="11409-132">Note</span><span class="sxs-lookup"><span data-stu-id="11409-132">NOTES</span></span>

## <span data-ttu-id="11409-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11409-133">RELATED LINKS</span></span>
