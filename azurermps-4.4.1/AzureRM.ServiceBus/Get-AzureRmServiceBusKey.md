---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510339"
---
# <span data-ttu-id="4177f-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="4177f-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="4177f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4177f-102">SYNOPSIS</span></span>
<span data-ttu-id="4177f-103">Ottiene le stringhe di connessione primarie e secondarie per lo spazio dei nomi o la coda o l'argomento specifico.</span><span class="sxs-lookup"><span data-stu-id="4177f-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4177f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4177f-104">SYNTAX</span></span>

### <span data-ttu-id="4177f-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4177f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4177f-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4177f-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4177f-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4177f-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4177f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4177f-108">DESCRIPTION</span></span>
<span data-ttu-id="4177f-109">Il cmdlet **Get-AzureRmServiceBusKey** restituisce le stringhe di connessione primarie e secondarie per lo spazio dei nomi o la coda o l'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="4177f-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="4177f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4177f-110">EXAMPLES</span></span>

### <span data-ttu-id="4177f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4177f-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="4177f-112">Stringa di connessione primaria e secondaria allo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="4177f-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="4177f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4177f-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="4177f-114">Stringa di connessione primaria e secondaria alla coda specificata.</span><span class="sxs-lookup"><span data-stu-id="4177f-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="4177f-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4177f-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="4177f-116">Stringa di connessione primaria e secondaria all'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="4177f-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="4177f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4177f-117">PARAMETERS</span></span>

### <span data-ttu-id="4177f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4177f-118">-Name</span></span>
<span data-ttu-id="4177f-119">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="4177f-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4177f-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4177f-120">-Namespace</span></span>
<span data-ttu-id="4177f-121">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4177f-121">Namespace Name.</span></span>

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

### <span data-ttu-id="4177f-122">-Queue</span><span class="sxs-lookup"><span data-stu-id="4177f-122">-Queue</span></span>
<span data-ttu-id="4177f-123">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="4177f-123">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4177f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4177f-124">-ResourceGroupName</span></span>
<span data-ttu-id="4177f-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4177f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4177f-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="4177f-126">-Topic</span></span>
<span data-ttu-id="4177f-127">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="4177f-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4177f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4177f-128">-DefaultProfile</span></span>
<span data-ttu-id="4177f-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4177f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4177f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4177f-130">CommonParameters</span></span>
<span data-ttu-id="4177f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4177f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4177f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4177f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4177f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4177f-133">INPUTS</span></span>

### <span data-ttu-id="4177f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4177f-134">System.String</span></span>

## <span data-ttu-id="4177f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4177f-135">OUTPUTS</span></span>

### <span data-ttu-id="4177f-136">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4177f-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="4177f-137">Note</span><span class="sxs-lookup"><span data-stu-id="4177f-137">NOTES</span></span>

## <span data-ttu-id="4177f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4177f-138">RELATED LINKS</span></span>

