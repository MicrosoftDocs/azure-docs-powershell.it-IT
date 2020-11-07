---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 4717775f840d816b8f99cc64c4036d5563e8d849
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677171"
---
# <span data-ttu-id="12f5a-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12f5a-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="12f5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="12f5a-103">Ottiene una descrizione della regola di autorizzazione specificata per un determinato spazio dei nomi o una coda o un argomento o un alias (configurazioni GeoDR).</span><span class="sxs-lookup"><span data-stu-id="12f5a-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="12f5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12f5a-104">SYNTAX</span></span>

### <span data-ttu-id="12f5a-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12f5a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12f5a-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="12f5a-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12f5a-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="12f5a-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12f5a-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="12f5a-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f5a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12f5a-109">DESCRIPTION</span></span>
<span data-ttu-id="12f5a-110">Il cmdlet **Get-AzServiceBusAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nello spazio dei nomi specificato o in una coda o un argomento o un alias (configurazioni GeoDR).</span><span class="sxs-lookup"><span data-stu-id="12f5a-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="12f5a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12f5a-111">EXAMPLES</span></span>

### <span data-ttu-id="12f5a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12f5a-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="12f5a-113">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="12f5a-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="12f5a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="12f5a-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="12f5a-115">Restituisce la descrizione della regola di autorizzazione specificata per una coda specificata.</span><span class="sxs-lookup"><span data-stu-id="12f5a-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="12f5a-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="12f5a-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="12f5a-117">Restituisce la descrizione della regola di autorizzazione specificata per un argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="12f5a-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="12f5a-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="12f5a-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="12f5a-119">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi e un alias specificati.</span><span class="sxs-lookup"><span data-stu-id="12f5a-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="12f5a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12f5a-120">PARAMETERS</span></span>

### <span data-ttu-id="12f5a-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="12f5a-121">-AliasName</span></span>
<span data-ttu-id="12f5a-122">Nome configurazione GeoDR</span><span class="sxs-lookup"><span data-stu-id="12f5a-122">GeoDR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12f5a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f5a-123">-DefaultProfile</span></span>
<span data-ttu-id="12f5a-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12f5a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f5a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="12f5a-125">-Name</span></span>
<span data-ttu-id="12f5a-126">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12f5a-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="12f5a-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12f5a-127">-Namespace</span></span>
<span data-ttu-id="12f5a-128">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12f5a-128">Namespace Name</span></span>

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

### <span data-ttu-id="12f5a-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="12f5a-129">-Queue</span></span>
<span data-ttu-id="12f5a-130">Nome coda</span><span class="sxs-lookup"><span data-stu-id="12f5a-130">Queue Name</span></span>

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

### <span data-ttu-id="12f5a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f5a-131">-ResourceGroupName</span></span>
<span data-ttu-id="12f5a-132">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="12f5a-132">Resource Group Name</span></span>

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

### <span data-ttu-id="12f5a-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="12f5a-133">-Topic</span></span>
<span data-ttu-id="12f5a-134">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="12f5a-134">Topic Name</span></span>

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

### <span data-ttu-id="12f5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f5a-135">CommonParameters</span></span>
<span data-ttu-id="12f5a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f5a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f5a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f5a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12f5a-138">INPUTS</span></span>

### <span data-ttu-id="12f5a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="12f5a-139">System.String</span></span>

## <span data-ttu-id="12f5a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12f5a-140">OUTPUTS</span></span>

### <span data-ttu-id="12f5a-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="12f5a-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="12f5a-142">Note</span><span class="sxs-lookup"><span data-stu-id="12f5a-142">NOTES</span></span>

## <span data-ttu-id="12f5a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12f5a-143">RELATED LINKS</span></span>