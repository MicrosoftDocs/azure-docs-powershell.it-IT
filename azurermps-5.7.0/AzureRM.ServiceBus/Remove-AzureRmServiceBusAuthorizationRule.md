---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: a41ddb9ee845bce0687448d0745904b9cec9ba05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517972"
---
# <span data-ttu-id="93f0b-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="93f0b-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="93f0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="93f0b-103">Rimuove la regola di autorizzazione di uno spazio dei nomi o una coda o un argomento di Service Bus dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="93f0b-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93f0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93f0b-104">SYNTAX</span></span>

### <span data-ttu-id="93f0b-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93f0b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f0b-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="93f0b-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f0b-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="93f0b-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93f0b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93f0b-108">DESCRIPTION</span></span>
<span data-ttu-id="93f0b-109">Il cmdlet **Remove-AzureRmServiceBusAuthorizationRule** rimuove la regola di autorizzazione di uno spazio dei nomi o una coda o un argomento di Service Bus per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="93f0b-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="93f0b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93f0b-110">EXAMPLES</span></span>

### <span data-ttu-id="93f0b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93f0b-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="93f0b-112">Rimuove la regola `SBAuthoRule1` di autorizzazione dello spazio dei nomi `SB-Example1` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="93f0b-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="93f0b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="93f0b-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="93f0b-114">Rimuove la regola `SBAuthoRule1` di autorizzazione di Queue `SBQueue` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="93f0b-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="93f0b-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="93f0b-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="93f0b-116">Rimuove la regola `SBAuthoRule1` di autorizzazione dell'argomento `SBTopic` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="93f0b-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="93f0b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93f0b-117">PARAMETERS</span></span>

### <span data-ttu-id="93f0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f0b-118">-DefaultProfile</span></span>
<span data-ttu-id="93f0b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93f0b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f0b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="93f0b-120">-Force</span></span>
<span data-ttu-id="93f0b-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="93f0b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="93f0b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93f0b-122">-InputObject</span></span>
<span data-ttu-id="93f0b-123">Oggetto AuthorizationRule di ServiceBus</span><span class="sxs-lookup"><span data-stu-id="93f0b-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93f0b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="93f0b-124">-Name</span></span>
<span data-ttu-id="93f0b-125">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="93f0b-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="93f0b-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="93f0b-126">-Namespace</span></span>
<span data-ttu-id="93f0b-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="93f0b-127">Namespace Name</span></span>

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

### <span data-ttu-id="93f0b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93f0b-128">-PassThru</span></span>
<span data-ttu-id="93f0b-129">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="93f0b-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93f0b-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="93f0b-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93f0b-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="93f0b-131">-Queue</span></span>
<span data-ttu-id="93f0b-132">Nome coda</span><span class="sxs-lookup"><span data-stu-id="93f0b-132">Queue Name</span></span>

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

### <span data-ttu-id="93f0b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f0b-133">-ResourceGroupName</span></span>
<span data-ttu-id="93f0b-134">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="93f0b-134">Resource Group Name</span></span>

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

### <span data-ttu-id="93f0b-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="93f0b-135">-Topic</span></span>
<span data-ttu-id="93f0b-136">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="93f0b-136">Topic Name</span></span>

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

### <span data-ttu-id="93f0b-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93f0b-137">-Confirm</span></span>
<span data-ttu-id="93f0b-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93f0b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f0b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f0b-139">-WhatIf</span></span>
<span data-ttu-id="93f0b-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93f0b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f0b-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93f0b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f0b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f0b-142">CommonParameters</span></span>
<span data-ttu-id="93f0b-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f0b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="93f0b-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f0b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f0b-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93f0b-145">INPUTS</span></span>

### <span data-ttu-id="93f0b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="93f0b-146">System.String</span></span>
<span data-ttu-id="93f0b-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="93f0b-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="93f0b-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93f0b-148">OUTPUTS</span></span>

### <span data-ttu-id="93f0b-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93f0b-149">System.Boolean</span></span>


## <span data-ttu-id="93f0b-150">Note</span><span class="sxs-lookup"><span data-stu-id="93f0b-150">NOTES</span></span>

## <span data-ttu-id="93f0b-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93f0b-151">RELATED LINKS</span></span>
