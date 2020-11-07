---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 980b84fd1b23cb7e4b034dee485b785b96893f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678195"
---
# <span data-ttu-id="6b612-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b612-101">New-AzVpnSite</span></span>

## <span data-ttu-id="6b612-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b612-102">SYNOPSIS</span></span>
<span data-ttu-id="6b612-103">Crea una nuova risorsa di Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="6b612-104">Questa è una rappresentazione RM delle branche del cliente caricata in Azure per la connettività S2S con un hub virtuale Cortex.</span><span class="sxs-lookup"><span data-stu-id="6b612-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="6b612-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b612-105">SYNTAX</span></span>

### <span data-ttu-id="6b612-106">ByVirtualWanName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b612-106">ByVirtualWanName (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b612-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="6b612-107">ByVirtualWanObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b612-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="6b612-108">ByVirtualWanResourceId</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b612-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b612-109">DESCRIPTION</span></span>
<span data-ttu-id="6b612-110">Crea una nuova risorsa di Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="6b612-111">Questa è una rappresentazione RM delle branche del cliente caricata in Azure per la connettività S2S con un hub virtuale Cortex.</span><span class="sxs-lookup"><span data-stu-id="6b612-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="6b612-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b612-112">EXAMPLES</span></span>

### <span data-ttu-id="6b612-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b612-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="6b612-114">Quanto sopra creerà un gruppo di risorse, Virtual WAN in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="6b612-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="6b612-115">Crea quindi un VpnSite per rappresentare un ramo Customer e lo collega alla rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="6b612-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="6b612-116">Una connessione IPSec può quindi essere imposta con questo ramo e un VpnGateway usando il comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="6b612-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="6b612-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b612-117">PARAMETERS</span></span>

### <span data-ttu-id="6b612-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="6b612-118">-AddressSpace</span></span>
<span data-ttu-id="6b612-119">I prefissi degli indirizzi della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6b612-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="6b612-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b612-120">-AsJob</span></span>
<span data-ttu-id="6b612-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6b612-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b612-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="6b612-122">-BgpAsn</span></span>
<span data-ttu-id="6b612-123">BGP ASN per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="6b612-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="6b612-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="6b612-125">Indirizzo di peering BGP per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="6b612-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="6b612-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="6b612-127">Il peso di peering BGP per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="6b612-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b612-128">-DefaultProfile</span></span>
<span data-ttu-id="6b612-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b612-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b612-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="6b612-130">-DeviceModel</span></span>
<span data-ttu-id="6b612-131">Modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="6b612-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="6b612-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="6b612-132">-DeviceVendor</span></span>
<span data-ttu-id="6b612-133">Il fornitore del dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="6b612-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="6b612-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="6b612-134">-IpAddress</span></span>
<span data-ttu-id="6b612-135">IPAddress per questo VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="6b612-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="6b612-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="6b612-137">Modello di dispositivo del dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="6b612-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="6b612-138">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6b612-138">-Location</span></span>
<span data-ttu-id="6b612-139">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b612-139">The resource location.</span></span>

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

### <span data-ttu-id="6b612-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b612-140">-Name</span></span>
<span data-ttu-id="6b612-141">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b612-141">The resource name.</span></span>

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

### <span data-ttu-id="6b612-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b612-142">-ResourceGroupName</span></span>
<span data-ttu-id="6b612-143">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b612-143">The resource name.</span></span>

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

### <span data-ttu-id="6b612-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b612-144">-Tag</span></span>
<span data-ttu-id="6b612-145">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6b612-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6b612-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="6b612-146">-VirtualWan</span></span>
<span data-ttu-id="6b612-147">VirtualWan a cui deve essere connessa la VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b612-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="6b612-148">-VirtualWanId</span></span>
<span data-ttu-id="6b612-149">ResourceId VirtualWan a cui deve essere connessa la VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b612-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="6b612-150">-VirtualWanName</span></span>
<span data-ttu-id="6b612-151">Il nome del VirtualWan a cui deve essere connesso VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b612-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b612-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="6b612-153">Il nome del gruppo di risorse di VirtualWan a cui deve essere connesso VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b612-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b612-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b612-154">-Confirm</span></span>
<span data-ttu-id="6b612-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b612-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b612-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b612-156">-WhatIf</span></span>
<span data-ttu-id="6b612-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b612-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b612-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b612-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b612-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b612-159">CommonParameters</span></span>
<span data-ttu-id="6b612-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b612-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b612-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b612-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b612-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b612-162">INPUTS</span></span>

### <span data-ttu-id="6b612-163">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6b612-163">None</span></span>

## <span data-ttu-id="6b612-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b612-164">OUTPUTS</span></span>

### <span data-ttu-id="6b612-165">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b612-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="6b612-166">Note</span><span class="sxs-lookup"><span data-stu-id="6b612-166">NOTES</span></span>

## <span data-ttu-id="6b612-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b612-167">RELATED LINKS</span></span>

[<span data-ttu-id="6b612-168">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b612-168">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="6b612-169">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b612-169">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="6b612-170">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b612-170">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
