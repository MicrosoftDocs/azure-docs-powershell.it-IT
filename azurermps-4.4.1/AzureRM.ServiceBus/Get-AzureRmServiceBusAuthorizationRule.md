---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521527"
---
# <span data-ttu-id="d17cf-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d17cf-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="d17cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d17cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d17cf-103">Ottiene una descrizione della regola di autorizzazione specificata per uno spazio dei nomi o una coda o un argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="d17cf-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d17cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d17cf-104">SYNTAX</span></span>

### <span data-ttu-id="d17cf-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d17cf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d17cf-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d17cf-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d17cf-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d17cf-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d17cf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d17cf-108">DESCRIPTION</span></span>
<span data-ttu-id="d17cf-109">Il cmdlet **Get-AzureRmServiceBusAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nello spazio dei nomi o in una coda o un argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="d17cf-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="d17cf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d17cf-110">EXAMPLES</span></span>

### <span data-ttu-id="d17cf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d17cf-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="d17cf-112">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="d17cf-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="d17cf-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d17cf-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="d17cf-114">Restituisce la descrizione della regola di autorizzazione specificata per una coda specificata.</span><span class="sxs-lookup"><span data-stu-id="d17cf-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="d17cf-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d17cf-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="d17cf-116">Restituisce la descrizione della regola di autorizzazione specificata per un argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="d17cf-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="d17cf-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d17cf-117">PARAMETERS</span></span>

### <span data-ttu-id="d17cf-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d17cf-118">-Name</span></span>
<span data-ttu-id="d17cf-119">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="d17cf-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17cf-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d17cf-120">-Namespace</span></span>
<span data-ttu-id="d17cf-121">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d17cf-121">Namespace Name.</span></span>

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

### <span data-ttu-id="d17cf-122">-Queue</span><span class="sxs-lookup"><span data-stu-id="d17cf-122">-Queue</span></span>
<span data-ttu-id="d17cf-123">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="d17cf-123">Queue Name.</span></span>

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

### <span data-ttu-id="d17cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="d17cf-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d17cf-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d17cf-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="d17cf-126">-Topic</span></span>
<span data-ttu-id="d17cf-127">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="d17cf-127">Topic Name.</span></span>

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

### <span data-ttu-id="d17cf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17cf-128">-DefaultProfile</span></span>
<span data-ttu-id="d17cf-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d17cf-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d17cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17cf-130">CommonParameters</span></span>
<span data-ttu-id="d17cf-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17cf-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d17cf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17cf-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d17cf-133">INPUTS</span></span>

### <span data-ttu-id="d17cf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d17cf-134">System.String</span></span>

## <span data-ttu-id="d17cf-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d17cf-135">OUTPUTS</span></span>

### <span data-ttu-id="d17cf-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d17cf-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d17cf-137">Note</span><span class="sxs-lookup"><span data-stu-id="d17cf-137">NOTES</span></span>
## <span data-ttu-id="d17cf-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d17cf-138">RELATED LINKS</span></span>

## <span data-ttu-id="d17cf-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d17cf-139">RELATED LINKS</span></span>

