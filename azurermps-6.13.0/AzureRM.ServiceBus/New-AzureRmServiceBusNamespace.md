---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 532135578418a90e9ce6887602723c2165f28aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518556"
---
# <span data-ttu-id="e7aa9-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="e7aa9-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="e7aa9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="e7aa9-103">Crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7aa9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7aa9-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7aa9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7aa9-105">DESCRIPTION</span></span>
<span data-ttu-id="e7aa9-106">Il cmdlet **New-AzureRmServiceBusNamespace** crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="e7aa9-107">Una volta creato, il manifesto delle risorse dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="e7aa9-108">Questa operazione è idempotente.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-108">This operation is idempotent.</span></span>

## <span data-ttu-id="e7aa9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7aa9-109">EXAMPLES</span></span>

### <span data-ttu-id="e7aa9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e7aa9-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="e7aa9-111">Crea un nuovo spazio dei nomi Service Bus all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="e7aa9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7aa9-112">PARAMETERS</span></span>

### <span data-ttu-id="e7aa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7aa9-113">-DefaultProfile</span></span>
<span data-ttu-id="e7aa9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7aa9-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e7aa9-115">-Location</span></span>
<span data-ttu-id="e7aa9-116">Posizione dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-116">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7aa9-117">-Name</span></span>
<span data-ttu-id="e7aa9-118">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7aa9-119">-ResourceGroupName</span></span>
<span data-ttu-id="e7aa9-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa9-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e7aa9-121">-SkuCapacity</span></span>
<span data-ttu-id="e7aa9-122">Unità throughput dello spazio dei nomi Service Bus Premium, valori consentiti 1 o 2 o 4</span><span class="sxs-lookup"><span data-stu-id="e7aa9-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa9-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e7aa9-123">-SkuName</span></span>
<span data-ttu-id="e7aa9-124">Nome del SKU dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e7aa9-125">-Tag</span></span>
<span data-ttu-id="e7aa9-126">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="e7aa9-127">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e7aa9-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa9-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e7aa9-128">-Confirm</span></span>
<span data-ttu-id="e7aa9-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7aa9-130">-WhatIf</span></span>
<span data-ttu-id="e7aa9-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7aa9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7aa9-133">CommonParameters</span></span>
<span data-ttu-id="e7aa9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7aa9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7aa9-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7aa9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7aa9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7aa9-136">INPUTS</span></span>

### <span data-ttu-id="e7aa9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e7aa9-137">System.String</span></span>

### <span data-ttu-id="e7aa9-138">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e7aa9-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e7aa9-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e7aa9-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e7aa9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7aa9-140">OUTPUTS</span></span>

### <span data-ttu-id="e7aa9-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e7aa9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e7aa9-142">Note</span><span class="sxs-lookup"><span data-stu-id="e7aa9-142">NOTES</span></span>

## <span data-ttu-id="e7aa9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7aa9-143">RELATED LINKS</span></span>
