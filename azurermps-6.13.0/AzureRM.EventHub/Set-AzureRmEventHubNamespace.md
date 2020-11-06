---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6fd3f000f7c91f0475cd18802dd6a9d096d35f5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518667"
---
# <span data-ttu-id="606a5-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="606a5-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="606a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="606a5-102">SYNOPSIS</span></span>
<span data-ttu-id="606a5-103">Aggiorna lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="606a5-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="606a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="606a5-104">SYNTAX</span></span>

### <span data-ttu-id="606a5-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="606a5-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="606a5-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="606a5-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="606a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="606a5-107">DESCRIPTION</span></span>
<span data-ttu-id="606a5-108">Il cmdlet Set-AzureRmEventHubNamespace aggiorna le proprietà dello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="606a5-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="606a5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="606a5-109">EXAMPLES</span></span>

### <span data-ttu-id="606a5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="606a5-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="606a5-111">Aggiorna lo stato dello spazio dei nomi NamespaceName \` \` in created.</span><span class="sxs-lookup"><span data-stu-id="606a5-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="606a5-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="606a5-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="606a5-113">Aggiorna lo stato dello spazio dei nomi MyNamespace \` \` con AutoInflate = Enabled e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="606a5-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="606a5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="606a5-114">PARAMETERS</span></span>

### <span data-ttu-id="606a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606a5-115">-DefaultProfile</span></span>
<span data-ttu-id="606a5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="606a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="606a5-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="606a5-117">-EnableAutoInflate</span></span>
<span data-ttu-id="606a5-118">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="606a5-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="606a5-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="606a5-119">-Location</span></span>
<span data-ttu-id="606a5-120">Posizione dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="606a5-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="606a5-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="606a5-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="606a5-122">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, il valore deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="606a5-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="606a5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="606a5-123">-Name</span></span>
<span data-ttu-id="606a5-124">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="606a5-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="606a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="606a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="606a5-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="606a5-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="606a5-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="606a5-127">-SkuCapacity</span></span>
<span data-ttu-id="606a5-128">Unità throughput eventhub.</span><span class="sxs-lookup"><span data-stu-id="606a5-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="606a5-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="606a5-129">-SkuName</span></span>
<span data-ttu-id="606a5-130">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="606a5-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="606a5-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="606a5-131">-State</span></span>
<span data-ttu-id="606a5-132">Disabilitare/abilitare lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="606a5-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="606a5-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="606a5-133">-Tag</span></span>
<span data-ttu-id="606a5-134">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="606a5-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="606a5-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="606a5-135">-Confirm</span></span>
<span data-ttu-id="606a5-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="606a5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="606a5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="606a5-137">-WhatIf</span></span>
<span data-ttu-id="606a5-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="606a5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="606a5-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="606a5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="606a5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606a5-140">CommonParameters</span></span>
<span data-ttu-id="606a5-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="606a5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606a5-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="606a5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606a5-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="606a5-143">INPUTS</span></span>

### <span data-ttu-id="606a5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="606a5-144">System.String</span></span>

### <span data-ttu-id="606a5-145">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="606a5-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="606a5-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceState, Microsoft. Azure. Commands. EventHub, Version = 0.6.7.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="606a5-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.6.7.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="606a5-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="606a5-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="606a5-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="606a5-148">OUTPUTS</span></span>

### <span data-ttu-id="606a5-149">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="606a5-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="606a5-150">Note</span><span class="sxs-lookup"><span data-stu-id="606a5-150">NOTES</span></span>

## <span data-ttu-id="606a5-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="606a5-151">RELATED LINKS</span></span>
