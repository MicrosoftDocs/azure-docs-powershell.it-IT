---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208178"
---
# <span data-ttu-id="8c8a1-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c8a1-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="8c8a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8a1-103">Recupera i dettagli di un set di regole di rete per gli hub eventi dello spazio dei nomi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="8c8a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c8a1-104">SYNTAX</span></span>

### <span data-ttu-id="8c8a1-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8a1-106">NetworkRuleSetPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8c8a1-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8a1-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c8a1-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c8a1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8c8a1-108">DESCRIPTION</span></span>
<span data-ttu-id="8c8a1-109">Recupera i dettagli di un set di regole di rete per gli hub eventi dello spazio dei nomi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="8c8a1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c8a1-110">EXAMPLES</span></span>

### <span data-ttu-id="8c8a1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8c8a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="8c8a1-112">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="8c8a1-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8c8a1-113">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando i parametri ResourceGroup e Namespace.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="8c8a1-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8c8a1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="8c8a1-115">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="8c8a1-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8c8a1-116">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando Spazio dei nomi, che si trova nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="8c8a1-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8c8a1-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="8c8a1-118">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="8c8a1-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8c8a1-119">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando ID risorsa di altro spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c8a1-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="8c8a1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c8a1-120">PARAMETERS</span></span>

### <span data-ttu-id="8c8a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8a1-121">-DefaultProfile</span></span>
<span data-ttu-id="8c8a1-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c8a1-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c8a1-123">-Namespace</span></span>
<span data-ttu-id="8c8a1-124">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c8a1-124">Namespace Name</span></span>

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

### <span data-ttu-id="8c8a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c8a1-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8c8a1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8c8a1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c8a1-127">-ResourceId</span></span>
<span data-ttu-id="8c8a1-128">ID risorsa spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c8a1-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="8c8a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8a1-129">CommonParameters</span></span>
<span data-ttu-id="8c8a1-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8c8a1-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c8a1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8a1-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="8c8a1-132">INPUTS</span></span>

### <span data-ttu-id="8c8a1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8c8a1-133">System.String</span></span>

## <span data-ttu-id="8c8a1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c8a1-134">OUTPUTS</span></span>

### <span data-ttu-id="8c8a1-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="8c8a1-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="8c8a1-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="8c8a1-136">NOTES</span></span>

## <span data-ttu-id="8c8a1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c8a1-137">RELATED LINKS</span></span>