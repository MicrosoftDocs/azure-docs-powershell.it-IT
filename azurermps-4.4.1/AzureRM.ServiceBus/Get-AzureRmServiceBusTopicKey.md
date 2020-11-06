---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520763"
---
# <span data-ttu-id="52d30-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="52d30-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="52d30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52d30-102">SYNOPSIS</span></span>
<span data-ttu-id="52d30-103">Ottiene le stringhe di connessione primarie e secondarie per l'argomento Service Bus.</span><span class="sxs-lookup"><span data-stu-id="52d30-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52d30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52d30-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d30-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52d30-105">DESCRIPTION</span></span>
<span data-ttu-id="52d30-106">Il cmdlet **Get-AzureRmServiceBusTopicKey** restituisce le stringhe di connessione primarie e secondarie per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="52d30-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="52d30-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52d30-107">EXAMPLES</span></span>

### <span data-ttu-id="52d30-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52d30-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="52d30-109">Restituisce le stringhe di connessione primarie e secondarie per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="52d30-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="52d30-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52d30-110">PARAMETERS</span></span>

### <span data-ttu-id="52d30-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52d30-111">-ResourceGroup</span></span>
<span data-ttu-id="52d30-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52d30-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="52d30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d30-113">-DefaultProfile</span></span>
<span data-ttu-id="52d30-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52d30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52d30-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="52d30-115">-Name</span></span>
<span data-ttu-id="52d30-116">Argomento AuthorizationRule nome.</span><span class="sxs-lookup"><span data-stu-id="52d30-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="52d30-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52d30-117">-Namespace</span></span>
<span data-ttu-id="52d30-118">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="52d30-118">Namespace Name.</span></span>

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

### <span data-ttu-id="52d30-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="52d30-119">-Topic</span></span>
<span data-ttu-id="52d30-120">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="52d30-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d30-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d30-121">CommonParameters</span></span>
<span data-ttu-id="52d30-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d30-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d30-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d30-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d30-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52d30-124">INPUTS</span></span>

### <span data-ttu-id="52d30-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52d30-125">-ResourceGroup</span></span>
 <span data-ttu-id="52d30-126">System. String</span><span class="sxs-lookup"><span data-stu-id="52d30-126">System.String</span></span>
 

### <span data-ttu-id="52d30-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="52d30-127">-NamespaceName</span></span>
 <span data-ttu-id="52d30-128">System. String</span><span class="sxs-lookup"><span data-stu-id="52d30-128">System.String</span></span>
 

### <span data-ttu-id="52d30-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="52d30-129">-TopicName</span></span>
 <span data-ttu-id="52d30-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52d30-130">System.String</span></span>
 

### <span data-ttu-id="52d30-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="52d30-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="52d30-132">System. String</span><span class="sxs-lookup"><span data-stu-id="52d30-132">System.String</span></span>

## <span data-ttu-id="52d30-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52d30-133">OUTPUTS</span></span>

### <span data-ttu-id="52d30-134">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="52d30-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="52d30-135">PrimaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-valore}; EntityPath = SB-to pic_exampl1 SecondaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-valore}; EntityPath = SB-to pic_exampl1 PrimaryKey: {PrimaryKey value} SecondaryKey: {SecondaryKey value} nome di pagina: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="52d30-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="52d30-136">Note</span><span class="sxs-lookup"><span data-stu-id="52d30-136">NOTES</span></span>

## <span data-ttu-id="52d30-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52d30-137">RELATED LINKS</span></span>

