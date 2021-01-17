---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486023"
---
# <span data-ttu-id="ccecc-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="ccecc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccecc-102">SYNOPSIS</span></span>
<span data-ttu-id="ccecc-103">Rimuove NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="ccecc-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="ccecc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccecc-104">SYNTAX</span></span>

### <span data-ttu-id="ccecc-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ccecc-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccecc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccecc-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccecc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccecc-108">DESCRIPTION</span></span>
<span data-ttu-id="ccecc-109">Rimuove NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="ccecc-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="ccecc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccecc-110">EXAMPLES</span></span>

### <span data-ttu-id="ccecc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ccecc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="ccecc-112">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="ccecc-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="ccecc-113">Elimina il NetworkRuleSet per lo spazio dei nomi "ServiceBus-Namespace1-1375" indicato</span><span class="sxs-lookup"><span data-stu-id="ccecc-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="ccecc-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ccecc-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="ccecc-115">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="ccecc-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="ccecc-116">Elimina il NetworkRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="ccecc-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="ccecc-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ccecc-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="ccecc-118">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="ccecc-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="ccecc-119">Elimina NetworkRuleSet usando ResourceId dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ccecc-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="ccecc-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccecc-120">PARAMETERS</span></span>

### <span data-ttu-id="ccecc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccecc-121">-AsJob</span></span>
<span data-ttu-id="ccecc-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ccecc-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccecc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccecc-123">-DefaultProfile</span></span>
<span data-ttu-id="ccecc-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ccecc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccecc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccecc-125">-InputObject</span></span>
<span data-ttu-id="ccecc-126">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="ccecc-126">Namespace Object</span></span>

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

### <span data-ttu-id="ccecc-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccecc-127">-Name</span></span>
<span data-ttu-id="ccecc-128">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ccecc-128">Namespace Name</span></span>

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

### <span data-ttu-id="ccecc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccecc-129">-PassThru</span></span>
<span data-ttu-id="ccecc-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ccecc-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ccecc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccecc-131">-ResourceGroupName</span></span>
<span data-ttu-id="ccecc-132">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ccecc-132">Resource Group Name</span></span>

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

### <span data-ttu-id="ccecc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccecc-133">-ResourceId</span></span>
<span data-ttu-id="ccecc-134">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ccecc-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="ccecc-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ccecc-135">-Confirm</span></span>
<span data-ttu-id="ccecc-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccecc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccecc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccecc-137">-WhatIf</span></span>
<span data-ttu-id="ccecc-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccecc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccecc-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccecc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccecc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccecc-140">CommonParameters</span></span>
<span data-ttu-id="ccecc-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccecc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ccecc-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccecc-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccecc-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccecc-143">INPUTS</span></span>

### <span data-ttu-id="ccecc-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ccecc-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="ccecc-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ccecc-145">System.String</span></span>

## <span data-ttu-id="ccecc-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccecc-146">OUTPUTS</span></span>

### <span data-ttu-id="ccecc-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ccecc-147">System.Boolean</span></span>

## <span data-ttu-id="ccecc-148">Note</span><span class="sxs-lookup"><span data-stu-id="ccecc-148">NOTES</span></span>

## <span data-ttu-id="ccecc-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccecc-149">RELATED LINKS</span></span>
