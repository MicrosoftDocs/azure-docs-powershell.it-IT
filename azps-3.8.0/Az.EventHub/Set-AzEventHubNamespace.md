---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 5717728fa868094a5d1d170af948743d1b9e065b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864465"
---
# <span data-ttu-id="b1857-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b1857-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="b1857-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1857-102">SYNOPSIS</span></span>
<span data-ttu-id="b1857-103">Aggiorna lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="b1857-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b1857-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1857-104">SYNTAX</span></span>

### <span data-ttu-id="b1857-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1857-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1857-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1857-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1857-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1857-107">DESCRIPTION</span></span>
<span data-ttu-id="b1857-108">Il cmdlet Set-AzEventHubNamespace aggiorna le proprietà dello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="b1857-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b1857-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1857-109">EXAMPLES</span></span>

### <span data-ttu-id="b1857-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1857-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="b1857-111">Aggiorna i tag per lo spazio dei nomi NamespaceName \` \` in created.</span><span class="sxs-lookup"><span data-stu-id="b1857-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="b1857-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b1857-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
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
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="b1857-113">Aggiorna lo stato dello spazio dei nomi MyNamespace \` \` con AutoInflate = Enabled e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="b1857-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="b1857-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1857-114">PARAMETERS</span></span>

### <span data-ttu-id="b1857-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1857-115">-DefaultProfile</span></span>
<span data-ttu-id="b1857-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1857-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1857-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="b1857-117">-EnableAutoInflate</span></span>
<span data-ttu-id="b1857-118">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="b1857-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="b1857-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="b1857-119">-EnableKafka</span></span>
<span data-ttu-id="b1857-120">Abilitazione o disabilitazione di Kafka per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1857-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="b1857-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b1857-121">-Location</span></span>
<span data-ttu-id="b1857-122">Posizione dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="b1857-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="b1857-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="b1857-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="b1857-124">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, il valore deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="b1857-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1857-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1857-125">-Name</span></span>
<span data-ttu-id="b1857-126">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="b1857-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="b1857-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1857-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1857-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1857-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1857-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b1857-129">-SkuCapacity</span></span>
<span data-ttu-id="b1857-130">Unità throughput eventhub.</span><span class="sxs-lookup"><span data-stu-id="b1857-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="b1857-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b1857-131">-SkuName</span></span>
<span data-ttu-id="b1857-132">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b1857-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="b1857-133">-Stato</span><span class="sxs-lookup"><span data-stu-id="b1857-133">-State</span></span>
<span data-ttu-id="b1857-134">Disabilitare/abilitare lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b1857-134">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1857-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1857-135">-Tag</span></span>
<span data-ttu-id="b1857-136">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b1857-136">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1857-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1857-137">-Confirm</span></span>
<span data-ttu-id="b1857-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1857-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1857-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1857-139">-WhatIf</span></span>
<span data-ttu-id="b1857-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1857-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1857-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1857-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1857-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1857-142">CommonParameters</span></span>
<span data-ttu-id="b1857-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1857-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1857-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1857-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1857-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1857-145">INPUTS</span></span>

### <span data-ttu-id="b1857-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b1857-146">System.String</span></span>

### <span data-ttu-id="b1857-147">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b1857-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b1857-148">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. Cmdlets. EventHub, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b1857-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b1857-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b1857-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b1857-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1857-150">OUTPUTS</span></span>

### <span data-ttu-id="b1857-151">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b1857-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b1857-152">Note</span><span class="sxs-lookup"><span data-stu-id="b1857-152">NOTES</span></span>

## <span data-ttu-id="b1857-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1857-153">RELATED LINKS</span></span>
