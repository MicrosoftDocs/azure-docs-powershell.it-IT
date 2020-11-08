---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 31679702c1499ac91f41b14057e1bc13ef2dfc32
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192309"
---
# <span data-ttu-id="ac880-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ac880-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="ac880-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac880-102">SYNOPSIS</span></span>
<span data-ttu-id="ac880-103">Crea un oggetto VpnSiteLinkConnection di Azure.</span><span class="sxs-lookup"><span data-stu-id="ac880-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="ac880-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac880-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac880-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac880-105">DESCRIPTION</span></span>
<span data-ttu-id="ac880-106">Crea un oggetto VpnSiteLinkConnection di Azure.</span><span class="sxs-lookup"><span data-stu-id="ac880-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="ac880-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac880-107">EXAMPLES</span></span>

### <span data-ttu-id="ac880-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac880-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="ac880-109">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un VpnSite con 1 VpnSiteLinks in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="ac880-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="ac880-110">Un gateway VPN verrà creato successivamente nell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac880-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="ac880-111">Dopo aver creato il gateway, viene connesso a VpnSite usando il comando New-AzVpnConnection con 1 VpnSiteLinkConnections alla VpnSiteLink di VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ac880-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="ac880-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac880-112">PARAMETERS</span></span>

### <span data-ttu-id="ac880-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="ac880-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="ac880-114">Larghezza di banda che deve essere gestita da questa connessione di collegamento in Mbps.</span><span class="sxs-lookup"><span data-stu-id="ac880-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac880-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac880-115">-DefaultProfile</span></span>
<span data-ttu-id="ac880-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac880-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac880-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ac880-117">-EnableBgp</span></span>
<span data-ttu-id="ac880-118">Abilitare BGP per questa connessione di collegamento</span><span class="sxs-lookup"><span data-stu-id="ac880-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="ac880-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="ac880-119">-IpSecPolicy</span></span>
<span data-ttu-id="ac880-120">Criteri IpSec da considerare per questa connessione di collegamento.</span><span class="sxs-lookup"><span data-stu-id="ac880-120">IpSec Policy to be considered for this link connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac880-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac880-121">-Name</span></span>
<span data-ttu-id="ac880-122">Nome</span><span class="sxs-lookup"><span data-stu-id="ac880-122">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac880-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="ac880-123">-RoutingWeight</span></span>
<span data-ttu-id="ac880-124">Peso del routing</span><span class="sxs-lookup"><span data-stu-id="ac880-124">Routing Weight</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac880-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ac880-125">-SharedKey</span></span>
<span data-ttu-id="ac880-126">Chiave condivisa necessaria per impostare la connessione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="ac880-126">The shared key required to set this link connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac880-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="ac880-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="ac880-128">Usa l'indirizzo IP locale di Azure come IP di origine per questa connessione di collegamento.</span><span class="sxs-lookup"><span data-stu-id="ac880-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="ac880-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ac880-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="ac880-130">Usare i selettori del traffico basati su criteri per questa connessione di collegamento.</span><span class="sxs-lookup"><span data-stu-id="ac880-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="ac880-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="ac880-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="ac880-132">Protocollo di connessione gateway: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="ac880-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac880-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ac880-133">-VpnSiteLink</span></span>
<span data-ttu-id="ac880-134">L'oggetto collegamento al sito VPN a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="ac880-134">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac880-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac880-135">CommonParameters</span></span>
<span data-ttu-id="ac880-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac880-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac880-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac880-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac880-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac880-138">INPUTS</span></span>

### <span data-ttu-id="ac880-139">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ac880-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="ac880-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac880-140">OUTPUTS</span></span>

### <span data-ttu-id="ac880-141">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ac880-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="ac880-142">Note</span><span class="sxs-lookup"><span data-stu-id="ac880-142">NOTES</span></span>

## <span data-ttu-id="ac880-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac880-143">RELATED LINKS</span></span>

[<span data-ttu-id="ac880-144">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ac880-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)