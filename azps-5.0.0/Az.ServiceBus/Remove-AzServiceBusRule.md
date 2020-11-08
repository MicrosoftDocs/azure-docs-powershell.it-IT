---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193213"
---
# <span data-ttu-id="bc19b-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="bc19b-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="bc19b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc19b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc19b-103">Rimuove la regola specificata di un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="bc19b-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="bc19b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc19b-104">SYNTAX</span></span>

### <span data-ttu-id="bc19b-105">RulePropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bc19b-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc19b-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bc19b-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc19b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc19b-107">DESCRIPTION</span></span>
<span data-ttu-id="bc19b-108">Il cmdlet **Remove-AzServiceBusRule** rimuove la regola di una sottoscrizione di un argomento specifico.</span><span class="sxs-lookup"><span data-stu-id="bc19b-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="bc19b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc19b-109">EXAMPLES</span></span>

### <span data-ttu-id="bc19b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc19b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="bc19b-111">Rimuove la regola `SBRule` di sottoscrizione `SBSubscription` dell'argomento specificato `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="bc19b-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="bc19b-112">Esempio 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="bc19b-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="bc19b-113">Rimuove la regola fornita tramite $inputobject parametro for-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc19b-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="bc19b-114">Esempio 3: InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="bc19b-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="bc19b-115">Esempio 4: ResourceId-utilizzo della variabile</span><span class="sxs-lookup"><span data-stu-id="bc19b-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="bc19b-116">Esempio 5: ResourceId-utilizzo di un valore stringa</span><span class="sxs-lookup"><span data-stu-id="bc19b-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="bc19b-117">Rimuove la regola fornita tramite ID ARM in $resourceid parametro/String for-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc19b-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="bc19b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc19b-118">PARAMETERS</span></span>

### <span data-ttu-id="bc19b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc19b-119">-AsJob</span></span>
<span data-ttu-id="bc19b-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bc19b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc19b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc19b-121">-DefaultProfile</span></span>
<span data-ttu-id="bc19b-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc19b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc19b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bc19b-123">-Force</span></span>
<span data-ttu-id="bc19b-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="bc19b-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bc19b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc19b-125">-InputObject</span></span>
<span data-ttu-id="bc19b-126">Oggetto regola Service Bus</span><span class="sxs-lookup"><span data-stu-id="bc19b-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc19b-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc19b-127">-Name</span></span>
<span data-ttu-id="bc19b-128">Nome regola</span><span class="sxs-lookup"><span data-stu-id="bc19b-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc19b-129">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc19b-129">-Namespace</span></span>
<span data-ttu-id="bc19b-130">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc19b-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc19b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc19b-131">-PassThru</span></span>
<span data-ttu-id="bc19b-132">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="bc19b-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="bc19b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc19b-133">-ResourceGroupName</span></span>
<span data-ttu-id="bc19b-134">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bc19b-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc19b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc19b-135">-ResourceId</span></span>
<span data-ttu-id="bc19b-136">ID risorsa della regola Service Bus</span><span class="sxs-lookup"><span data-stu-id="bc19b-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc19b-137">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="bc19b-137">-Subscription</span></span>
<span data-ttu-id="bc19b-138">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="bc19b-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc19b-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="bc19b-139">-Topic</span></span>
<span data-ttu-id="bc19b-140">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="bc19b-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc19b-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc19b-141">-Confirm</span></span>
<span data-ttu-id="bc19b-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc19b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc19b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc19b-143">-WhatIf</span></span>
<span data-ttu-id="bc19b-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc19b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc19b-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc19b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc19b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc19b-146">CommonParameters</span></span>
<span data-ttu-id="bc19b-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc19b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc19b-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc19b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc19b-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc19b-149">INPUTS</span></span>

### <span data-ttu-id="bc19b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bc19b-150">System.String</span></span>

### <span data-ttu-id="bc19b-151">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="bc19b-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="bc19b-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc19b-152">OUTPUTS</span></span>

### <span data-ttu-id="bc19b-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc19b-153">System.Boolean</span></span>

## <span data-ttu-id="bc19b-154">Note</span><span class="sxs-lookup"><span data-stu-id="bc19b-154">NOTES</span></span>

## <span data-ttu-id="bc19b-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc19b-155">RELATED LINKS</span></span>
