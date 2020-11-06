---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520761"
---
# <span data-ttu-id="52fc1-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="52fc1-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="52fc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="52fc1-103">Crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="52fc1-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52fc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52fc1-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52fc1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="52fc1-106">Il cmdlet **New-AzureRmServiceBusNamespace** crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="52fc1-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="52fc1-107">Una volta creato, il manifesto delle risorse dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="52fc1-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="52fc1-108">Questa operazione è idempotente.</span><span class="sxs-lookup"><span data-stu-id="52fc1-108">This operation is idempotent.</span></span>

## <span data-ttu-id="52fc1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52fc1-109">EXAMPLES</span></span>

### <span data-ttu-id="52fc1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52fc1-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="52fc1-111">Crea un nuovo spazio dei nomi Service Bus all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="52fc1-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="52fc1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52fc1-112">PARAMETERS</span></span>

### <span data-ttu-id="52fc1-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="52fc1-113">-Location</span></span>
<span data-ttu-id="52fc1-114">Posizione dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="52fc1-114">The Service Bus namespace location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52fc1-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="52fc1-115">-NamespaceName</span></span>
<span data-ttu-id="52fc1-116">Nome dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="52fc1-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="52fc1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52fc1-117">-ResourceGroupName</span></span>
<span data-ttu-id="52fc1-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52fc1-118">The resource group name.</span></span>

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

### <span data-ttu-id="52fc1-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="52fc1-119">-SkuName</span></span>
<span data-ttu-id="52fc1-120">Nome del SKU dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="52fc1-120">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="52fc1-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="52fc1-121">-Tag</span></span>
<span data-ttu-id="52fc1-122">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="52fc1-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="52fc1-123">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="52fc1-123">For example:</span></span>

<span data-ttu-id="52fc1-124">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="52fc1-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="52fc1-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52fc1-125">-Confirm</span></span>
<span data-ttu-id="52fc1-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fc1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52fc1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52fc1-127">-WhatIf</span></span>
<span data-ttu-id="52fc1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52fc1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52fc1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52fc1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52fc1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fc1-130">CommonParameters</span></span>
<span data-ttu-id="52fc1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fc1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fc1-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52fc1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fc1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52fc1-133">INPUTS</span></span>

### <span data-ttu-id="52fc1-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52fc1-134">-ResourceGroup</span></span>
 <span data-ttu-id="52fc1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="52fc1-135">System.String</span></span>

### <span data-ttu-id="52fc1-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="52fc1-136">-NamespaceName</span></span>
 <span data-ttu-id="52fc1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="52fc1-137">System.String</span></span>

### <span data-ttu-id="52fc1-138">-Posizione</span><span class="sxs-lookup"><span data-stu-id="52fc1-138">-Location</span></span>
 <span data-ttu-id="52fc1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="52fc1-139">System.String</span></span>

### <span data-ttu-id="52fc1-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="52fc1-140">-SkuName</span></span>
 <span data-ttu-id="52fc1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="52fc1-141">System.String</span></span>

### <span data-ttu-id="52fc1-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="52fc1-142">-Tag</span></span>
 <span data-ttu-id="52fc1-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="52fc1-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="52fc1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52fc1-144">OUTPUTS</span></span>

### <span data-ttu-id="52fc1-145">Microsoft. Azure. Commands. ServiceBus. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="52fc1-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="52fc1-146">Note</span><span class="sxs-lookup"><span data-stu-id="52fc1-146">NOTES</span></span>

## <span data-ttu-id="52fc1-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52fc1-147">RELATED LINKS</span></span>
