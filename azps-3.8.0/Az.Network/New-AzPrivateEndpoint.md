---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: 6e83def7c4956e4936e8e3c55f96aab1da0d451d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019728"
---
# <span data-ttu-id="544a3-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="544a3-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="544a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="544a3-102">SYNOPSIS</span></span>
<span data-ttu-id="544a3-103">Crea un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="544a3-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="544a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="544a3-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="544a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="544a3-105">DESCRIPTION</span></span>
<span data-ttu-id="544a3-106">Il cmdlet **New-AzPrivateEndpoint** crea un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="544a3-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="544a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="544a3-107">EXAMPLES</span></span>

### <span data-ttu-id="544a3-108">1: creare un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="544a3-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="544a3-109">Questo esempio crea un endpoint privato con ID del servizio di collegamento privato specifico in una subnet specifica in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="544a3-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="544a3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="544a3-110">PARAMETERS</span></span>

### <span data-ttu-id="544a3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="544a3-111">-AsJob</span></span>
<span data-ttu-id="544a3-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="544a3-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="544a3-113">-ByManualRequest</span></span>
<span data-ttu-id="544a3-114">Uso della richiesta manuale.</span><span class="sxs-lookup"><span data-stu-id="544a3-114">Using manual request.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="544a3-115">-DefaultProfile</span></span>
<span data-ttu-id="544a3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="544a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="544a3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="544a3-117">-Force</span></span>
<span data-ttu-id="544a3-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="544a3-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="544a3-119">-Location</span></span>
<span data-ttu-id="544a3-120">posizione.</span><span class="sxs-lookup"><span data-stu-id="544a3-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="544a3-121">-Name</span></span>
<span data-ttu-id="544a3-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="544a3-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="544a3-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="544a3-124">Connessione del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="544a3-124">The private link service connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="544a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="544a3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="544a3-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-127">-Subnet</span><span class="sxs-lookup"><span data-stu-id="544a3-127">-Subnet</span></span>
<span data-ttu-id="544a3-128">Subnet dell'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="544a3-128">The subnet of the private endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="544a3-129">-Tag</span></span>
<span data-ttu-id="544a3-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="544a3-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="544a3-131">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="544a3-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="544a3-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="544a3-132">-Confirm</span></span>
<span data-ttu-id="544a3-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="544a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="544a3-134">-WhatIf</span></span>
<span data-ttu-id="544a3-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="544a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="544a3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="544a3-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="544a3-137">CommonParameters</span></span>
<span data-ttu-id="544a3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="544a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="544a3-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="544a3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="544a3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="544a3-140">INPUTS</span></span>

### <span data-ttu-id="544a3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="544a3-141">System.String</span></span>

### <span data-ttu-id="544a3-142">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="544a3-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="544a3-143">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="544a3-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="544a3-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="544a3-144">OUTPUTS</span></span>

### <span data-ttu-id="544a3-145">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="544a3-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="544a3-146">Note</span><span class="sxs-lookup"><span data-stu-id="544a3-146">NOTES</span></span>

## <span data-ttu-id="544a3-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="544a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="544a3-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="544a3-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="544a3-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="544a3-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="544a3-150">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="544a3-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)