---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: e3e262bee01306eacfdde8b97b13c0ba2a35b745
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960094"
---
# <span data-ttu-id="67183-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="67183-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="67183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67183-102">SYNOPSIS</span></span>
<span data-ttu-id="67183-103">Crea un nuovo spazio dei nomi del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="67183-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="67183-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67183-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67183-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67183-105">DESCRIPTION</span></span>
<span data-ttu-id="67183-106">Il cmdlet **New-AzServiceBus Pull crea** un nuovo spazio dei nomi del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="67183-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="67183-107">Una volta creato, il manifesto della risorsa dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="67183-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="67183-108">Questa operazione è stata identificata come idempotente.</span><span class="sxs-lookup"><span data-stu-id="67183-108">This operation is idempotent.</span></span>

## <span data-ttu-id="67183-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67183-109">EXAMPLES</span></span>

### <span data-ttu-id="67183-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67183-110">Example 1</span></span>
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

<span data-ttu-id="67183-111">Crea un nuovo spazio dei nomi bus di servizio all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="67183-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="67183-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67183-112">PARAMETERS</span></span>

### <span data-ttu-id="67183-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67183-113">-DefaultProfile</span></span>
<span data-ttu-id="67183-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67183-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67183-115">-Location</span><span class="sxs-lookup"><span data-stu-id="67183-115">-Location</span></span>
<span data-ttu-id="67183-116">Posizione dello spazio dei nomi del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="67183-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="67183-117">-Name</span><span class="sxs-lookup"><span data-stu-id="67183-117">-Name</span></span>
<span data-ttu-id="67183-118">Nome spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="67183-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="67183-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67183-119">-ResourceGroupName</span></span>
<span data-ttu-id="67183-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67183-120">The resource group name.</span></span>

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

### <span data-ttu-id="67183-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="67183-121">-SkuCapacity</span></span>
<span data-ttu-id="67183-122">Unità di velocità effettiva premium del bus di servizio, valori consentiti 1 o 2 o 4</span><span class="sxs-lookup"><span data-stu-id="67183-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="67183-123">-SKUName</span><span class="sxs-lookup"><span data-stu-id="67183-123">-SkuName</span></span>
<span data-ttu-id="67183-124">Nome SKU dello spazio dei nomi del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="67183-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="67183-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="67183-125">-Tag</span></span>
<span data-ttu-id="67183-126">Coppie chiave-valore sotto forma di tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="67183-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="67183-127">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="67183-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="67183-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67183-128">-Confirm</span></span>
<span data-ttu-id="67183-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67183-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67183-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67183-130">-WhatIf</span></span>
<span data-ttu-id="67183-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67183-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67183-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67183-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67183-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67183-133">CommonParameters</span></span>
<span data-ttu-id="67183-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67183-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67183-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67183-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67183-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="67183-136">INPUTS</span></span>

### <span data-ttu-id="67183-137">System.String</span><span class="sxs-lookup"><span data-stu-id="67183-137">System.String</span></span>

### <span data-ttu-id="67183-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="67183-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="67183-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="67183-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="67183-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67183-140">OUTPUTS</span></span>

### <span data-ttu-id="67183-141">Microsoft.Azure.Commands.ServiceBus.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="67183-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="67183-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="67183-142">NOTES</span></span>

## <span data-ttu-id="67183-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67183-143">RELATED LINKS</span></span>
