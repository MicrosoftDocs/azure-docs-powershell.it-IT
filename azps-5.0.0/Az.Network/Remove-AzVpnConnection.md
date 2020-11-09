---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301789"
---
# <span data-ttu-id="40801-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="40801-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="40801-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40801-102">SYNOPSIS</span></span>
<span data-ttu-id="40801-103">Rimuove un VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="40801-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="40801-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40801-104">SYNTAX</span></span>

### <span data-ttu-id="40801-105">ByVpnConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40801-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40801-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="40801-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40801-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="40801-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40801-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40801-108">DESCRIPTION</span></span>
<span data-ttu-id="40801-109">Rimuove un VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="40801-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="40801-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40801-110">EXAMPLES</span></span>

### <span data-ttu-id="40801-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40801-111">Example 1</span></span>
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

<span data-ttu-id="40801-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un VpnSite in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="40801-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="40801-113">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="40801-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="40801-114">Dopo aver creato il gateway, viene collegato al VpnSite usando il comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="40801-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="40801-115">Viene quindi rimossa la connessione usando il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="40801-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="40801-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="40801-116">Example 2</span></span>

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

<span data-ttu-id="40801-117">Come l'esempio 1, ma ora rimuove la connessione usando l'oggetto piped da Get-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="40801-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="40801-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40801-118">PARAMETERS</span></span>

### <span data-ttu-id="40801-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40801-119">-DefaultProfile</span></span>
<span data-ttu-id="40801-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40801-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40801-121">-Force</span><span class="sxs-lookup"><span data-stu-id="40801-121">-Force</span></span>
<span data-ttu-id="40801-122">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="40801-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="40801-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40801-123">-InputObject</span></span>
<span data-ttu-id="40801-124">L'oggetto VpnConnection da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="40801-124">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="40801-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="40801-125">-Name</span></span>
<span data-ttu-id="40801-126">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="40801-126">The resource name.</span></span>

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

### <span data-ttu-id="40801-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="40801-127">-ParentResourceName</span></span>
<span data-ttu-id="40801-128">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="40801-128">The parent resource name.</span></span>

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

### <span data-ttu-id="40801-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40801-129">-PassThru</span></span>
<span data-ttu-id="40801-130">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="40801-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="40801-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="40801-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="40801-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40801-132">-ResourceGroupName</span></span>
<span data-ttu-id="40801-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40801-133">The resource group name.</span></span>

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

### <span data-ttu-id="40801-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40801-134">-ResourceId</span></span>
<span data-ttu-id="40801-135">ID risorsa dell'oggetto VpnConnection da eliminare.</span><span class="sxs-lookup"><span data-stu-id="40801-135">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="40801-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40801-136">-Confirm</span></span>
<span data-ttu-id="40801-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40801-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40801-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40801-138">-WhatIf</span></span>
<span data-ttu-id="40801-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40801-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40801-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40801-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40801-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40801-141">CommonParameters</span></span>
<span data-ttu-id="40801-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40801-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40801-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40801-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40801-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40801-144">INPUTS</span></span>

### <span data-ttu-id="40801-145">System. String</span><span class="sxs-lookup"><span data-stu-id="40801-145">System.String</span></span>

### <span data-ttu-id="40801-146">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="40801-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="40801-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40801-147">OUTPUTS</span></span>

### <span data-ttu-id="40801-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40801-148">System.Boolean</span></span>

## <span data-ttu-id="40801-149">Note</span><span class="sxs-lookup"><span data-stu-id="40801-149">NOTES</span></span>

## <span data-ttu-id="40801-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40801-150">RELATED LINKS</span></span>

[<span data-ttu-id="40801-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="40801-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="40801-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="40801-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="40801-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="40801-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
