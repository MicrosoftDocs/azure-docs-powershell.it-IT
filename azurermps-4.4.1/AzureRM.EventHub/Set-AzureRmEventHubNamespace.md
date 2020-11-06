---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510620"
---
# <span data-ttu-id="f397c-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f397c-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="f397c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f397c-102">SYNOPSIS</span></span>
<span data-ttu-id="f397c-103">Aggiorna lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="f397c-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f397c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f397c-104">SYNTAX</span></span>

### <span data-ttu-id="f397c-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f397c-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f397c-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="f397c-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f397c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f397c-107">DESCRIPTION</span></span>
<span data-ttu-id="f397c-108">Il cmdlet Set-AzureRmEventHubNamespace aggiorna le proprietà dello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="f397c-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="f397c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f397c-109">EXAMPLES</span></span>

### <span data-ttu-id="f397c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f397c-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="f397c-111">Aggiorna lo stato dello spazio dei nomi NamespaceName \` \` in created.</span><span class="sxs-lookup"><span data-stu-id="f397c-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="f397c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f397c-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="f397c-113">Aggiorna lo stato dello spazio dei nomi MyNamespace \` \` con AutoInflate = Enabled e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="f397c-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="f397c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f397c-114">PARAMETERS</span></span>

### <span data-ttu-id="f397c-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f397c-115">-Location</span></span>
<span data-ttu-id="f397c-116">Area geografica dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="f397c-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="f397c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f397c-117">-ResourceGroupName</span></span>
<span data-ttu-id="f397c-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f397c-118">Resource group name.</span></span>

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

### <span data-ttu-id="f397c-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f397c-119">-SkuCapacity</span></span>
<span data-ttu-id="f397c-120">Unità di throughput dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="f397c-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="f397c-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f397c-121">-SkuName</span></span>
<span data-ttu-id="f397c-122">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f397c-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f397c-123">-Stato</span><span class="sxs-lookup"><span data-stu-id="f397c-123">-State</span></span>
<span data-ttu-id="f397c-124">Specifica lo stato (disattivato o abilitato) dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f397c-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f397c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f397c-125">-Tag</span></span>
<span data-ttu-id="f397c-126">Hashtable che rappresentano i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f397c-126">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="f397c-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f397c-127">-Confirm</span></span>
<span data-ttu-id="f397c-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f397c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f397c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f397c-129">-WhatIf</span></span>
<span data-ttu-id="f397c-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f397c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f397c-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f397c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f397c-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="f397c-132">-EnableAutoInflate</span></span>
<span data-ttu-id="f397c-133">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="f397c-133">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="f397c-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="f397c-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="f397c-135">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, vaule deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="f397c-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="f397c-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="f397c-136">-Name</span></span>
<span data-ttu-id="f397c-137">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="f397c-137">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="f397c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f397c-138">INPUTS</span></span>

### <span data-ttu-id="f397c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f397c-139">System.String</span></span>

### <span data-ttu-id="f397c-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f397c-140">System.Int32</span></span>

### <span data-ttu-id="f397c-141">Microsoft. Azure. Management. EventHub. Models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="f397c-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="f397c-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f397c-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f397c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f397c-143">OUTPUTS</span></span>

### <span data-ttu-id="f397c-144">Microsoft. Azure. Commands. EventHub. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f397c-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="f397c-145">Note</span><span class="sxs-lookup"><span data-stu-id="f397c-145">NOTES</span></span>

## <span data-ttu-id="f397c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f397c-146">RELATED LINKS</span></span>

