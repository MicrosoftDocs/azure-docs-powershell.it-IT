---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: e5ada12a6fd55cc882ba5b9ba33c817f7eb4daab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972686"
---
# <span data-ttu-id="cca16-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="cca16-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="cca16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca16-102">SYNOPSIS</span></span>
<span data-ttu-id="cca16-103">Ottiene la configurazione Vpn per un sottoinsieme di VpnSites connessi a questa WAN tramite VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="cca16-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="cca16-104">Carica la configurazione Vpn generata in un BLOB di archiviazione specificato dal cliente.</span><span class="sxs-lookup"><span data-stu-id="cca16-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="cca16-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cca16-105">SYNTAX</span></span>

### <span data-ttu-id="cca16-106">ByVirtualWanNameByVpnSiteObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cca16-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca16-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="cca16-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca16-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="cca16-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca16-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="cca16-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca16-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="cca16-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca16-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="cca16-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cca16-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cca16-112">DESCRIPTION</span></span>
<span data-ttu-id="cca16-113">Ottiene la configurazione Vpn per un sottoinsieme di VpnSites connessi a questa WAN tramite VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="cca16-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="cca16-114">Carica la configurazione Vpn generata in un BLOB di archiviazione specificato dal cliente.</span><span class="sxs-lookup"><span data-stu-id="cca16-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="cca16-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cca16-115">EXAMPLES</span></span>

### <span data-ttu-id="cca16-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cca16-116">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="cca16-117">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un sito Vpn negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="cca16-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cca16-118">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cca16-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="cca16-119">Una volta creato, il gateway viene connesso a VpnSite usando il comando New-AzVpnConnection></span><span class="sxs-lookup"><span data-stu-id="cca16-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="cca16-120">La configurazione viene quindi scaricata con questo commandlet.</span><span class="sxs-lookup"><span data-stu-id="cca16-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="cca16-121">Se il commandlet ha esito positivo, la configurazione del download verrà scritta nel BLOB indicato da SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="cca16-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="cca16-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cca16-122">PARAMETERS</span></span>

### <span data-ttu-id="cca16-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca16-123">-DefaultProfile</span></span>
<span data-ttu-id="cca16-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cca16-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca16-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cca16-125">-InputObject</span></span>
<span data-ttu-id="cca16-126">Oggetto sito vpn da modificare</span><span class="sxs-lookup"><span data-stu-id="cca16-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cca16-127">-Name</span><span class="sxs-lookup"><span data-stu-id="cca16-127">-Name</span></span>
<span data-ttu-id="cca16-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cca16-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca16-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca16-129">-ResourceGroupName</span></span>
<span data-ttu-id="cca16-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cca16-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca16-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cca16-131">-ResourceId</span></span>
<span data-ttu-id="cca16-132">ID della risorsa Azure per la wan virtuale.</span><span class="sxs-lookup"><span data-stu-id="cca16-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca16-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="cca16-133">-StorageSasUrl</span></span>
<span data-ttu-id="cca16-134">URL della firma di accesso condiviso per la posizione di archiviazione in cui deve essere generata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="cca16-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="cca16-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="cca16-135">-VpnSite</span></span>
<span data-ttu-id="cca16-136">Elenco degli ID di risorse VpnSite per cui generare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="cca16-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca16-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="cca16-137">-VpnSiteId</span></span>
<span data-ttu-id="cca16-138">Elenco degli ID di risorse VpnSite per cui generare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="cca16-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca16-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cca16-139">-Confirm</span></span>
<span data-ttu-id="cca16-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cca16-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cca16-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cca16-141">-WhatIf</span></span>
<span data-ttu-id="cca16-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cca16-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cca16-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cca16-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cca16-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca16-144">CommonParameters</span></span>
<span data-ttu-id="cca16-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca16-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca16-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cca16-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca16-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="cca16-147">INPUTS</span></span>

### <span data-ttu-id="cca16-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cca16-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="cca16-149">System.String</span><span class="sxs-lookup"><span data-stu-id="cca16-149">System.String</span></span>

## <span data-ttu-id="cca16-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cca16-150">OUTPUTS</span></span>

### <span data-ttu-id="cca16-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="cca16-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="cca16-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="cca16-152">NOTES</span></span>

## <span data-ttu-id="cca16-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cca16-153">RELATED LINKS</span></span>
