---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 0fb90529f4157bf627e43477e3db41764040e5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686402"
---
# <span data-ttu-id="c3bfe-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c3bfe-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="c3bfe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="c3bfe-103">Crea uno spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3bfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3bfe-104">SYNTAX</span></span>

### <span data-ttu-id="c3bfe-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3bfe-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3bfe-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3bfe-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3bfe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3bfe-107">DESCRIPTION</span></span>
<span data-ttu-id="c3bfe-108">Il cmdlet New-AzureRmEventHubNamespace crea un nuovo spazio dei nomi di tipo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="c3bfe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3bfe-109">EXAMPLES</span></span>

### <span data-ttu-id="c3bfe-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3bfe-110">Example 1</span></span>                                              
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="c3bfe-111">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c3bfe-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c3bfe-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c3bfe-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="c3bfe-113">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` e AutoInflate è abilitato con MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="c3bfe-114">Esempio di spazio dei nomi abilitato 3-Kafka</span><span class="sxs-lookup"><span data-stu-id="c3bfe-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="c3bfe-115">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` con Kafka e AutoInflate abilitato.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="c3bfe-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3bfe-116">PARAMETERS</span></span>

### <span data-ttu-id="c3bfe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3bfe-117">-DefaultProfile</span></span>
<span data-ttu-id="c3bfe-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bfe-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="c3bfe-119">-EnableAutoInflate</span></span>
<span data-ttu-id="c3bfe-120">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="c3bfe-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="c3bfe-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="c3bfe-121">-EnableKafka</span></span>
<span data-ttu-id="c3bfe-122">Abilitazione o disabilitazione di Kafka per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3bfe-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```         

### <span data-ttu-id="c3bfe-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c3bfe-123">-Location</span></span>
<span data-ttu-id="c3bfe-124">Posizione dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="c3bfe-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="c3bfe-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="c3bfe-126">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, il valore deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="c3bfe-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3bfe-127">-Name</span></span>
<span data-ttu-id="c3bfe-128">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="c3bfe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3bfe-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3bfe-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c3bfe-130">Resource Group Name</span></span>

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

### <span data-ttu-id="c3bfe-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c3bfe-131">-SkuCapacity</span></span>
<span data-ttu-id="c3bfe-132">Unità throughput eventhub.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="c3bfe-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c3bfe-133">-SkuName</span></span>
<span data-ttu-id="c3bfe-134">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="c3bfe-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3bfe-135">-Tag</span></span>
<span data-ttu-id="c3bfe-136">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="c3bfe-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3bfe-137">-Confirm</span></span>
<span data-ttu-id="c3bfe-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3bfe-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3bfe-139">-WhatIf</span></span>
<span data-ttu-id="c3bfe-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3bfe-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3bfe-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3bfe-142">CommonParameters</span></span>
<span data-ttu-id="c3bfe-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3bfe-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c3bfe-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3bfe-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3bfe-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3bfe-145">INPUTS</span></span>


## <span data-ttu-id="c3bfe-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3bfe-146">OUTPUTS</span></span>

### <span data-ttu-id="c3bfe-147">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c3bfe-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="c3bfe-148">Note</span><span class="sxs-lookup"><span data-stu-id="c3bfe-148">NOTES</span></span>

## <span data-ttu-id="c3bfe-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3bfe-149">RELATED LINKS</span></span>
