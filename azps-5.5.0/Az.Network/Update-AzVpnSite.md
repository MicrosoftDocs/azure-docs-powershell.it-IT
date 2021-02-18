---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193262"
---
# <span data-ttu-id="3b20a-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3b20a-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="3b20a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b20a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b20a-103">Aggiorna un sito VPN.</span><span class="sxs-lookup"><span data-stu-id="3b20a-103">Updates a VPN site.</span></span>

## <span data-ttu-id="3b20a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b20a-104">SYNTAX</span></span>

### <span data-ttu-id="3b20a-105">ByVpnSiteNameNoVirtualWanUpdate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b20a-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b20a-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="3b20a-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b20a-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="3b20a-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b20a-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="3b20a-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b20a-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="3b20a-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b20a-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="3b20a-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b20a-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="3b20a-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b20a-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="3b20a-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b20a-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="3b20a-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b20a-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="3b20a-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b20a-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="3b20a-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b20a-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="3b20a-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b20a-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b20a-117">DESCRIPTION</span></span>
<span data-ttu-id="3b20a-118">Il cmdlet **Update-AzVpnSite** aggiorna un sito VPN.</span><span class="sxs-lookup"><span data-stu-id="3b20a-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="3b20a-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b20a-119">EXAMPLES</span></span>

### <span data-ttu-id="3b20a-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b20a-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="3b20a-121">Come descritto in precedenza verrà creato un gruppo di risorse, wan virtuale negli Stati Uniti occidentali, nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="3b20a-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="3b20a-122">Viene quindi creato un sito Vpn che rappresenta un ramo di un cliente e lo collega alla WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b20a-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="3b20a-123">Una volta creato, il sito aggiorna IpAddress del sito usando il comando Set-AzVpnSite></span><span class="sxs-lookup"><span data-stu-id="3b20a-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="3b20a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b20a-124">PARAMETERS</span></span>

### <span data-ttu-id="3b20a-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="3b20a-125">-AddressSpace</span></span>
<span data-ttu-id="3b20a-126">Prefissi di indirizzo della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b20a-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="3b20a-127">Usare questo o AddressSpaceObject, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="3b20a-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="3b20a-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b20a-128">-AsJob</span></span>
<span data-ttu-id="3b20a-129">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3b20a-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b20a-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="3b20a-130">-BgpAsn</span></span>
<span data-ttu-id="3b20a-131">L'ASN BGP per questo Sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="3b20a-132">-BgpAddressingAddress</span><span class="sxs-lookup"><span data-stu-id="3b20a-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="3b20a-133">Indirizzo peering BGP per questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="3b20a-134">-BgpWeight</span><span class="sxs-lookup"><span data-stu-id="3b20a-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="3b20a-135">Peso del peering BGP per questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="3b20a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b20a-136">-DefaultProfile</span></span>
<span data-ttu-id="3b20a-137">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b20a-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b20a-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="3b20a-138">-DeviceModel</span></span>
<span data-ttu-id="3b20a-139">Il modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="3b20a-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="3b20a-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="3b20a-140">-DeviceVendor</span></span>
<span data-ttu-id="3b20a-141">Il fornitore del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="3b20a-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="3b20a-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b20a-142">-InputObject</span></span>
<span data-ttu-id="3b20a-143">Oggetto sito vpn da modificare</span><span class="sxs-lookup"><span data-stu-id="3b20a-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="3b20a-144">-IpAddress</span></span>
<span data-ttu-id="3b20a-145">Indirizzo IP del gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="3b20a-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="3b20a-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="3b20a-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="3b20a-147">Il modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="3b20a-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="3b20a-148">-Name</span><span class="sxs-lookup"><span data-stu-id="3b20a-148">-Name</span></span>
<span data-ttu-id="3b20a-149">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3b20a-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="3b20a-150">-O365Policy</span></span>
<span data-ttu-id="3b20a-151">Criteri di interruzione del traffico di Office 365 per questo Sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="3b20a-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b20a-152">-ResourceGroupName</span></span>
<span data-ttu-id="3b20a-153">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b20a-153">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b20a-154">-ResourceId</span></span>
<span data-ttu-id="3b20a-155">ID della risorsa Azure per il sito vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-155">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b20a-156">-Tag</span></span>
<span data-ttu-id="3b20a-157">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="3b20a-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3b20a-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="3b20a-158">-VirtualWan</span></span>
<span data-ttu-id="3b20a-159">Il virtualwan a cui deve essere connesso questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="3b20a-160">-VirtualWanId</span></span>
<span data-ttu-id="3b20a-161">Il valore ResourceId VirtualWan a cui deve essere connesso questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="3b20a-162">-VirtualWanName</span></span>
<span data-ttu-id="3b20a-163">Nome del virtualwan a cui deve essere connesso questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b20a-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="3b20a-165">Il nome del gruppo di risorse di VirtualWan a cui deve essere connesso questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3b20a-166">-VpnSiteLink</span></span>
<span data-ttu-id="3b20a-167">Elenco di VpnSiteLinks disponibili in questo sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="3b20a-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b20a-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b20a-168">-Confirm</span></span>
<span data-ttu-id="3b20a-169">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b20a-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b20a-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b20a-170">-WhatIf</span></span>
<span data-ttu-id="3b20a-171">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b20a-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b20a-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b20a-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b20a-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b20a-173">CommonParameters</span></span>
<span data-ttu-id="3b20a-174">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b20a-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b20a-175">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b20a-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b20a-176">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b20a-176">INPUTS</span></span>

### <span data-ttu-id="3b20a-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="3b20a-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="3b20a-178">System.String</span><span class="sxs-lookup"><span data-stu-id="3b20a-178">System.String</span></span>

## <span data-ttu-id="3b20a-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b20a-179">OUTPUTS</span></span>

### <span data-ttu-id="3b20a-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="3b20a-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="3b20a-181">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b20a-181">NOTES</span></span>

## <span data-ttu-id="3b20a-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b20a-182">RELATED LINKS</span></span>

[<span data-ttu-id="3b20a-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3b20a-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="3b20a-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3b20a-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="3b20a-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3b20a-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
