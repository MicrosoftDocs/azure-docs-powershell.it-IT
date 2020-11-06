---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
ms.openlocfilehash: da023b7c0b060e9e263b6b0677065746568524b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513599"
---
# <span data-ttu-id="b04c4-101">Remove-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b04c4-101">Remove-AzureRmVpnConnection</span></span>

## <span data-ttu-id="b04c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b04c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b04c4-103">Rimuove un VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b04c4-103">Removes a VpnConnection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b04c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b04c4-104">SYNTAX</span></span>

### <span data-ttu-id="b04c4-105">ByVpnConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b04c4-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b04c4-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b04c4-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzureRmVpnConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b04c4-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b04c4-107">ByVpnConnectionObject</span></span>
```
Remove-AzureRmVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b04c4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b04c4-108">DESCRIPTION</span></span>
<span data-ttu-id="b04c4-109">Rimuove un VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b04c4-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="b04c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b04c4-110">EXAMPLES</span></span>

### <span data-ttu-id="b04c4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b04c4-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="b04c4-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un VpnSite in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="b04c4-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b04c4-113">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="b04c4-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b04c4-114">Dopo aver creato il gateway, viene collegato al VpnSite usando il comando New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b04c4-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="b04c4-115">Viene quindi rimossa la connessione usando il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="b04c4-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="b04c4-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b04c4-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzureRmVpnConnection
```

<span data-ttu-id="b04c4-117">Come l'esempio 1, ma ora rimuove la connessione usando l'oggetto piped da Get-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b04c4-117">Same as example 1, but it now removes the connection using the piped object from Get-AzureRmVpnConnection.</span></span>

## <span data-ttu-id="b04c4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b04c4-118">PARAMETERS</span></span>

### <span data-ttu-id="b04c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04c4-119">-DefaultProfile</span></span>
<span data-ttu-id="b04c4-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b04c4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04c4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b04c4-121">-Force</span></span>
<span data-ttu-id="b04c4-122">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="b04c4-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b04c4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b04c4-123">-InputObject</span></span>
<span data-ttu-id="b04c4-124">L'oggetto VpnConenction da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b04c4-124">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="b04c4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b04c4-125">-Name</span></span>
<span data-ttu-id="b04c4-126">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b04c4-126">The resource name.</span></span>

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

### <span data-ttu-id="b04c4-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b04c4-127">-ParentResourceName</span></span>
<span data-ttu-id="b04c4-128">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="b04c4-128">The parent resource name.</span></span>

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

### <span data-ttu-id="b04c4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b04c4-129">-PassThru</span></span>
<span data-ttu-id="b04c4-130">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b04c4-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b04c4-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b04c4-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b04c4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04c4-132">-ResourceGroupName</span></span>
<span data-ttu-id="b04c4-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b04c4-133">The resource group name.</span></span>

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

### <span data-ttu-id="b04c4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b04c4-134">-ResourceId</span></span>
<span data-ttu-id="b04c4-135">ID risorsa dell'oggetto VpnConenction da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b04c4-135">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="b04c4-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b04c4-136">-Confirm</span></span>
<span data-ttu-id="b04c4-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b04c4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b04c4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b04c4-138">-WhatIf</span></span>
<span data-ttu-id="b04c4-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b04c4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b04c4-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b04c4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b04c4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04c4-141">CommonParameters</span></span>
<span data-ttu-id="b04c4-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04c4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04c4-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b04c4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04c4-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b04c4-144">INPUTS</span></span>

### <span data-ttu-id="b04c4-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b04c4-145">System.String</span></span>

### <span data-ttu-id="b04c4-146">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b04c4-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="b04c4-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b04c4-147">OUTPUTS</span></span>

### <span data-ttu-id="b04c4-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b04c4-148">System.Boolean</span></span>

## <span data-ttu-id="b04c4-149">Note</span><span class="sxs-lookup"><span data-stu-id="b04c4-149">NOTES</span></span>

## <span data-ttu-id="b04c4-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b04c4-150">RELATED LINKS</span></span>
