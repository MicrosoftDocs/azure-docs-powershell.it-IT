---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201686"
---
# <span data-ttu-id="6fff1-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6fff1-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="6fff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fff1-102">SYNOPSIS</span></span>
<span data-ttu-id="6fff1-103">Ottiene una descrizione della regola di autorizzazione specificata per uno spazio dei nomi o una coda o un argomento o alias (configurazioni geoDR) specificato.</span><span class="sxs-lookup"><span data-stu-id="6fff1-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="6fff1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fff1-104">SYNTAX</span></span>

### <span data-ttu-id="6fff1-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6fff1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fff1-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6fff1-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fff1-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6fff1-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fff1-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="6fff1-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fff1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6fff1-109">DESCRIPTION</span></span>
<span data-ttu-id="6fff1-110">Il cmdlet **Get-AzServiceBusAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nello spazio dei nomi o nella coda o nell'argomento o alias (configurazioni geoDR) specificati.</span><span class="sxs-lookup"><span data-stu-id="6fff1-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="6fff1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fff1-111">EXAMPLES</span></span>

### <span data-ttu-id="6fff1-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6fff1-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="6fff1-113">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="6fff1-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="6fff1-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6fff1-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="6fff1-115">Restituisce la descrizione della regola di autorizzazione specificata per una coda specificata.</span><span class="sxs-lookup"><span data-stu-id="6fff1-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="6fff1-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6fff1-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="6fff1-117">Restituisce la descrizione della regola di autorizzazione specificata per un argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="6fff1-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="6fff1-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="6fff1-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="6fff1-119">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi e un alias specificati.</span><span class="sxs-lookup"><span data-stu-id="6fff1-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="6fff1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fff1-120">PARAMETERS</span></span>

### <span data-ttu-id="6fff1-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="6fff1-121">-AliasName</span></span>
<span data-ttu-id="6fff1-122">Nome configurazione GeoDR</span><span class="sxs-lookup"><span data-stu-id="6fff1-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="6fff1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fff1-123">-DefaultProfile</span></span>
<span data-ttu-id="6fff1-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fff1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fff1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6fff1-125">-Name</span></span>
<span data-ttu-id="6fff1-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="6fff1-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="6fff1-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6fff1-127">-Namespace</span></span>
<span data-ttu-id="6fff1-128">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6fff1-128">Namespace Name</span></span>

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

### <span data-ttu-id="6fff1-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="6fff1-129">-Queue</span></span>
<span data-ttu-id="6fff1-130">Nome coda</span><span class="sxs-lookup"><span data-stu-id="6fff1-130">Queue Name</span></span>

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

### <span data-ttu-id="6fff1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fff1-131">-ResourceGroupName</span></span>
<span data-ttu-id="6fff1-132">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6fff1-132">Resource Group Name</span></span>

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

### <span data-ttu-id="6fff1-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="6fff1-133">-Topic</span></span>
<span data-ttu-id="6fff1-134">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="6fff1-134">Topic Name</span></span>

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

### <span data-ttu-id="6fff1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fff1-135">CommonParameters</span></span>
<span data-ttu-id="6fff1-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fff1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fff1-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fff1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fff1-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="6fff1-138">INPUTS</span></span>

### <span data-ttu-id="6fff1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6fff1-139">System.String</span></span>

## <span data-ttu-id="6fff1-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fff1-140">OUTPUTS</span></span>

### <span data-ttu-id="6fff1-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6fff1-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6fff1-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="6fff1-142">NOTES</span></span>

## <span data-ttu-id="6fff1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fff1-143">RELATED LINKS</span></span>
