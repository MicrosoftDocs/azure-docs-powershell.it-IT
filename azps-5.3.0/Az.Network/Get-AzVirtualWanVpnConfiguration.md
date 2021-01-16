---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: 6e67f192cab1d1183d8c8cfd1a38f6c398311bf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379760"
---
# <span data-ttu-id="5dfaf-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="5dfaf-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="5dfaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfaf-103">Ottiene la configurazione VPN per un sottoinsieme di VpnSites connesso a questa WAN tramite VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="5dfaf-104">Carica la configurazione VPN generata in un BLOB di archiviazione specificato dal cliente.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="5dfaf-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dfaf-105">SYNTAX</span></span>

### <span data-ttu-id="5dfaf-106">ByVirtualWanNameByVpnSiteObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5dfaf-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dfaf-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5dfaf-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dfaf-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="5dfaf-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dfaf-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5dfaf-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dfaf-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="5dfaf-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dfaf-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5dfaf-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dfaf-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dfaf-112">DESCRIPTION</span></span>
<span data-ttu-id="5dfaf-113">Ottiene la configurazione VPN per un sottoinsieme di VpnSites connesso a questa WAN tramite VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="5dfaf-114">Carica la configurazione VPN generata in un BLOB di archiviazione specificato dal cliente.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="5dfaf-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dfaf-115">EXAMPLES</span></span>

### <span data-ttu-id="5dfaf-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5dfaf-116">Example 1</span></span>
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

<span data-ttu-id="5dfaf-117">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un VpnSite in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5dfaf-118">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5dfaf-119">Dopo aver creato il gateway, viene collegato al VpnSite usando il comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="5dfaf-120">La configurazione viene quindi scaricata usando questo unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="5dfaf-121">Se il unifiedgroup è riuscito, la configurazione del download verrà scritta nel BLOB indicato da SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="5dfaf-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dfaf-122">PARAMETERS</span></span>

### <span data-ttu-id="5dfaf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfaf-123">-DefaultProfile</span></span>
<span data-ttu-id="5dfaf-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dfaf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dfaf-125">-InputObject</span></span>
<span data-ttu-id="5dfaf-126">Oggetto sito VPN da modificare</span><span class="sxs-lookup"><span data-stu-id="5dfaf-126">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="5dfaf-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="5dfaf-127">-Name</span></span>
<span data-ttu-id="5dfaf-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-128">The resource name.</span></span>

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

### <span data-ttu-id="5dfaf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dfaf-129">-ResourceGroupName</span></span>
<span data-ttu-id="5dfaf-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-130">The resource group name.</span></span>

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

### <span data-ttu-id="5dfaf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dfaf-131">-ResourceId</span></span>
<span data-ttu-id="5dfaf-132">ID risorsa Azure per la rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="5dfaf-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="5dfaf-133">-StorageSasUrl</span></span>
<span data-ttu-id="5dfaf-134">URL SAS per il percorso di archiviazione in cui deve essere generata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="5dfaf-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5dfaf-135">-VpnSite</span></span>
<span data-ttu-id="5dfaf-136">Elenco di ID delle risorse di VpnSite per cui generare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-136">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="5dfaf-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="5dfaf-137">-VpnSiteId</span></span>
<span data-ttu-id="5dfaf-138">Elenco di ID delle risorse di VpnSite per cui generare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-138">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="5dfaf-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5dfaf-139">-Confirm</span></span>
<span data-ttu-id="5dfaf-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dfaf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dfaf-141">-WhatIf</span></span>
<span data-ttu-id="5dfaf-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dfaf-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dfaf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfaf-144">CommonParameters</span></span>
<span data-ttu-id="5dfaf-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfaf-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dfaf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfaf-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dfaf-147">INPUTS</span></span>

### <span data-ttu-id="5dfaf-148">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="5dfaf-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="5dfaf-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5dfaf-149">System.String</span></span>

## <span data-ttu-id="5dfaf-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dfaf-150">OUTPUTS</span></span>

### <span data-ttu-id="5dfaf-151">Microsoft. Azure. Commands. Network. Models. PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="5dfaf-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="5dfaf-152">Note</span><span class="sxs-lookup"><span data-stu-id="5dfaf-152">NOTES</span></span>

## <span data-ttu-id="5dfaf-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dfaf-153">RELATED LINKS</span></span>
