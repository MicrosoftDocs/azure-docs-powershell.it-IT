---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519965"
---
# <span data-ttu-id="89e36-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="89e36-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="89e36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89e36-102">SYNOPSIS</span></span>
<span data-ttu-id="89e36-103">Ottiene le stringhe di connessione primarie e secondarie per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="89e36-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89e36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89e36-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89e36-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89e36-105">DESCRIPTION</span></span>
<span data-ttu-id="89e36-106">Il cmdlet **Get-AzureRmServiceBusQueueKey** restituisce le stringhe di connessione primarie e secondarie per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="89e36-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="89e36-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89e36-107">EXAMPLES</span></span>

### <span data-ttu-id="89e36-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="89e36-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="89e36-109">Restituisce le stringhe di connessione primarie e secondarie per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="89e36-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="89e36-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89e36-110">PARAMETERS</span></span>

### <span data-ttu-id="89e36-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89e36-111">-ResourceGroup</span></span>
<span data-ttu-id="89e36-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89e36-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="89e36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e36-113">-DefaultProfile</span></span>
<span data-ttu-id="89e36-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89e36-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e36-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="89e36-115">-Name</span></span>
<span data-ttu-id="89e36-116">Nome AuthorizationRule coda di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="89e36-116">ServiceBus Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e36-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89e36-117">-Namespace</span></span>
<span data-ttu-id="89e36-118">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="89e36-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e36-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="89e36-119">-Queue</span></span>
<span data-ttu-id="89e36-120">Nome coda di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="89e36-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e36-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e36-121">CommonParameters</span></span>
<span data-ttu-id="89e36-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e36-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e36-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e36-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e36-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89e36-124">INPUTS</span></span>

### <span data-ttu-id="89e36-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89e36-125">-ResourceGroup</span></span>
 <span data-ttu-id="89e36-126">System. String</span><span class="sxs-lookup"><span data-stu-id="89e36-126">System.String</span></span>
 

### <span data-ttu-id="89e36-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="89e36-127">-NamespaceName</span></span>
 <span data-ttu-id="89e36-128">System. String</span><span class="sxs-lookup"><span data-stu-id="89e36-128">System.String</span></span>
 

### <span data-ttu-id="89e36-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="89e36-129">-QueueName</span></span>
 <span data-ttu-id="89e36-130">System. String</span><span class="sxs-lookup"><span data-stu-id="89e36-130">System.String</span></span>
 

### <span data-ttu-id="89e36-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="89e36-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="89e36-132">System. String</span><span class="sxs-lookup"><span data-stu-id="89e36-132">System.String</span></span>

## <span data-ttu-id="89e36-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89e36-133">OUTPUTS</span></span>

### <span data-ttu-id="89e36-134">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="89e36-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="89e36-135">PrimaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-valore}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-valore}; EntityPath = SB-Queue_e xampl1 PrimaryKey: {PrimaryKey value} SecondaryKey: {SecondaryKey value} nome di pagina: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="89e36-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="89e36-136">Note</span><span class="sxs-lookup"><span data-stu-id="89e36-136">NOTES</span></span>

## <span data-ttu-id="89e36-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89e36-137">RELATED LINKS</span></span>

