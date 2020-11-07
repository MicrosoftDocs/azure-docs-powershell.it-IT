---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: d1cb165b537815227a15223a1b646c38892005bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677135"
---
# <span data-ttu-id="b4844-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b4844-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="b4844-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4844-102">SYNOPSIS</span></span>
<span data-ttu-id="b4844-103">Rimuove la regola di autorizzazione di uno spazio dei nomi o una coda o un argomento di Service Bus dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b4844-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="b4844-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4844-104">SYNTAX</span></span>

### <span data-ttu-id="b4844-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4844-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4844-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4844-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4844-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4844-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4844-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4844-108">DESCRIPTION</span></span>
<span data-ttu-id="b4844-109">Il cmdlet **Remove-AzServiceBusAuthorizationRule** rimuove la regola di autorizzazione di uno spazio dei nomi o una coda o un argomento di Service Bus per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b4844-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="b4844-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4844-110">EXAMPLES</span></span>

### <span data-ttu-id="b4844-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b4844-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="b4844-112">Rimuove la regola `SBAuthoRule1` di autorizzazione dello spazio dei nomi `SB-Example1` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b4844-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="b4844-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b4844-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="b4844-114">Rimuove la regola `SBAuthoRule1` di autorizzazione di Queue `SBQueue` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b4844-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="b4844-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b4844-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="b4844-116">Rimuove la regola `SBAuthoRule1` di autorizzazione dell'argomento `SBTopic` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b4844-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="b4844-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4844-117">PARAMETERS</span></span>

### <span data-ttu-id="b4844-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4844-118">-DefaultProfile</span></span>
<span data-ttu-id="b4844-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4844-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4844-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b4844-120">-Force</span></span>
<span data-ttu-id="b4844-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b4844-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b4844-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4844-122">-InputObject</span></span>
<span data-ttu-id="b4844-123">Oggetto AuthorizationRule di ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b4844-123">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="b4844-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4844-124">-Name</span></span>
<span data-ttu-id="b4844-125">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b4844-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b4844-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4844-126">-Namespace</span></span>
<span data-ttu-id="b4844-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4844-127">Namespace Name</span></span>

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

### <span data-ttu-id="b4844-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4844-128">-PassThru</span></span>
<span data-ttu-id="b4844-129">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b4844-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b4844-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b4844-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4844-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="b4844-131">-Queue</span></span>
<span data-ttu-id="b4844-132">Nome coda</span><span class="sxs-lookup"><span data-stu-id="b4844-132">Queue Name</span></span>

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

### <span data-ttu-id="b4844-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4844-133">-ResourceGroupName</span></span>
<span data-ttu-id="b4844-134">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b4844-134">Resource Group Name</span></span>

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

### <span data-ttu-id="b4844-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="b4844-135">-Topic</span></span>
<span data-ttu-id="b4844-136">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="b4844-136">Topic Name</span></span>

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

### <span data-ttu-id="b4844-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4844-137">-Confirm</span></span>
<span data-ttu-id="b4844-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4844-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4844-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4844-139">-WhatIf</span></span>
<span data-ttu-id="b4844-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4844-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4844-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4844-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4844-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4844-142">CommonParameters</span></span>
<span data-ttu-id="b4844-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4844-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4844-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4844-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4844-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4844-145">INPUTS</span></span>

### <span data-ttu-id="b4844-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b4844-146">System.String</span></span>

### <span data-ttu-id="b4844-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b4844-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b4844-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4844-148">OUTPUTS</span></span>

### <span data-ttu-id="b4844-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4844-149">System.Boolean</span></span>

## <span data-ttu-id="b4844-150">Note</span><span class="sxs-lookup"><span data-stu-id="b4844-150">NOTES</span></span>

## <span data-ttu-id="b4844-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4844-151">RELATED LINKS</span></span>
