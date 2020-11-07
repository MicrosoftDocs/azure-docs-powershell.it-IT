---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: d200d342bfa16fb0b2864e0196dc9648b4aa7fcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677160"
---
# <span data-ttu-id="f4530-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4530-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="f4530-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4530-102">SYNOPSIS</span></span>
<span data-ttu-id="f4530-103">Ottiene i dettagli di un evento Hub NetwrokruleSet dello spazio dei nomi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="f4530-103">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f4530-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4530-104">SYNTAX</span></span>

### <span data-ttu-id="f4530-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4530-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4530-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f4530-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4530-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4530-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4530-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4530-108">DESCRIPTION</span></span>
<span data-ttu-id="f4530-109">Ottiene i dettagli di un evento Hub NetwrokruleSet dello spazio dei nomi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="f4530-109">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f4530-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4530-110">EXAMPLES</span></span>

### <span data-ttu-id="f4530-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4530-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="f4530-112">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="f4530-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f4530-113">Ottenere i dettagli degli hub degli eventi NetwrokruleSet dello spazio dei nomi usando i parametri ResourceGroup e Namesape.</span><span class="sxs-lookup"><span data-stu-id="f4530-113">Get the details of Event Hubs NetwrokruleSet of namespace using ResourceGroup and Namesape parameters.</span></span> 

### <span data-ttu-id="f4530-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f4530-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="f4530-115">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="f4530-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f4530-116">Ottenere i dettagli degli hub degli eventi NetwrokruleSet dello spazio dei nomi usando lo spazio dei nomi che si trova nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f4530-116">Get the details of Event Hubs NetwrokruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="f4530-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f4530-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="f4530-118">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="f4530-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f4530-119">Ottenere i dettagli degli hub degli eventi NetwrokruleSet dello spazio dei nomi usando l'ID risorsa di altri spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="f4530-119">Get the details of Event Hubs NetwrokruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="f4530-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4530-120">PARAMETERS</span></span>

### <span data-ttu-id="f4530-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4530-121">-DefaultProfile</span></span>
<span data-ttu-id="f4530-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4530-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4530-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f4530-123">-Namespace</span></span>
<span data-ttu-id="f4530-124">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f4530-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4530-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4530-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4530-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f4530-126">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4530-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4530-127">-ResourceId</span></span>
<span data-ttu-id="f4530-128">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f4530-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f4530-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4530-129">CommonParameters</span></span>
<span data-ttu-id="f4530-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4530-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f4530-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4530-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4530-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4530-132">INPUTS</span></span>

### <span data-ttu-id="f4530-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f4530-133">System.String</span></span>

## <span data-ttu-id="f4530-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4530-134">OUTPUTS</span></span>

### <span data-ttu-id="f4530-135">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f4530-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f4530-136">Note</span><span class="sxs-lookup"><span data-stu-id="f4530-136">NOTES</span></span>

## <span data-ttu-id="f4530-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4530-137">RELATED LINKS</span></span>