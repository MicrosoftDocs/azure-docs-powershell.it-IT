---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685870"
---
# <span data-ttu-id="a7324-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a7324-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="a7324-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7324-102">SYNOPSIS</span></span>
<span data-ttu-id="a7324-103">Rimuove la regola di autorizzazione di uno spazio dei nomi o una coda o un argomento di Service Bus dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a7324-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7324-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7324-104">SYNTAX</span></span>

### <span data-ttu-id="a7324-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7324-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a7324-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7324-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a7324-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7324-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a7324-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7324-108">DESCRIPTION</span></span>
<span data-ttu-id="a7324-109">Il cmdlet **Remove-AzureRmServiceBusAuthorizationRule** rimuove la regola di autorizzazione di uno spazio dei nomi o una coda o un argomento di Service Bus per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a7324-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="a7324-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7324-110">EXAMPLES</span></span>

### <span data-ttu-id="a7324-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7324-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="a7324-112">Rimuove la regola `SBAuthoRule1` di autorizzazione dello spazio dei nomi `SB-Example1` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a7324-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="a7324-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a7324-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="a7324-114">Rimuove la regola `SBAuthoRule1` di autorizzazione di Queue `SBQueue` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a7324-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="a7324-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a7324-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="a7324-116">Rimuove la regola `SBAuthoRule1` di autorizzazione dell'argomento `SBTopic` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a7324-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="a7324-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7324-117">PARAMETERS</span></span>

### <span data-ttu-id="a7324-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7324-118">-Confirm</span></span>
<span data-ttu-id="a7324-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7324-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7324-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a7324-120">-Force</span></span>
<span data-ttu-id="a7324-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a7324-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7324-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7324-122">-Name</span></span>
<span data-ttu-id="a7324-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a7324-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7324-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7324-124">-Namespace</span></span>
<span data-ttu-id="a7324-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a7324-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7324-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7324-126">-PassThru</span></span>
<span data-ttu-id="a7324-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a7324-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7324-128">-Queue</span><span class="sxs-lookup"><span data-stu-id="a7324-128">-Queue</span></span>
<span data-ttu-id="a7324-129">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="a7324-129">Queue Name.</span></span>

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

### <span data-ttu-id="a7324-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7324-130">-ResourceGroupName</span></span>
<span data-ttu-id="a7324-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a7324-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="a7324-132">-Topic</span><span class="sxs-lookup"><span data-stu-id="a7324-132">-Topic</span></span>
<span data-ttu-id="a7324-133">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="a7324-133">Topic Name.</span></span>

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

### <span data-ttu-id="a7324-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7324-134">-WhatIf</span></span>
<span data-ttu-id="a7324-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7324-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7324-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7324-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a7324-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7324-137">INPUTS</span></span>

### <span data-ttu-id="a7324-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a7324-138">System.String</span></span>


## <span data-ttu-id="a7324-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7324-139">OUTPUTS</span></span>

### <span data-ttu-id="a7324-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7324-140">System.Boolean</span></span>


## <span data-ttu-id="a7324-141">Note</span><span class="sxs-lookup"><span data-stu-id="a7324-141">NOTES</span></span>

## <span data-ttu-id="a7324-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7324-142">RELATED LINKS</span></span>

