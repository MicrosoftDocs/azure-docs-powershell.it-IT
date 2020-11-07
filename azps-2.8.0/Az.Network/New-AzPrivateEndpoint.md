---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: c72af57f860dcc1c889ecf81111341fa7dbe21eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854410"
---
# <span data-ttu-id="60f74-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60f74-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="60f74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60f74-102">SYNOPSIS</span></span>
<span data-ttu-id="60f74-103">Crea un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="60f74-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="60f74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60f74-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60f74-105">DESCRIPTION</span></span>
<span data-ttu-id="60f74-106">Il cmdlet **New-AzPrivateEndpoint** crea un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="60f74-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="60f74-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60f74-107">EXAMPLES</span></span>

### <span data-ttu-id="60f74-108">1: creare un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="60f74-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="60f74-109">Questo esempio crea un endpoint privato con ID del servizio di collegamento privato specifico in una subnet specifica in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="60f74-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="60f74-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60f74-110">PARAMETERS</span></span>

### <span data-ttu-id="60f74-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60f74-111">-AsJob</span></span>
<span data-ttu-id="60f74-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="60f74-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60f74-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="60f74-113">-ByManualRequest</span></span>
<span data-ttu-id="60f74-114">Uso della richiesta manuale.</span><span class="sxs-lookup"><span data-stu-id="60f74-114">Using manual request.</span></span>

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

### <span data-ttu-id="60f74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f74-115">-DefaultProfile</span></span>
<span data-ttu-id="60f74-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60f74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f74-117">-Force</span><span class="sxs-lookup"><span data-stu-id="60f74-117">-Force</span></span>
<span data-ttu-id="60f74-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="60f74-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="60f74-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="60f74-119">-Location</span></span>
<span data-ttu-id="60f74-120">posizione.</span><span class="sxs-lookup"><span data-stu-id="60f74-120">location.</span></span>

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

### <span data-ttu-id="60f74-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="60f74-121">-Name</span></span>
<span data-ttu-id="60f74-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="60f74-122">The resource name.</span></span>

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

### <span data-ttu-id="60f74-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="60f74-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="60f74-124">Connessione del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="60f74-124">The private link service connection.</span></span>

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

### <span data-ttu-id="60f74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f74-125">-ResourceGroupName</span></span>
<span data-ttu-id="60f74-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60f74-126">The resource group name.</span></span>

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

### <span data-ttu-id="60f74-127">-Subnet</span><span class="sxs-lookup"><span data-stu-id="60f74-127">-Subnet</span></span>
<span data-ttu-id="60f74-128">Subnet dell'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="60f74-128">The subnet of the private endpoint</span></span>

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

### <span data-ttu-id="60f74-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="60f74-129">-Tag</span></span>
<span data-ttu-id="60f74-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="60f74-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="60f74-131">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="60f74-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="60f74-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60f74-132">-Confirm</span></span>
<span data-ttu-id="60f74-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60f74-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f74-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f74-134">-WhatIf</span></span>
<span data-ttu-id="60f74-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60f74-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f74-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60f74-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f74-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f74-137">CommonParameters</span></span>
<span data-ttu-id="60f74-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f74-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f74-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60f74-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f74-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60f74-140">INPUTS</span></span>

### <span data-ttu-id="60f74-141">System. String</span><span class="sxs-lookup"><span data-stu-id="60f74-141">System.String</span></span>

### <span data-ttu-id="60f74-142">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="60f74-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="60f74-143">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="60f74-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="60f74-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60f74-144">OUTPUTS</span></span>

### <span data-ttu-id="60f74-145">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60f74-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="60f74-146">Note</span><span class="sxs-lookup"><span data-stu-id="60f74-146">NOTES</span></span>

## <span data-ttu-id="60f74-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60f74-147">RELATED LINKS</span></span>

[<span data-ttu-id="60f74-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60f74-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="60f74-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60f74-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="60f74-150">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="60f74-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)