---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: a459ec99852d83dcba05a3a594ee2ae4378c318c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018975"
---
# <span data-ttu-id="bdf8c-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdf8c-101">New-AzVpnSite</span></span>

## <span data-ttu-id="bdf8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdf8c-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf8c-103">Crea una nuova risorsa di Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="bdf8c-104">Questa è una rappresentazione RM delle branche del cliente caricata in Azure per la connettività S2S con un hub virtuale Cortex.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="bdf8c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdf8c-105">SYNTAX</span></span>

### <span data-ttu-id="bdf8c-106">ByVirtualWanNameByVpnSiteIpAddress (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdf8c-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf8c-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="bdf8c-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf8c-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf8c-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdf8c-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="bdf8c-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdf8c-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf8c-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdf8c-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="bdf8c-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdf8c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdf8c-112">DESCRIPTION</span></span>
<span data-ttu-id="bdf8c-113">Crea una nuova risorsa di Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="bdf8c-114">Questa è una rappresentazione RM delle branche del cliente caricata in Azure per la connettività S2S con un hub virtuale Cortex.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="bdf8c-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdf8c-115">EXAMPLES</span></span>

### <span data-ttu-id="bdf8c-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bdf8c-116">Example 1</span></span>

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

<span data-ttu-id="bdf8c-117">In precedenza verrà creato un gruppo di risorse, Virtual WAN in East US nel gruppo di risorse "nonlinkSite" in Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="bdf8c-118">Crea quindi un VpnSite per rappresentare un ramo Customer e lo collega alla rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="bdf8c-119">Una connessione IPSec può quindi essere imposta con questo ramo e un VpnGateway usando il comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="bdf8c-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bdf8c-120">Example 2</span></span>
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

<span data-ttu-id="bdf8c-121">Il precedente creerà un gruppo di risorse, una WAN virtuale e un VpnSite con 1 VpnSiteLinks in East US nel gruppo di risorse "Multilink" in Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

## <span data-ttu-id="bdf8c-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdf8c-122">PARAMETERS</span></span>

### <span data-ttu-id="bdf8c-123">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="bdf8c-123">-AddressSpace</span></span>
<span data-ttu-id="bdf8c-124">I prefissi degli indirizzi della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-124">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="bdf8c-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdf8c-125">-AsJob</span></span>
<span data-ttu-id="bdf8c-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bdf8c-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdf8c-127">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="bdf8c-127">-BgpAsn</span></span>
<span data-ttu-id="bdf8c-128">BGP ASN per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-128">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="bdf8c-129">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="bdf8c-129">-BgpPeeringAddress</span></span>
<span data-ttu-id="bdf8c-130">Indirizzo di peering BGP per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-130">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="bdf8c-131">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="bdf8c-131">-BgpPeeringWeight</span></span>
<span data-ttu-id="bdf8c-132">Il peso di peering BGP per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-132">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="bdf8c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf8c-133">-DefaultProfile</span></span>
<span data-ttu-id="bdf8c-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdf8c-135">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="bdf8c-135">-DeviceModel</span></span>
<span data-ttu-id="bdf8c-136">Modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-136">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="bdf8c-137">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="bdf8c-137">-DeviceVendor</span></span>
<span data-ttu-id="bdf8c-138">Il fornitore del dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-138">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="bdf8c-139">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf8c-139">-IpAddress</span></span>
<span data-ttu-id="bdf8c-140">IPAddress per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-140">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="bdf8c-141">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="bdf8c-141">-LinkSpeedInMbps</span></span>
<span data-ttu-id="bdf8c-142">Modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-142">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="bdf8c-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bdf8c-143">-Location</span></span>
<span data-ttu-id="bdf8c-144">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-144">The resource location.</span></span>

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

### <span data-ttu-id="bdf8c-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdf8c-145">-Name</span></span>
<span data-ttu-id="bdf8c-146">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-146">The resource name.</span></span>

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

### <span data-ttu-id="bdf8c-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf8c-147">-ResourceGroupName</span></span>
<span data-ttu-id="bdf8c-148">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-148">The resource name.</span></span>

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

### <span data-ttu-id="bdf8c-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="bdf8c-149">-Tag</span></span>
<span data-ttu-id="bdf8c-150">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-150">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bdf8c-151">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="bdf8c-151">-VirtualWan</span></span>
<span data-ttu-id="bdf8c-152">VirtualWan a cui deve essere connessa la VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-152">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="bdf8c-153">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="bdf8c-153">-VirtualWanId</span></span>
<span data-ttu-id="bdf8c-154">ResourceId VirtualWan a cui deve essere connessa la VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-154">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="bdf8c-155">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="bdf8c-155">-VirtualWanName</span></span>
<span data-ttu-id="bdf8c-156">Il nome del VirtualWan a cui deve essere connesso VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-156">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="bdf8c-157">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf8c-157">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="bdf8c-158">Il nome del gruppo di risorse di VirtualWan a cui deve essere connesso VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-158">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="bdf8c-159">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="bdf8c-159">-VpnSiteLink</span></span>
<span data-ttu-id="bdf8c-160">L'elenco di VpnSiteLinks che ha VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-160">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="bdf8c-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bdf8c-161">-Confirm</span></span>
<span data-ttu-id="bdf8c-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdf8c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf8c-163">-WhatIf</span></span>
<span data-ttu-id="bdf8c-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdf8c-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdf8c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf8c-166">CommonParameters</span></span>
<span data-ttu-id="bdf8c-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf8c-168">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdf8c-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf8c-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdf8c-169">INPUTS</span></span>

### <span data-ttu-id="bdf8c-170">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bdf8c-170">None</span></span>

## <span data-ttu-id="bdf8c-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdf8c-171">OUTPUTS</span></span>

### <span data-ttu-id="bdf8c-172">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdf8c-172">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="bdf8c-173">Note</span><span class="sxs-lookup"><span data-stu-id="bdf8c-173">NOTES</span></span>

## <span data-ttu-id="bdf8c-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdf8c-174">RELATED LINKS</span></span>

[<span data-ttu-id="bdf8c-175">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdf8c-175">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="bdf8c-176">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdf8c-176">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="bdf8c-177">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdf8c-177">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
