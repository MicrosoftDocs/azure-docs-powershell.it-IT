---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 6ac46fc8b8f94480e11f00d44efc690d97ee56a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687259"
---
# <span data-ttu-id="49d00-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="49d00-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="49d00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49d00-102">SYNOPSIS</span></span>
<span data-ttu-id="49d00-103">Aggiorna la descrizione di uno spazio dei nomi di Service Bus esistente.</span><span class="sxs-lookup"><span data-stu-id="49d00-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49d00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49d00-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49d00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49d00-105">DESCRIPTION</span></span>
<span data-ttu-id="49d00-106">Il cmdlet **set-AzureRmServiceBusNamespace** aggiorna la descrizione dello spazio dei nomi Service Bus specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49d00-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="49d00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49d00-107">EXAMPLES</span></span>

### <span data-ttu-id="49d00-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49d00-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="49d00-109">Aggiorna lo spazio dei nomi Service Bus con una nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="49d00-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="49d00-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49d00-110">PARAMETERS</span></span>

### <span data-ttu-id="49d00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d00-111">-DefaultProfile</span></span>
<span data-ttu-id="49d00-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49d00-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49d00-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="49d00-113">-Location</span></span>
<span data-ttu-id="49d00-114">Posizione dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="49d00-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="49d00-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="49d00-115">-Name</span></span>
<span data-ttu-id="49d00-116">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="49d00-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="49d00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d00-117">-ResourceGroupName</span></span>
<span data-ttu-id="49d00-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49d00-118">The resource group name.</span></span>

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

### <span data-ttu-id="49d00-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="49d00-119">-SkuCapacity</span></span>
<span data-ttu-id="49d00-120">Capacità SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="49d00-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="49d00-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="49d00-121">-SkuName</span></span>
<span data-ttu-id="49d00-122">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="49d00-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="49d00-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="49d00-123">-Tag</span></span>
<span data-ttu-id="49d00-124">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="49d00-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="49d00-125">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="49d00-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="49d00-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49d00-126">-Confirm</span></span>
<span data-ttu-id="49d00-127">Aggiorna lo spazio dei nomi Service Bus con le informazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="49d00-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="49d00-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49d00-128">-WhatIf</span></span>
<span data-ttu-id="49d00-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49d00-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49d00-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49d00-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49d00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d00-131">CommonParameters</span></span>
<span data-ttu-id="49d00-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d00-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d00-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d00-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49d00-134">INPUTS</span></span>

### <span data-ttu-id="49d00-135">System. String</span><span class="sxs-lookup"><span data-stu-id="49d00-135">System.String</span></span>

### <span data-ttu-id="49d00-136">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="49d00-136">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="49d00-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="49d00-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="49d00-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49d00-138">OUTPUTS</span></span>

### <span data-ttu-id="49d00-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="49d00-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="49d00-140">Note</span><span class="sxs-lookup"><span data-stu-id="49d00-140">NOTES</span></span>

## <span data-ttu-id="49d00-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49d00-141">RELATED LINKS</span></span>
