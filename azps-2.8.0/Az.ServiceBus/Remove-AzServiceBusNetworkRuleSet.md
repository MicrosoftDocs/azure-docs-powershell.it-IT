---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: dadabed1a9e78fe44d28eae31adcf70d2aad2ea5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854629"
---
# <span data-ttu-id="cec28-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cec28-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="cec28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cec28-102">SYNOPSIS</span></span>
<span data-ttu-id="cec28-103">Rimuove NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="cec28-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="cec28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cec28-104">SYNTAX</span></span>

### <span data-ttu-id="cec28-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cec28-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cec28-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cec28-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cec28-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cec28-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cec28-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cec28-108">DESCRIPTION</span></span>
<span data-ttu-id="cec28-109">Rimuove NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="cec28-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="cec28-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cec28-110">EXAMPLES</span></span>

### <span data-ttu-id="cec28-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cec28-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="cec28-112">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="cec28-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="cec28-113">Elimina il NetworkRuleSet per lo spazio dei nomi "ServiceBus-Namespace1-1375" indicato</span><span class="sxs-lookup"><span data-stu-id="cec28-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="cec28-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cec28-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="cec28-115">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="cec28-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="cec28-116">Elimina il NetworkRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="cec28-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="cec28-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="cec28-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="cec28-118">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="cec28-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="cec28-119">Elimina NetworkRuleSet usando ResourceId dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cec28-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="cec28-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cec28-120">PARAMETERS</span></span>

### <span data-ttu-id="cec28-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cec28-121">-AsJob</span></span>
<span data-ttu-id="cec28-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cec28-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cec28-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec28-123">-DefaultProfile</span></span>
<span data-ttu-id="cec28-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cec28-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cec28-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cec28-125">-InputObject</span></span>
<span data-ttu-id="cec28-126">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="cec28-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cec28-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="cec28-127">-Name</span></span>
<span data-ttu-id="cec28-128">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cec28-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec28-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cec28-129">-PassThru</span></span>
<span data-ttu-id="cec28-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cec28-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cec28-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cec28-131">-ResourceGroupName</span></span>
<span data-ttu-id="cec28-132">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cec28-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec28-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cec28-133">-ResourceId</span></span>
<span data-ttu-id="cec28-134">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cec28-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec28-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cec28-135">-Confirm</span></span>
<span data-ttu-id="cec28-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cec28-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cec28-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cec28-137">-WhatIf</span></span>
<span data-ttu-id="cec28-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cec28-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cec28-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cec28-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cec28-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec28-140">CommonParameters</span></span>
<span data-ttu-id="cec28-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cec28-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cec28-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cec28-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec28-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cec28-143">INPUTS</span></span>

### <span data-ttu-id="cec28-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cec28-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="cec28-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cec28-145">System.String</span></span>

## <span data-ttu-id="cec28-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cec28-146">OUTPUTS</span></span>

### <span data-ttu-id="cec28-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cec28-147">System.Boolean</span></span>

## <span data-ttu-id="cec28-148">Note</span><span class="sxs-lookup"><span data-stu-id="cec28-148">NOTES</span></span>

## <span data-ttu-id="cec28-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cec28-149">RELATED LINKS</span></span>
