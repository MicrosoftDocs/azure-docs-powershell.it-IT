---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518028"
---
# <span data-ttu-id="b3d98-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="b3d98-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="b3d98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3d98-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d98-103">Crea un nuovo spazio dei nomi di inoltro.</span><span class="sxs-lookup"><span data-stu-id="b3d98-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3d98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3d98-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3d98-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3d98-105">DESCRIPTION</span></span>
<span data-ttu-id="b3d98-106">Il cmdlet **New-AzureRmRelayNamespace** crea un nuovo spazio dei nomi di inoltro.</span><span class="sxs-lookup"><span data-stu-id="b3d98-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="b3d98-107">Una volta creato, il manifesto delle risorse dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="b3d98-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="b3d98-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3d98-108">EXAMPLES</span></span>

### <span data-ttu-id="b3d98-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3d98-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="b3d98-110">Crea un nuovo spazio dei nomi di inoltro all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b3d98-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="b3d98-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3d98-111">PARAMETERS</span></span>

### <span data-ttu-id="b3d98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d98-112">-DefaultProfile</span></span>
<span data-ttu-id="b3d98-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3d98-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3d98-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b3d98-114">-Location</span></span>
<span data-ttu-id="b3d98-115">Posizione dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="b3d98-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="b3d98-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3d98-116">-Name</span></span>
<span data-ttu-id="b3d98-117">Nome dello spazio dei nomi Relay</span><span class="sxs-lookup"><span data-stu-id="b3d98-117">Relay Namespace Name</span></span>

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

### <span data-ttu-id="b3d98-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d98-118">-ResourceGroupName</span></span>
<span data-ttu-id="b3d98-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3d98-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="b3d98-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3d98-120">-Tag</span></span>
<span data-ttu-id="b3d98-121">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b3d98-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b3d98-122">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="b3d98-122">For example:</span></span>

<span data-ttu-id="b3d98-123">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b3d98-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b3d98-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3d98-124">-Confirm</span></span>
<span data-ttu-id="b3d98-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3d98-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3d98-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3d98-126">-WhatIf</span></span>
<span data-ttu-id="b3d98-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3d98-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3d98-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3d98-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3d98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d98-129">CommonParameters</span></span>
<span data-ttu-id="b3d98-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d98-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3d98-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d98-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3d98-132">INPUTS</span></span>

### <span data-ttu-id="b3d98-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d98-133">-ResourceGroupName</span></span>
 <span data-ttu-id="b3d98-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d98-134">System.String</span></span>

### <span data-ttu-id="b3d98-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b3d98-135">-NamespaceName</span></span>
 <span data-ttu-id="b3d98-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d98-136">System.String</span></span>

### <span data-ttu-id="b3d98-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b3d98-137">-Location</span></span>
 <span data-ttu-id="b3d98-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d98-138">System.String</span></span>

### <span data-ttu-id="b3d98-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b3d98-139">-SkuName</span></span>
 <span data-ttu-id="b3d98-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d98-140">System.String</span></span>

### <span data-ttu-id="b3d98-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3d98-141">-Tag</span></span>
 <span data-ttu-id="b3d98-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b3d98-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b3d98-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3d98-143">OUTPUTS</span></span>

### <span data-ttu-id="b3d98-144">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b3d98-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="b3d98-145">Note</span><span class="sxs-lookup"><span data-stu-id="b3d98-145">NOTES</span></span>

## <span data-ttu-id="b3d98-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3d98-146">RELATED LINKS</span></span>

