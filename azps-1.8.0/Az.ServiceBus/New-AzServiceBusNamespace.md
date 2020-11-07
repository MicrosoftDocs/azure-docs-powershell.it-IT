---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 8ca2b63b541bb20e6cbde861fc8c1329410335a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677139"
---
# <span data-ttu-id="36376-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="36376-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="36376-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36376-102">SYNOPSIS</span></span>
<span data-ttu-id="36376-103">Crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="36376-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="36376-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36376-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36376-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36376-105">DESCRIPTION</span></span>
<span data-ttu-id="36376-106">Il cmdlet **New-AzServiceBusNamespace** crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="36376-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="36376-107">Una volta creato, il manifesto delle risorse dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="36376-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="36376-108">Questa operazione è idempotente.</span><span class="sxs-lookup"><span data-stu-id="36376-108">This operation is idempotent.</span></span>

## <span data-ttu-id="36376-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36376-109">EXAMPLES</span></span>

### <span data-ttu-id="36376-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36376-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="36376-111">Crea un nuovo spazio dei nomi Service Bus all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="36376-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="36376-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36376-112">PARAMETERS</span></span>

### <span data-ttu-id="36376-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36376-113">-DefaultProfile</span></span>
<span data-ttu-id="36376-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36376-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36376-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="36376-115">-Location</span></span>
<span data-ttu-id="36376-116">Posizione dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="36376-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="36376-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="36376-117">-Name</span></span>
<span data-ttu-id="36376-118">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="36376-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="36376-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36376-119">-ResourceGroupName</span></span>
<span data-ttu-id="36376-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36376-120">The resource group name.</span></span>

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

### <span data-ttu-id="36376-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="36376-121">-SkuCapacity</span></span>
<span data-ttu-id="36376-122">Unità throughput dello spazio dei nomi Service Bus Premium, valori consentiti 1 o 2 o 4</span><span class="sxs-lookup"><span data-stu-id="36376-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="36376-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="36376-123">-SkuName</span></span>
<span data-ttu-id="36376-124">Nome del SKU dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="36376-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="36376-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="36376-125">-Tag</span></span>
<span data-ttu-id="36376-126">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="36376-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="36376-127">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="36376-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="36376-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36376-128">-Confirm</span></span>
<span data-ttu-id="36376-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36376-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36376-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36376-130">-WhatIf</span></span>
<span data-ttu-id="36376-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36376-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36376-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36376-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36376-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36376-133">CommonParameters</span></span>
<span data-ttu-id="36376-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36376-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36376-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36376-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36376-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36376-136">INPUTS</span></span>

### <span data-ttu-id="36376-137">System. String</span><span class="sxs-lookup"><span data-stu-id="36376-137">System.String</span></span>

### <span data-ttu-id="36376-138">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36376-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="36376-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="36376-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="36376-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36376-140">OUTPUTS</span></span>

### <span data-ttu-id="36376-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="36376-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="36376-142">Note</span><span class="sxs-lookup"><span data-stu-id="36376-142">NOTES</span></span>

## <span data-ttu-id="36376-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36376-143">RELATED LINKS</span></span>
