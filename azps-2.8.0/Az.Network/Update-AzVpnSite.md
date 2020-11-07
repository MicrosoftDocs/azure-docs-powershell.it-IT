---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: 239a09435c7410ef948503d7f4b31cd60943ce59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855074"
---
# <span data-ttu-id="25bea-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="25bea-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="25bea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25bea-102">SYNOPSIS</span></span>
<span data-ttu-id="25bea-103">Aggiorna un sito VPN.</span><span class="sxs-lookup"><span data-stu-id="25bea-103">Updates a VPN site.</span></span>

## <span data-ttu-id="25bea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25bea-104">SYNTAX</span></span>

### <span data-ttu-id="25bea-105">ByVpnSiteNameNoVirtualWanUpdate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25bea-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bea-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="25bea-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bea-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="25bea-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25bea-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="25bea-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25bea-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="25bea-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bea-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="25bea-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25bea-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="25bea-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25bea-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="25bea-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bea-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="25bea-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bea-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="25bea-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bea-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="25bea-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25bea-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="25bea-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25bea-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25bea-117">DESCRIPTION</span></span>
<span data-ttu-id="25bea-118">Il cmdlet **Update-AzVpnSite** aggiorna un sito VPN.</span><span class="sxs-lookup"><span data-stu-id="25bea-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="25bea-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25bea-119">EXAMPLES</span></span>

### <span data-ttu-id="25bea-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25bea-120">Example 1</span></span>

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

<span data-ttu-id="25bea-121">Quanto sopra creerà un gruppo di risorse, Virtual WAN in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="25bea-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="25bea-122">Crea quindi un VpnSite per rappresentare un ramo Customer e lo collega alla rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="25bea-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="25bea-123">Dopo aver creato il sito, viene aggiornato l'indirizzo IpAddress del sito tramite il comando Set-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="25bea-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25bea-124">PARAMETERS</span></span>

### <span data-ttu-id="25bea-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="25bea-125">-AddressSpace</span></span>
<span data-ttu-id="25bea-126">I prefissi degli indirizzi della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="25bea-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="25bea-127">Usare questo o AddressSpaceObject ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="25bea-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="25bea-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25bea-128">-AsJob</span></span>
<span data-ttu-id="25bea-129">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="25bea-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25bea-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="25bea-130">-BgpAsn</span></span>
<span data-ttu-id="25bea-131">BGP ASN per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="25bea-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="25bea-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="25bea-133">Indirizzo di peering BGP per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="25bea-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="25bea-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="25bea-135">Il peso di peering BGP per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="25bea-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bea-136">-DefaultProfile</span></span>
<span data-ttu-id="25bea-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25bea-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25bea-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="25bea-138">-DeviceModel</span></span>
<span data-ttu-id="25bea-139">Modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="25bea-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="25bea-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="25bea-140">-DeviceVendor</span></span>
<span data-ttu-id="25bea-141">Il fornitore del dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="25bea-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="25bea-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25bea-142">-InputObject</span></span>
<span data-ttu-id="25bea-143">Oggetto sito VPN da modificare</span><span class="sxs-lookup"><span data-stu-id="25bea-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="25bea-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="25bea-144">-IpAddress</span></span>
<span data-ttu-id="25bea-145">Indirizzo IP del gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="25bea-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="25bea-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="25bea-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="25bea-147">Modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="25bea-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="25bea-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="25bea-148">-Name</span></span>
<span data-ttu-id="25bea-149">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="25bea-149">The resource name.</span></span>

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

### <span data-ttu-id="25bea-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bea-150">-ResourceGroupName</span></span>
<span data-ttu-id="25bea-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25bea-151">The resource group name.</span></span>

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

### <span data-ttu-id="25bea-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25bea-152">-ResourceId</span></span>
<span data-ttu-id="25bea-153">ID risorsa Azure per il sito VPN.</span><span class="sxs-lookup"><span data-stu-id="25bea-153">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="25bea-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="25bea-154">-Tag</span></span>
<span data-ttu-id="25bea-155">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="25bea-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="25bea-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="25bea-156">-VirtualWan</span></span>
<span data-ttu-id="25bea-157">VirtualWan a cui deve essere connessa la VpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="25bea-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="25bea-158">-VirtualWanId</span></span>
<span data-ttu-id="25bea-159">ResourceId VirtualWan a cui deve essere connessa la VpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="25bea-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="25bea-160">-VirtualWanName</span></span>
<span data-ttu-id="25bea-161">Il nome del VirtualWan a cui deve essere connesso VpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="25bea-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bea-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="25bea-163">Il nome del gruppo di risorse di VirtualWan a cui deve essere connesso VpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="25bea-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="25bea-164">-VpnSiteLink</span></span>
<span data-ttu-id="25bea-165">L'elenco di VpnSiteLinks che ha VpnSite.</span><span class="sxs-lookup"><span data-stu-id="25bea-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="25bea-166">-Confermare</span><span class="sxs-lookup"><span data-stu-id="25bea-166">-Confirm</span></span>
<span data-ttu-id="25bea-167">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25bea-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25bea-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25bea-168">-WhatIf</span></span>
<span data-ttu-id="25bea-169">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25bea-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25bea-170">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25bea-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25bea-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bea-171">CommonParameters</span></span>
<span data-ttu-id="25bea-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25bea-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bea-173">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25bea-173">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bea-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25bea-174">INPUTS</span></span>

### <span data-ttu-id="25bea-175">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="25bea-175">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="25bea-176">System. String</span><span class="sxs-lookup"><span data-stu-id="25bea-176">System.String</span></span>

## <span data-ttu-id="25bea-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25bea-177">OUTPUTS</span></span>

### <span data-ttu-id="25bea-178">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="25bea-178">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="25bea-179">Note</span><span class="sxs-lookup"><span data-stu-id="25bea-179">NOTES</span></span>

## <span data-ttu-id="25bea-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25bea-180">RELATED LINKS</span></span>

[<span data-ttu-id="25bea-181">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="25bea-181">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="25bea-182">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="25bea-182">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="25bea-183">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="25bea-183">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
