---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191694"
---
# <span data-ttu-id="34314-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="34314-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="34314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34314-102">SYNOPSIS</span></span>
<span data-ttu-id="34314-103">Rimuove una VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="34314-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="34314-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34314-104">SYNTAX</span></span>

### <span data-ttu-id="34314-105">ByVpnConnectionName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34314-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34314-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="34314-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34314-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="34314-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34314-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34314-108">DESCRIPTION</span></span>
<span data-ttu-id="34314-109">Rimuove una VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="34314-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="34314-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34314-110">EXAMPLES</span></span>

### <span data-ttu-id="34314-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34314-111">Example 1</span></span>
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
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="34314-112">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un sito Vpn negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="34314-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="34314-113">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="34314-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="34314-114">Una volta creato, il gateway viene connesso a VpnSite usando il comando New-AzVpnConnection></span><span class="sxs-lookup"><span data-stu-id="34314-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="34314-115">La connessione viene quindi rimossa con il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="34314-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="34314-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="34314-116">Example 2</span></span>

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
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="34314-117">Come l'esempio 1, ma ora rimuove la connessione usando l'oggetto piped da Get-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="34314-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="34314-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34314-118">PARAMETERS</span></span>

### <span data-ttu-id="34314-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34314-119">-DefaultProfile</span></span>
<span data-ttu-id="34314-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34314-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34314-121">-Force</span><span class="sxs-lookup"><span data-stu-id="34314-121">-Force</span></span>
<span data-ttu-id="34314-122">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="34314-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="34314-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34314-123">-InputObject</span></span>
<span data-ttu-id="34314-124">L'oggetto VpnConnection da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="34314-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34314-125">-Name</span><span class="sxs-lookup"><span data-stu-id="34314-125">-Name</span></span>
<span data-ttu-id="34314-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="34314-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34314-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="34314-127">-ParentResourceName</span></span>
<span data-ttu-id="34314-128">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="34314-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34314-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34314-129">-PassThru</span></span>
<span data-ttu-id="34314-130">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="34314-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="34314-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="34314-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34314-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34314-132">-ResourceGroupName</span></span>
<span data-ttu-id="34314-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34314-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34314-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34314-134">-ResourceId</span></span>
<span data-ttu-id="34314-135">ID risorsa dell'oggetto VpnConnection da eliminare.</span><span class="sxs-lookup"><span data-stu-id="34314-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34314-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34314-136">-Confirm</span></span>
<span data-ttu-id="34314-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34314-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34314-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34314-138">-WhatIf</span></span>
<span data-ttu-id="34314-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34314-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34314-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34314-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34314-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34314-141">CommonParameters</span></span>
<span data-ttu-id="34314-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34314-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34314-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34314-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34314-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="34314-144">INPUTS</span></span>

### <span data-ttu-id="34314-145">System.String</span><span class="sxs-lookup"><span data-stu-id="34314-145">System.String</span></span>

### <span data-ttu-id="34314-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="34314-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="34314-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34314-147">OUTPUTS</span></span>

### <span data-ttu-id="34314-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34314-148">System.Boolean</span></span>

## <span data-ttu-id="34314-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="34314-149">NOTES</span></span>

## <span data-ttu-id="34314-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34314-150">RELATED LINKS</span></span>

[<span data-ttu-id="34314-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="34314-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="34314-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="34314-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="34314-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="34314-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
