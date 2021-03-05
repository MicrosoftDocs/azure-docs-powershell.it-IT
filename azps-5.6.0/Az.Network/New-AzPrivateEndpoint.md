---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: f7ec596a73c3659584d1e0b80c899b4bf9aad8d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982350"
---
# <span data-ttu-id="436f8-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="436f8-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="436f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="436f8-102">SYNOPSIS</span></span>
<span data-ttu-id="436f8-103">Crea un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="436f8-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="436f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="436f8-104">SYNTAX</span></span>

### <span data-ttu-id="436f8-105">Tutti</span><span class="sxs-lookup"><span data-stu-id="436f8-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="436f8-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="436f8-106">DESCRIPTION</span></span>

<span data-ttu-id="436f8-107">Il cmdlet **New-AzPrivateEndpoint** crea un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="436f8-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="436f8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="436f8-108">EXAMPLES</span></span>

### <span data-ttu-id="436f8-109">Esempio 1: Creare un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="436f8-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="436f8-110">L'esempio seguente crea un endpoint privato con un ID del servizio di collegamento privato specifico nella subnet specificata in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="436f8-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="436f8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="436f8-111">PARAMETERS</span></span>

### <span data-ttu-id="436f8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="436f8-112">-AsJob</span></span>

<span data-ttu-id="436f8-113">Eseguire il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="436f8-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="436f8-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="436f8-114">-ByManualRequest</span></span>

<span data-ttu-id="436f8-115">Usare la richiesta manuale per stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="436f8-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="436f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436f8-116">-DefaultProfile</span></span>

<span data-ttu-id="436f8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="436f8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="436f8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="436f8-118">-Force</span></span>

<span data-ttu-id="436f8-119">Non chiedere conferma per sovrascrivere una risorsa.</span><span class="sxs-lookup"><span data-stu-id="436f8-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="436f8-120">-Location</span><span class="sxs-lookup"><span data-stu-id="436f8-120">-Location</span></span>

<span data-ttu-id="436f8-121">Specifica una posizione per l'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="436f8-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="436f8-122">Usare [Get-AzLocation per](/powershell/module/az.resources/get-azlocation) determinare i valori validi per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="436f8-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="436f8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="436f8-123">-Name</span></span>

<span data-ttu-id="436f8-124">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="436f8-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="436f8-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="436f8-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="436f8-126">ID della risorsa per connettere l'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="436f8-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="436f8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="436f8-127">-ResourceGroupName</span></span>

<span data-ttu-id="436f8-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="436f8-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="436f8-129">-Subnet</span><span class="sxs-lookup"><span data-stu-id="436f8-129">-Subnet</span></span>

<span data-ttu-id="436f8-130">Subnet dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="436f8-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="436f8-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="436f8-131">-Tag</span></span>

<span data-ttu-id="436f8-132">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="436f8-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="436f8-133">Ad esempio: @{key0='value0';key1=$null;key2='value2'}</span><span class="sxs-lookup"><span data-stu-id="436f8-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="436f8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="436f8-134">-Confirm</span></span>

<span data-ttu-id="436f8-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="436f8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="436f8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="436f8-136">-WhatIf</span></span>

<span data-ttu-id="436f8-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="436f8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="436f8-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="436f8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="436f8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436f8-139">CommonParameters</span></span>

<span data-ttu-id="436f8-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="436f8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436f8-141">Per altre informazioni, [vedere](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="436f8-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="436f8-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="436f8-142">INPUTS</span></span>

### <span data-ttu-id="436f8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="436f8-143">System.String</span></span>

### <span data-ttu-id="436f8-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="436f8-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="436f8-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span><span class="sxs-lookup"><span data-stu-id="436f8-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="436f8-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="436f8-146">OUTPUTS</span></span>

### <span data-ttu-id="436f8-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="436f8-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="436f8-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="436f8-148">NOTES</span></span>

## <span data-ttu-id="436f8-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="436f8-149">RELATED LINKS</span></span>

[<span data-ttu-id="436f8-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="436f8-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="436f8-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="436f8-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="436f8-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="436f8-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)