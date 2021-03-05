---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 5a33eae7e31ecdc793411bcddc2855d0dbcce8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961645"
---
# <span data-ttu-id="ecaa4-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ecaa4-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ecaa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecaa4-102">SYNOPSIS</span></span>
<span data-ttu-id="ecaa4-103">Rimuove la regola di autorizzazione di uno spazio dei nomi o di una coda di bus di servizio o di un argomento dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="ecaa4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecaa4-104">SYNTAX</span></span>

### <span data-ttu-id="ecaa4-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecaa4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecaa4-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecaa4-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecaa4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecaa4-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecaa4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecaa4-108">DESCRIPTION</span></span>
<span data-ttu-id="ecaa4-109">Il cmdlet **Remove-AzServiceBusAuthorizationRule** rimuove la regola di autorizzazione di uno spazio dei nomi o di una coda o di un argomento del bus di servizio per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="ecaa4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecaa4-110">EXAMPLES</span></span>

### <span data-ttu-id="ecaa4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ecaa4-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="ecaa4-112">Rimuove la regola di autorizzazione `SBAuthoRule1` dello spazio dei nomi dal gruppo di risorse `SB-Example1` specificato.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="ecaa4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ecaa4-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="ecaa4-114">Rimuove la regola di autorizzazione `SBAuthoRule1` della coda dal gruppo di risorse `SBQueue` specificato.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="ecaa4-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ecaa4-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="ecaa4-116">Rimuove la regola di `SBAuthoRule1` autorizzazione `SBTopic` dell'argomento dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="ecaa4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecaa4-117">PARAMETERS</span></span>

### <span data-ttu-id="ecaa4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecaa4-118">-DefaultProfile</span></span>
<span data-ttu-id="ecaa4-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecaa4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ecaa4-120">-Force</span></span>
<span data-ttu-id="ecaa4-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecaa4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecaa4-122">-InputObject</span></span>
<span data-ttu-id="ecaa4-123">Oggetto ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ecaa4-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecaa4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ecaa4-124">-Name</span></span>
<span data-ttu-id="ecaa4-125">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="ecaa4-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ecaa4-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ecaa4-126">-Namespace</span></span>
<span data-ttu-id="ecaa4-127">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ecaa4-127">Namespace Name</span></span>

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

### <span data-ttu-id="ecaa4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecaa4-128">-PassThru</span></span>
<span data-ttu-id="ecaa4-129">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ecaa4-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecaa4-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="ecaa4-131">-Queue</span></span>
<span data-ttu-id="ecaa4-132">Nome coda</span><span class="sxs-lookup"><span data-stu-id="ecaa4-132">Queue Name</span></span>

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

### <span data-ttu-id="ecaa4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecaa4-133">-ResourceGroupName</span></span>
<span data-ttu-id="ecaa4-134">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ecaa4-134">Resource Group Name</span></span>

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

### <span data-ttu-id="ecaa4-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="ecaa4-135">-Topic</span></span>
<span data-ttu-id="ecaa4-136">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="ecaa4-136">Topic Name</span></span>

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

### <span data-ttu-id="ecaa4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecaa4-137">-Confirm</span></span>
<span data-ttu-id="ecaa4-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecaa4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecaa4-139">-WhatIf</span></span>
<span data-ttu-id="ecaa4-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecaa4-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecaa4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecaa4-142">CommonParameters</span></span>
<span data-ttu-id="ecaa4-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecaa4-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecaa4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecaa4-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecaa4-145">INPUTS</span></span>

### <span data-ttu-id="ecaa4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ecaa4-146">System.String</span></span>

### <span data-ttu-id="ecaa4-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ecaa4-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ecaa4-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecaa4-148">OUTPUTS</span></span>

### <span data-ttu-id="ecaa4-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ecaa4-149">System.Boolean</span></span>

## <span data-ttu-id="ecaa4-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecaa4-150">NOTES</span></span>

## <span data-ttu-id="ecaa4-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecaa4-151">RELATED LINKS</span></span>
