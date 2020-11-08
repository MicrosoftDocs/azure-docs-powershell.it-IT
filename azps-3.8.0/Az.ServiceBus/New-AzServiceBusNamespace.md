---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021676"
---
# <span data-ttu-id="feca0-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="feca0-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="feca0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="feca0-102">SYNOPSIS</span></span>
<span data-ttu-id="feca0-103">Crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="feca0-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="feca0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="feca0-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feca0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="feca0-105">DESCRIPTION</span></span>
<span data-ttu-id="feca0-106">Il cmdlet **New-AzServiceBusNamespace** crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="feca0-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="feca0-107">Una volta creato, il manifesto delle risorse dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="feca0-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="feca0-108">Questa operazione è idempotente.</span><span class="sxs-lookup"><span data-stu-id="feca0-108">This operation is idempotent.</span></span>

## <span data-ttu-id="feca0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="feca0-109">EXAMPLES</span></span>

### <span data-ttu-id="feca0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="feca0-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="feca0-111">Crea un nuovo spazio dei nomi Service Bus all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="feca0-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="feca0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="feca0-112">PARAMETERS</span></span>

### <span data-ttu-id="feca0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feca0-113">-DefaultProfile</span></span>
<span data-ttu-id="feca0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="feca0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feca0-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="feca0-115">-Location</span></span>
<span data-ttu-id="feca0-116">Posizione dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="feca0-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="feca0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="feca0-117">-Name</span></span>
<span data-ttu-id="feca0-118">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="feca0-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="feca0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feca0-119">-ResourceGroupName</span></span>
<span data-ttu-id="feca0-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="feca0-120">The resource group name.</span></span>

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

### <span data-ttu-id="feca0-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="feca0-121">-SkuCapacity</span></span>
<span data-ttu-id="feca0-122">Unità throughput dello spazio dei nomi Service Bus Premium, valori consentiti 1 o 2 o 4</span><span class="sxs-lookup"><span data-stu-id="feca0-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="feca0-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="feca0-123">-SkuName</span></span>
<span data-ttu-id="feca0-124">Nome del SKU dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="feca0-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="feca0-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="feca0-125">-Tag</span></span>
<span data-ttu-id="feca0-126">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="feca0-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="feca0-127">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="feca0-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="feca0-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="feca0-128">-Confirm</span></span>
<span data-ttu-id="feca0-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feca0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feca0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feca0-130">-WhatIf</span></span>
<span data-ttu-id="feca0-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="feca0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="feca0-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="feca0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feca0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feca0-133">CommonParameters</span></span>
<span data-ttu-id="feca0-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feca0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feca0-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feca0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feca0-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="feca0-136">INPUTS</span></span>

### <span data-ttu-id="feca0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="feca0-137">System.String</span></span>

### <span data-ttu-id="feca0-138">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="feca0-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="feca0-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="feca0-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="feca0-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="feca0-140">OUTPUTS</span></span>

### <span data-ttu-id="feca0-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="feca0-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="feca0-142">Note</span><span class="sxs-lookup"><span data-stu-id="feca0-142">NOTES</span></span>

## <span data-ttu-id="feca0-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="feca0-143">RELATED LINKS</span></span>
