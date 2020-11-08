---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d6a499292521632b7e0a307a6c745d1606ae4d2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018620"
---
# <span data-ttu-id="5cc25-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5cc25-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5cc25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cc25-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc25-103">Configura una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5cc25-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="5cc25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cc25-104">SYNTAX</span></span>

### <span data-ttu-id="5cc25-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5cc25-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
<<<<<<< HEAD
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc25-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="5cc25-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
<<<<<<< HEAD
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc25-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cc25-107">DESCRIPTION</span></span>
<span data-ttu-id="5cc25-108">Il cmdlet **set-AzVirtualNetworkGatewayConnection** configura una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5cc25-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="5cc25-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cc25-109">EXAMPLES</span></span>

### <span data-ttu-id="5cc25-110">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="5cc25-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="5cc25-111">Esempio 2: aggiungere/aggiornare i tag a un VirtualNetworkGatewayConnection esistente</span><span class="sxs-lookup"><span data-stu-id="5cc25-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="5cc25-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cc25-112">PARAMETERS</span></span>

### <span data-ttu-id="5cc25-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cc25-113">-AsJob</span></span>
<span data-ttu-id="5cc25-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5cc25-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cc25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc25-115">-DefaultProfile</span></span>
<span data-ttu-id="5cc25-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cc25-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cc25-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="5cc25-117">-EnableBgp</span></span>
<span data-ttu-id="5cc25-118">Se usare una sessione BGP su un tunnel VPN di S2S</span><span class="sxs-lookup"><span data-stu-id="5cc25-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc25-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="5cc25-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="5cc25-120">Timeout di rilevamento peer non recapitato della connessione in pochi secondi</span><span class="sxs-lookup"><span data-stu-id="5cc25-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc25-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5cc25-121">-Force</span></span>
<span data-ttu-id="5cc25-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5cc25-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5cc25-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="5cc25-123">-IpsecPolicies</span></span>
<span data-ttu-id="5cc25-124">Elenco di criteri IPSec.</span><span class="sxs-lookup"><span data-stu-id="5cc25-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc25-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="5cc25-125">-Tag</span></span>
<span data-ttu-id="5cc25-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5cc25-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc25-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="5cc25-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="5cc25-128">Elenco dei criteri del selettore del traffico.</span><span class="sxs-lookup"><span data-stu-id="5cc25-128">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc25-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="5cc25-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="5cc25-130">Se usare PrivateIP per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="5cc25-130">Whether to use PrivateIP for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc25-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="5cc25-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="5cc25-132">Se usare i selettori del traffico basati su criteri per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="5cc25-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc25-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5cc25-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="5cc25-134">Specifica l'oggetto PSVirtualNetworkGatewayConnection usato da questo cmdlet per modificare la connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5cc25-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc25-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5cc25-135">-Confirm</span></span>
<span data-ttu-id="5cc25-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cc25-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc25-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc25-137">-WhatIf</span></span>
<span data-ttu-id="5cc25-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cc25-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc25-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cc25-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc25-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc25-140">CommonParameters</span></span>
<span data-ttu-id="5cc25-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cc25-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc25-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc25-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc25-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cc25-143">INPUTS</span></span>

### <span data-ttu-id="5cc25-144">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5cc25-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="5cc25-145">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5cc25-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5cc25-146">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="5cc25-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="5cc25-147">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="5cc25-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="5cc25-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cc25-148">OUTPUTS</span></span>

### <span data-ttu-id="5cc25-149">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5cc25-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5cc25-150">Note</span><span class="sxs-lookup"><span data-stu-id="5cc25-150">NOTES</span></span>

## <span data-ttu-id="5cc25-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cc25-151">RELATED LINKS</span></span>

[<span data-ttu-id="5cc25-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5cc25-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5cc25-153">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5cc25-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5cc25-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5cc25-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


