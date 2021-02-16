---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191814"
---
# <span data-ttu-id="c17df-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c17df-101">New-AzVpnSite</span></span>

## <span data-ttu-id="c17df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c17df-102">SYNOPSIS</span></span>
<span data-ttu-id="c17df-103">Crea una nuova risorsa VpnSite di Azure.</span><span class="sxs-lookup"><span data-stu-id="c17df-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="c17df-104">Si tratta di una rappresentazione RM dei rami dei clienti caricati in Connettività di Azure per S2S con un hub virtuale di Cortex.</span><span class="sxs-lookup"><span data-stu-id="c17df-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="c17df-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c17df-105">SYNTAX</span></span>

### <span data-ttu-id="c17df-106">ByVirtualWanNameByVpnSiteIpAddress (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c17df-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c17df-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="c17df-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c17df-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="c17df-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c17df-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="c17df-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c17df-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="c17df-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c17df-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="c17df-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c17df-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c17df-112">DESCRIPTION</span></span>
<span data-ttu-id="c17df-113">Crea una nuova risorsa VpnSite di Azure.</span><span class="sxs-lookup"><span data-stu-id="c17df-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="c17df-114">Si tratta di una rappresentazione RM dei rami dei clienti caricati in Connettività di Azure per S2S con un hub virtuale di Cortex.</span><span class="sxs-lookup"><span data-stu-id="c17df-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="c17df-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c17df-115">EXAMPLES</span></span>

### <span data-ttu-id="c17df-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c17df-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="c17df-117">Come descritto in precedenza verrà creato un gruppo di risorse, WAN virtuale negli Stati Uniti orientali, nel gruppo di risorse "nonlinkSite" in Azure.</span><span class="sxs-lookup"><span data-stu-id="c17df-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="c17df-118">Viene quindi creato un sito Vpn che rappresenta un ramo di un cliente e lo collega alla WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="c17df-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="c17df-119">È quindi possibile configurare una connessione IPSec con questo ramo e una VpnGateway usando il comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c17df-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="c17df-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c17df-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="c17df-121">In questo modo verrà creato un gruppo di risorse, una WAN virtuale e un sito Vpn con 1 VpnSiteLinks negli Stati Uniti orientali in un gruppo di risorse "multilink" in Azure.</span><span class="sxs-lookup"><span data-stu-id="c17df-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="c17df-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c17df-122">Example 3</span></span>

<span data-ttu-id="c17df-123">Crea una nuova risorsa VpnSite di Azure.</span><span class="sxs-lookup"><span data-stu-id="c17df-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="c17df-124">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c17df-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="c17df-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c17df-125">PARAMETERS</span></span>

### <span data-ttu-id="c17df-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="c17df-126">-AddressSpace</span></span>
<span data-ttu-id="c17df-127">Prefissi di indirizzo della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c17df-127">The address prefixes of the virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c17df-128">-AsJob</span></span>
<span data-ttu-id="c17df-129">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c17df-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c17df-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="c17df-130">-BgpAsn</span></span>
<span data-ttu-id="c17df-131">L'ASN BGP per questo Sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-132">-BgpAddressingAddress</span><span class="sxs-lookup"><span data-stu-id="c17df-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="c17df-133">Indirizzo peering BGP per questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-134">-BgpWeight</span><span class="sxs-lookup"><span data-stu-id="c17df-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="c17df-135">Peso del peering BGP per questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17df-136">-DefaultProfile</span></span>
<span data-ttu-id="c17df-137">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c17df-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c17df-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="c17df-138">-DeviceModel</span></span>
<span data-ttu-id="c17df-139">Il modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="c17df-139">The device model of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="c17df-140">-DeviceVendor</span></span>
<span data-ttu-id="c17df-141">Il fornitore del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="c17df-141">The device vendor of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c17df-142">-IpAddress</span></span>
<span data-ttu-id="c17df-143">IPAddress per questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="c17df-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="c17df-145">Il modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="c17df-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-146">-Location</span><span class="sxs-lookup"><span data-stu-id="c17df-146">-Location</span></span>
<span data-ttu-id="c17df-147">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c17df-147">The resource location.</span></span>

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

### <span data-ttu-id="c17df-148">-Name</span><span class="sxs-lookup"><span data-stu-id="c17df-148">-Name</span></span>
<span data-ttu-id="c17df-149">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c17df-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="c17df-150">-O365Policy</span></span>
<span data-ttu-id="c17df-151">Criteri di interruzione del traffico di Office 365 per questo Sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c17df-152">-ResourceGroupName</span></span>
<span data-ttu-id="c17df-153">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c17df-153">The resource name.</span></span>

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

### <span data-ttu-id="c17df-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="c17df-154">-Tag</span></span>
<span data-ttu-id="c17df-155">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c17df-155">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="c17df-156">-VirtualWan</span></span>
<span data-ttu-id="c17df-157">Il virtualwan a cui deve essere connesso questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="c17df-158">-VirtualWanId</span></span>
<span data-ttu-id="c17df-159">Il valore ResourceId VirtualWan a cui deve essere connesso questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c17df-160">-VirtualWanName</span></span>
<span data-ttu-id="c17df-161">Nome del virtualwan a cui deve essere connesso questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c17df-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="c17df-163">Il nome del gruppo di risorse di VirtualWan a cui deve essere connesso questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c17df-164">-VpnSiteLink</span></span>
<span data-ttu-id="c17df-165">Elenco di VpnSiteLinks disponibili in questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="c17df-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17df-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c17df-166">-Confirm</span></span>
<span data-ttu-id="c17df-167">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c17df-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c17df-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c17df-168">-WhatIf</span></span>
<span data-ttu-id="c17df-169">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c17df-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c17df-170">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c17df-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c17df-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17df-171">CommonParameters</span></span>
<span data-ttu-id="c17df-172">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c17df-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17df-173">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c17df-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17df-174">INPUT</span><span class="sxs-lookup"><span data-stu-id="c17df-174">INPUTS</span></span>

### <span data-ttu-id="c17df-175">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c17df-175">None</span></span>

## <span data-ttu-id="c17df-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c17df-176">OUTPUTS</span></span>

### <span data-ttu-id="c17df-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c17df-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="c17df-178">NOTE</span><span class="sxs-lookup"><span data-stu-id="c17df-178">NOTES</span></span>

## <span data-ttu-id="c17df-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c17df-179">RELATED LINKS</span></span>

[<span data-ttu-id="c17df-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c17df-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="c17df-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c17df-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="c17df-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c17df-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
