---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688316"
---
# <span data-ttu-id="4565d-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4565d-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="4565d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4565d-102">SYNOPSIS</span></span>
<span data-ttu-id="4565d-103">Crea uno spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="4565d-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4565d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4565d-104">SYNTAX</span></span>

### <span data-ttu-id="4565d-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4565d-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4565d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="4565d-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4565d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4565d-107">DESCRIPTION</span></span>
<span data-ttu-id="4565d-108">Il cmdlet New-AzureRmEventHubNamespace crea un nuovo spazio dei nomi di tipo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="4565d-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="4565d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4565d-109">EXAMPLES</span></span>

### <span data-ttu-id="4565d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4565d-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="4565d-111">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4565d-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4565d-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4565d-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="4565d-113">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` e AutoInflate è abilitato con MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="4565d-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="4565d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4565d-114">PARAMETERS</span></span>

### <span data-ttu-id="4565d-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4565d-115">-Location</span></span>
<span data-ttu-id="4565d-116">Area geografica dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="4565d-116">Event Hubs namespace geo-location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4565d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4565d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4565d-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4565d-118">Resource group name.</span></span>

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

### <span data-ttu-id="4565d-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4565d-119">-SkuCapacity</span></span>
<span data-ttu-id="4565d-120">Unità di throughput dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="4565d-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4565d-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4565d-121">-SkuName</span></span>
<span data-ttu-id="4565d-122">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4565d-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4565d-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="4565d-123">-Tag</span></span>
<span data-ttu-id="4565d-124">Hashtable che rappresentano i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4565d-124">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4565d-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4565d-125">-Confirm</span></span>
<span data-ttu-id="4565d-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4565d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4565d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4565d-127">-WhatIf</span></span>
<span data-ttu-id="4565d-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4565d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4565d-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4565d-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4565d-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="4565d-130">-EnableAutoInflate</span></span>
<span data-ttu-id="4565d-131">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="4565d-131">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4565d-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="4565d-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="4565d-133">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, vaule deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="4565d-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4565d-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="4565d-134">-Name</span></span>
<span data-ttu-id="4565d-135">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="4565d-135">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="4565d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4565d-136">INPUTS</span></span>

### <span data-ttu-id="4565d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4565d-137">System.String</span></span>
<span data-ttu-id="4565d-138">System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4565d-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="4565d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4565d-139">OUTPUTS</span></span>

### <span data-ttu-id="4565d-140">Microsoft. Azure. Commands. EventHub. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4565d-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="4565d-141">Note</span><span class="sxs-lookup"><span data-stu-id="4565d-141">NOTES</span></span>

## <span data-ttu-id="4565d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4565d-142">RELATED LINKS</span></span>

