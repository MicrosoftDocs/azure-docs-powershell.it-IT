---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678767"
---
# <span data-ttu-id="fcee2-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fcee2-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="fcee2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fcee2-102">SYNOPSIS</span></span>
<span data-ttu-id="fcee2-103">Aggiorna lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="fcee2-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="fcee2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fcee2-104">SYNTAX</span></span>

### <span data-ttu-id="fcee2-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fcee2-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcee2-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcee2-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcee2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcee2-107">DESCRIPTION</span></span>
<span data-ttu-id="fcee2-108">Il cmdlet Set-AzEventHubNamespace aggiorna le proprietà dello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="fcee2-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="fcee2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fcee2-109">EXAMPLES</span></span>

### <span data-ttu-id="fcee2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fcee2-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="fcee2-111">Aggiorna lo stato dello spazio dei nomi NamespaceName \` \` in created.</span><span class="sxs-lookup"><span data-stu-id="fcee2-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="fcee2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fcee2-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="fcee2-113">Aggiorna lo stato dello spazio dei nomi MyNamespace \` \` con AutoInflate = Enabled e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="fcee2-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="fcee2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fcee2-114">PARAMETERS</span></span>

### <span data-ttu-id="fcee2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcee2-115">-DefaultProfile</span></span>
<span data-ttu-id="fcee2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fcee2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcee2-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="fcee2-117">-EnableAutoInflate</span></span>
<span data-ttu-id="fcee2-118">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="fcee2-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="fcee2-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fcee2-119">-Location</span></span>
<span data-ttu-id="fcee2-120">Posizione dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="fcee2-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="fcee2-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="fcee2-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="fcee2-122">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, il valore deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="fcee2-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="fcee2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcee2-123">-Name</span></span>
<span data-ttu-id="fcee2-124">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="fcee2-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="fcee2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcee2-125">-ResourceGroupName</span></span>
<span data-ttu-id="fcee2-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fcee2-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcee2-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fcee2-127">-SkuCapacity</span></span>
<span data-ttu-id="fcee2-128">Unità throughput eventhub.</span><span class="sxs-lookup"><span data-stu-id="fcee2-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="fcee2-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fcee2-129">-SkuName</span></span>
<span data-ttu-id="fcee2-130">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fcee2-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="fcee2-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="fcee2-131">-State</span></span>
<span data-ttu-id="fcee2-132">Disabilitare/abilitare lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fcee2-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="fcee2-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="fcee2-133">-Tag</span></span>
<span data-ttu-id="fcee2-134">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="fcee2-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="fcee2-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fcee2-135">-Confirm</span></span>
<span data-ttu-id="fcee2-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcee2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcee2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcee2-137">-WhatIf</span></span>
<span data-ttu-id="fcee2-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcee2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcee2-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcee2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcee2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcee2-140">CommonParameters</span></span>
<span data-ttu-id="fcee2-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcee2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcee2-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcee2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcee2-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fcee2-143">INPUTS</span></span>

### <span data-ttu-id="fcee2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fcee2-144">System.String</span></span>

### <span data-ttu-id="fcee2-145">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fcee2-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fcee2-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. Cmdlets. EventHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fcee2-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="fcee2-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fcee2-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fcee2-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fcee2-148">OUTPUTS</span></span>

### <span data-ttu-id="fcee2-149">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fcee2-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="fcee2-150">Note</span><span class="sxs-lookup"><span data-stu-id="fcee2-150">NOTES</span></span>

## <span data-ttu-id="fcee2-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fcee2-151">RELATED LINKS</span></span>
