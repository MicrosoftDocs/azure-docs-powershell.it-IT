---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519007"
---
# <span data-ttu-id="b96a1-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b96a1-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="b96a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b96a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b96a1-103">Crea uno spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="b96a1-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b96a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b96a1-104">SYNTAX</span></span>

### <span data-ttu-id="b96a1-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b96a1-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96a1-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="b96a1-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b96a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b96a1-107">DESCRIPTION</span></span>
<span data-ttu-id="b96a1-108">Il cmdlet New-AzureRmEventHubNamespace crea un nuovo spazio dei nomi di tipo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="b96a1-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="b96a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b96a1-109">EXAMPLES</span></span>

### <span data-ttu-id="b96a1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b96a1-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="b96a1-111">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b96a1-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b96a1-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b96a1-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="b96a1-113">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` e AutoInflate è abilitato con MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="b96a1-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="b96a1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b96a1-114">PARAMETERS</span></span>

### <span data-ttu-id="b96a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96a1-115">-DefaultProfile</span></span>
<span data-ttu-id="b96a1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b96a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96a1-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="b96a1-117">-EnableAutoInflate</span></span>
<span data-ttu-id="b96a1-118">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="b96a1-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96a1-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b96a1-119">-Location</span></span>
<span data-ttu-id="b96a1-120">Posizione dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="b96a1-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="b96a1-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="b96a1-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="b96a1-122">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, il valore deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="b96a1-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96a1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b96a1-123">-Name</span></span>
<span data-ttu-id="b96a1-124">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="b96a1-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="b96a1-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b96a1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b96a1-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b96a1-127">-SkuCapacity</span></span>
<span data-ttu-id="b96a1-128">Unità throughput eventhub.</span><span class="sxs-lookup"><span data-stu-id="b96a1-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96a1-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b96a1-129">-SkuName</span></span>
<span data-ttu-id="b96a1-130">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b96a1-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="b96a1-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="b96a1-131">-Tag</span></span>
<span data-ttu-id="b96a1-132">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b96a1-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96a1-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b96a1-133">-Confirm</span></span>
<span data-ttu-id="b96a1-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b96a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b96a1-135">-WhatIf</span></span>
<span data-ttu-id="b96a1-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b96a1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b96a1-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b96a1-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96a1-138">CommonParameters</span></span>
<span data-ttu-id="b96a1-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b96a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b96a1-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b96a1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96a1-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b96a1-141">INPUTS</span></span>

### <span data-ttu-id="b96a1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b96a1-142">System.String</span></span>
<span data-ttu-id="b96a1-143">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b96a1-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="b96a1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b96a1-144">OUTPUTS</span></span>

### <span data-ttu-id="b96a1-145">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b96a1-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="b96a1-146">Note</span><span class="sxs-lookup"><span data-stu-id="b96a1-146">NOTES</span></span>

## <span data-ttu-id="b96a1-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b96a1-147">RELATED LINKS</span></span>
