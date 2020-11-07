---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 9217dfa2d5465841cb0ed33c2781849ddebff3b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674433"
---
# <span data-ttu-id="a459a-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a459a-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="a459a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a459a-102">SYNOPSIS</span></span>
<span data-ttu-id="a459a-103">Crea uno spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="a459a-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="a459a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a459a-104">SYNTAX</span></span>

### <span data-ttu-id="a459a-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a459a-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a459a-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="a459a-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a459a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a459a-107">DESCRIPTION</span></span>
<span data-ttu-id="a459a-108">Il cmdlet New-AzEventHubNamespace crea un nuovo spazio dei nomi di tipo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="a459a-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="a459a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a459a-109">EXAMPLES</span></span>

### <span data-ttu-id="a459a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a459a-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="a459a-111">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a459a-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a459a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a459a-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="a459a-113">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` e AutoInflate è abilitato con MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="a459a-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="a459a-114">Esempio di spazio dei nomi abilitato 3-Kafka</span><span class="sxs-lookup"><span data-stu-id="a459a-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="a459a-115">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` con Kafka e AutoInflate abilitato.</span><span class="sxs-lookup"><span data-stu-id="a459a-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="a459a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a459a-116">PARAMETERS</span></span>

### <span data-ttu-id="a459a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a459a-117">-DefaultProfile</span></span>
<span data-ttu-id="a459a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a459a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a459a-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="a459a-119">-EnableAutoInflate</span></span>
<span data-ttu-id="a459a-120">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="a459a-120">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a459a-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="a459a-121">-EnableKafka</span></span>
<span data-ttu-id="a459a-122">Abilitazione o disabilitazione di Kafka per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a459a-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="a459a-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a459a-123">-Location</span></span>
<span data-ttu-id="a459a-124">Posizione dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="a459a-124">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a459a-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="a459a-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="a459a-126">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, il valore deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="a459a-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a459a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a459a-127">-Name</span></span>
<span data-ttu-id="a459a-128">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="a459a-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="a459a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a459a-129">-ResourceGroupName</span></span>
<span data-ttu-id="a459a-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a459a-130">Resource Group Name</span></span>

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

### <span data-ttu-id="a459a-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a459a-131">-SkuCapacity</span></span>
<span data-ttu-id="a459a-132">Unità throughput eventhub.</span><span class="sxs-lookup"><span data-stu-id="a459a-132">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a459a-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a459a-133">-SkuName</span></span>
<span data-ttu-id="a459a-134">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a459a-134">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a459a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a459a-135">-Tag</span></span>
<span data-ttu-id="a459a-136">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a459a-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a459a-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a459a-137">-Confirm</span></span>
<span data-ttu-id="a459a-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a459a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a459a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a459a-139">-WhatIf</span></span>
<span data-ttu-id="a459a-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a459a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a459a-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a459a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a459a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a459a-142">CommonParameters</span></span>
<span data-ttu-id="a459a-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a459a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a459a-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a459a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a459a-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a459a-145">INPUTS</span></span>

### <span data-ttu-id="a459a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a459a-146">System.String</span></span>

### <span data-ttu-id="a459a-147">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a459a-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a459a-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a459a-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a459a-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a459a-149">OUTPUTS</span></span>

### <span data-ttu-id="a459a-150">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a459a-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a459a-151">Note</span><span class="sxs-lookup"><span data-stu-id="a459a-151">NOTES</span></span>

## <span data-ttu-id="a459a-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a459a-152">RELATED LINKS</span></span>