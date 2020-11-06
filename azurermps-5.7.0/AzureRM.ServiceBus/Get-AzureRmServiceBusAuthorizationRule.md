---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: e5a4886eef132f0e48c146fa70889dfa283489b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512292"
---
# <span data-ttu-id="1bc33-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1bc33-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="1bc33-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bc33-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc33-103">Ottiene una descrizione della regola di autorizzazione specificata per un determinato spazio dei nomi o una coda o un argomento o un alias (configurazioni GeoDR).</span><span class="sxs-lookup"><span data-stu-id="1bc33-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 


[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bc33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bc33-104">SYNTAX</span></span>

### <span data-ttu-id="1bc33-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1bc33-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bc33-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1bc33-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bc33-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1bc33-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bc33-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="1bc33-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bc33-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bc33-109">DESCRIPTION</span></span>
<span data-ttu-id="1bc33-110">Il cmdlet **Get-AzureRmServiceBusAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nello spazio dei nomi specificato o in una coda o un argomento o un alias (configurazioni GeoDR).</span><span class="sxs-lookup"><span data-stu-id="1bc33-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="1bc33-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bc33-111">EXAMPLES</span></span>

### <span data-ttu-id="1bc33-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1bc33-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="1bc33-113">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="1bc33-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="1bc33-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1bc33-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="1bc33-115">Restituisce la descrizione della regola di autorizzazione specificata per una coda specificata.</span><span class="sxs-lookup"><span data-stu-id="1bc33-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="1bc33-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1bc33-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="1bc33-117">Restituisce la descrizione della regola di autorizzazione specificata per un argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="1bc33-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="1bc33-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="1bc33-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="1bc33-119">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi e un alias specificati.</span><span class="sxs-lookup"><span data-stu-id="1bc33-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="1bc33-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bc33-120">PARAMETERS</span></span>

### <span data-ttu-id="1bc33-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="1bc33-121">-AliasName</span></span>
<span data-ttu-id="1bc33-122">Nome configurazione GeoDR</span><span class="sxs-lookup"><span data-stu-id="1bc33-122">GeoDR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc33-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc33-123">-DefaultProfile</span></span>
<span data-ttu-id="1bc33-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bc33-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bc33-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bc33-125">-Name</span></span>
<span data-ttu-id="1bc33-126">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1bc33-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc33-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1bc33-127">-Namespace</span></span>
<span data-ttu-id="1bc33-128">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1bc33-128">Namespace Name</span></span>

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

### <span data-ttu-id="1bc33-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="1bc33-129">-Queue</span></span>
<span data-ttu-id="1bc33-130">Nome coda</span><span class="sxs-lookup"><span data-stu-id="1bc33-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc33-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bc33-131">-ResourceGroupName</span></span>
<span data-ttu-id="1bc33-132">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1bc33-132">Resource Group Name</span></span>

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

### <span data-ttu-id="1bc33-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="1bc33-133">-Topic</span></span>
<span data-ttu-id="1bc33-134">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="1bc33-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc33-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc33-135">CommonParameters</span></span>
<span data-ttu-id="1bc33-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bc33-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1bc33-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc33-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc33-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bc33-138">INPUTS</span></span>

### <span data-ttu-id="1bc33-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1bc33-139">System.String</span></span>


## <span data-ttu-id="1bc33-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bc33-140">OUTPUTS</span></span>

### <span data-ttu-id="1bc33-141">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1bc33-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="1bc33-142">Note</span><span class="sxs-lookup"><span data-stu-id="1bc33-142">NOTES</span></span>

## <span data-ttu-id="1bc33-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bc33-143">RELATED LINKS</span></span>
