---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514340"
---
# <span data-ttu-id="b6e4f-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="b6e4f-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="b6e4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e4f-103">Ottiene i dettagli di un singolo hub di eventi o restituisce un elenco di hub eventi.</span><span class="sxs-lookup"><span data-stu-id="b6e4f-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6e4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6e4f-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6e4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="b6e4f-106">Il cmdlet Get-AzureRmEventHub restituisce i dettagli di un hub eventi o un elenco di tutti gli hub eventi nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="b6e4f-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="b6e4f-107">Se viene fornito il nome dell'hub eventi, vengono restituiti i dettagli di un singolo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="b6e4f-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="b6e4f-108">Se non viene specificato un nome Hub eventi, viene restituito un elenco di tutti gli hub eventi nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="b6e4f-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="b6e4f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6e4f-109">EXAMPLES</span></span>

### <span data-ttu-id="b6e4f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6e4f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="b6e4f-111">Restituisce i dettagli dell'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="b6e4f-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="b6e4f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b6e4f-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="b6e4f-113">Restituisce un elenco di hub eventi nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="b6e4f-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="b6e4f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6e4f-114">PARAMETERS</span></span>

### <span data-ttu-id="b6e4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e4f-115">-DefaultProfile</span></span>
<span data-ttu-id="b6e4f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6e4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e4f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6e4f-117">-Name</span></span>
<span data-ttu-id="b6e4f-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="b6e4f-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e4f-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6e4f-119">-Namespace</span></span>
<span data-ttu-id="b6e4f-120">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6e4f-120">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e4f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e4f-121">-ResourceGroupName</span></span>
<span data-ttu-id="b6e4f-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b6e4f-122">Resource Group Name</span></span>

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

### <span data-ttu-id="b6e4f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e4f-123">CommonParameters</span></span>
<span data-ttu-id="b6e4f-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e4f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b6e4f-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6e4f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e4f-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6e4f-126">INPUTS</span></span>

### <span data-ttu-id="b6e4f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b6e4f-127">System.String</span></span>


## <span data-ttu-id="b6e4f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6e4f-128">OUTPUTS</span></span>

### <span data-ttu-id="b6e4f-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b6e4f-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="b6e4f-130">Note</span><span class="sxs-lookup"><span data-stu-id="b6e4f-130">NOTES</span></span>

## <span data-ttu-id="b6e4f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6e4f-131">RELATED LINKS</span></span>
