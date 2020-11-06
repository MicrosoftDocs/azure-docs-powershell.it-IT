---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517980"
---
# <span data-ttu-id="87a85-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="87a85-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="87a85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87a85-102">SYNOPSIS</span></span>
<span data-ttu-id="87a85-103">Crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="87a85-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87a85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87a85-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87a85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87a85-105">DESCRIPTION</span></span>
<span data-ttu-id="87a85-106">Il cmdlet **New-AzureRmServiceBusNamespace** crea un nuovo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="87a85-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="87a85-107">Una volta creato, il manifesto delle risorse dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="87a85-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="87a85-108">Questa operazione è idempotente.</span><span class="sxs-lookup"><span data-stu-id="87a85-108">This operation is idempotent.</span></span>

## <span data-ttu-id="87a85-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87a85-109">EXAMPLES</span></span>

### <span data-ttu-id="87a85-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="87a85-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="87a85-111">Crea un nuovo spazio dei nomi Service Bus all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="87a85-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="87a85-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87a85-112">PARAMETERS</span></span>

### <span data-ttu-id="87a85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a85-113">-DefaultProfile</span></span>
<span data-ttu-id="87a85-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87a85-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87a85-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="87a85-115">-Location</span></span>
<span data-ttu-id="87a85-116">Posizione dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="87a85-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="87a85-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="87a85-117">-Name</span></span>
<span data-ttu-id="87a85-118">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="87a85-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a85-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a85-119">-ResourceGroupName</span></span>
<span data-ttu-id="87a85-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87a85-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a85-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="87a85-121">-SkuName</span></span>
<span data-ttu-id="87a85-122">Nome del SKU dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="87a85-122">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="87a85-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="87a85-123">-Tag</span></span>
<span data-ttu-id="87a85-124">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="87a85-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="87a85-125">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="87a85-125">For example:</span></span>

<span data-ttu-id="87a85-126">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="87a85-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="87a85-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="87a85-127">-Confirm</span></span>
<span data-ttu-id="87a85-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87a85-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a85-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a85-129">-WhatIf</span></span>
<span data-ttu-id="87a85-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87a85-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87a85-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87a85-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a85-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a85-132">CommonParameters</span></span>
<span data-ttu-id="87a85-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a85-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a85-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a85-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a85-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87a85-135">INPUTS</span></span>

### <span data-ttu-id="87a85-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87a85-136">-ResourceGroup</span></span>
 <span data-ttu-id="87a85-137">System. String</span><span class="sxs-lookup"><span data-stu-id="87a85-137">System.String</span></span>

### <span data-ttu-id="87a85-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="87a85-138">-NamespaceName</span></span>
 <span data-ttu-id="87a85-139">System. String</span><span class="sxs-lookup"><span data-stu-id="87a85-139">System.String</span></span>

### <span data-ttu-id="87a85-140">-Posizione</span><span class="sxs-lookup"><span data-stu-id="87a85-140">-Location</span></span>
 <span data-ttu-id="87a85-141">System. String</span><span class="sxs-lookup"><span data-stu-id="87a85-141">System.String</span></span>

### <span data-ttu-id="87a85-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="87a85-142">-SkuName</span></span>
 <span data-ttu-id="87a85-143">System. String</span><span class="sxs-lookup"><span data-stu-id="87a85-143">System.String</span></span>

### <span data-ttu-id="87a85-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="87a85-144">-Tag</span></span>
 <span data-ttu-id="87a85-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="87a85-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87a85-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87a85-146">OUTPUTS</span></span>

### <span data-ttu-id="87a85-147">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="87a85-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="87a85-148">Note</span><span class="sxs-lookup"><span data-stu-id="87a85-148">NOTES</span></span>

## <span data-ttu-id="87a85-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87a85-149">RELATED LINKS</span></span>

