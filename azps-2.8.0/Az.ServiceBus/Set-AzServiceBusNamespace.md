---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: 87636c1a15f20610943cc2024ec8ad1f0d4e1647
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854602"
---
# <span data-ttu-id="a5a90-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a5a90-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="a5a90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5a90-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a90-103">Aggiorna la descrizione di uno spazio dei nomi di Service Bus esistente.</span><span class="sxs-lookup"><span data-stu-id="a5a90-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="a5a90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5a90-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a90-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5a90-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a90-106">Il cmdlet **set-AzServiceBusNamespace** aggiorna la descrizione dello spazio dei nomi Service Bus specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5a90-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="a5a90-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5a90-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a90-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5a90-108">Example 1</span></span>
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

<span data-ttu-id="a5a90-109">Aggiorna lo spazio dei nomi Service Bus con una nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="a5a90-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="a5a90-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5a90-110">PARAMETERS</span></span>

### <span data-ttu-id="a5a90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a90-111">-DefaultProfile</span></span>
<span data-ttu-id="a5a90-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5a90-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a5a90-113">-Location</span></span>
<span data-ttu-id="a5a90-114">Posizione dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a5a90-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="a5a90-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5a90-115">-Name</span></span>
<span data-ttu-id="a5a90-116">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="a5a90-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="a5a90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a90-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5a90-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5a90-118">The resource group name.</span></span>

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

### <span data-ttu-id="a5a90-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a90-119">-SkuCapacity</span></span>
<span data-ttu-id="a5a90-120">Capacità SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a5a90-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="a5a90-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a5a90-121">-SkuName</span></span>
<span data-ttu-id="a5a90-122">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a5a90-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="a5a90-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5a90-123">-Tag</span></span>
<span data-ttu-id="a5a90-124">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a5a90-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a5a90-125">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a5a90-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a5a90-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5a90-126">-Confirm</span></span>
<span data-ttu-id="a5a90-127">Aggiorna lo spazio dei nomi Service Bus con le informazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="a5a90-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="a5a90-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a90-128">-WhatIf</span></span>
<span data-ttu-id="a5a90-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5a90-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a90-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5a90-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a90-131">CommonParameters</span></span>
<span data-ttu-id="a5a90-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a90-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a90-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a90-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5a90-134">INPUTS</span></span>

### <span data-ttu-id="a5a90-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a90-135">System.String</span></span>

### <span data-ttu-id="a5a90-136">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a5a90-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a5a90-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a5a90-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a5a90-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5a90-138">OUTPUTS</span></span>

### <span data-ttu-id="a5a90-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a5a90-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a5a90-140">Note</span><span class="sxs-lookup"><span data-stu-id="a5a90-140">NOTES</span></span>

## <span data-ttu-id="a5a90-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5a90-141">RELATED LINKS</span></span>
