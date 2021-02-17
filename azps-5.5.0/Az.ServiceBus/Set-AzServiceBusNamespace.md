---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191159"
---
# <span data-ttu-id="3a6bd-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="3a6bd-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="3a6bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6bd-103">Aggiorna la descrizione di uno spazio dei nomi bus di servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="3a6bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a6bd-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a6bd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3a6bd-105">DESCRIPTION</span></span>
<span data-ttu-id="3a6bd-106">Il cmdlet **Set-AzServiceBus Firmware** aggiorna la descrizione dello spazio dei nomi del bus di servizio specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="3a6bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a6bd-107">EXAMPLES</span></span>

### <span data-ttu-id="3a6bd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a6bd-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="3a6bd-109">Aggiorna lo spazio dei nomi dei bus di servizio con una nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="3a6bd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a6bd-110">PARAMETERS</span></span>

### <span data-ttu-id="3a6bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6bd-111">-DefaultProfile</span></span>
<span data-ttu-id="3a6bd-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a6bd-113">-Location</span><span class="sxs-lookup"><span data-stu-id="3a6bd-113">-Location</span></span>
<span data-ttu-id="3a6bd-114">Posizione dello spazio dei nomi del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="3a6bd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3a6bd-115">-Name</span></span>
<span data-ttu-id="3a6bd-116">Nome spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="3a6bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a6bd-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-118">The resource group name.</span></span>

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

### <span data-ttu-id="3a6bd-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3a6bd-119">-SkuCapacity</span></span>
<span data-ttu-id="3a6bd-120">Capacità SKU spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="3a6bd-121">-SKUName</span><span class="sxs-lookup"><span data-stu-id="3a6bd-121">-SkuName</span></span>
<span data-ttu-id="3a6bd-122">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="3a6bd-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="3a6bd-123">-Tag</span></span>
<span data-ttu-id="3a6bd-124">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3a6bd-125">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3a6bd-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3a6bd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a6bd-126">-Confirm</span></span>
<span data-ttu-id="3a6bd-127">Aggiorna lo spazio dei nomi dei bus di servizio con le informazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="3a6bd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a6bd-128">-WhatIf</span></span>
<span data-ttu-id="3a6bd-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a6bd-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a6bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6bd-131">CommonParameters</span></span>
<span data-ttu-id="3a6bd-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a6bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6bd-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a6bd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6bd-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="3a6bd-134">INPUTS</span></span>

### <span data-ttu-id="3a6bd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3a6bd-135">System.String</span></span>

### <span data-ttu-id="3a6bd-136">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3a6bd-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3a6bd-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a6bd-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3a6bd-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a6bd-138">OUTPUTS</span></span>

### <span data-ttu-id="3a6bd-139">Microsoft.Azure.Commands.ServiceBus.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="3a6bd-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3a6bd-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="3a6bd-140">NOTES</span></span>

## <span data-ttu-id="3a6bd-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a6bd-141">RELATED LINKS</span></span>
