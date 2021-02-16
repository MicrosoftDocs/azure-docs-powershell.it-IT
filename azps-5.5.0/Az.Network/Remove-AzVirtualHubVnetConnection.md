---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: a6affc87ab0ace3e3808d43ac6bd9cfeb9496970
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193438"
---
# <span data-ttu-id="b9caf-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b9caf-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="b9caf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9caf-102">SYNOPSIS</span></span>
<span data-ttu-id="b9caf-103">Il cmdlet Remove-AzVirtualHubVnetConnection rimuove una connessione di rete virtuale di Azure che peera una VNET remota alla VNET hub.</span><span class="sxs-lookup"><span data-stu-id="b9caf-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="b9caf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9caf-104">SYNTAX</span></span>

### <span data-ttu-id="b9caf-105">ByHubVirtualNetworkConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9caf-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9caf-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b9caf-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9caf-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b9caf-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9caf-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b9caf-108">DESCRIPTION</span></span>
<span data-ttu-id="b9caf-109">Il cmdlet Remove-AzVirtualHubVnetConnection rimuove una connessione di rete virtuale di Azure che peera una VNET remota alla VNET hub.</span><span class="sxs-lookup"><span data-stu-id="b9caf-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="b9caf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9caf-110">EXAMPLES</span></span>

### <span data-ttu-id="b9caf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9caf-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="b9caf-112">Come descritto sopra, verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti centrali in tale gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="b9caf-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="b9caf-113">Successivamente verrà creata una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="b9caf-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="b9caf-114">Dopo la creazione, la connessione alla rete virtuale dell'hub viene rimossa usando il nome del gruppo di risorse, il nome dell'hub e il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="b9caf-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="b9caf-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b9caf-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="b9caf-116">Come descritto sopra, verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti centrali in tale gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="b9caf-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="b9caf-117">Successivamente verrà creata una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="b9caf-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="b9caf-118">Dopo la creazione della connessione alla rete virtuale dell'hub, la connessione alla rete virtuale dell'hub viene rimossa usando i piping di PowerShell sull'output di Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="b9caf-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="b9caf-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9caf-119">PARAMETERS</span></span>

### <span data-ttu-id="b9caf-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9caf-120">-AsJob</span></span>
<span data-ttu-id="b9caf-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b9caf-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9caf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9caf-122">-DefaultProfile</span></span>
<span data-ttu-id="b9caf-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9caf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9caf-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b9caf-124">-Force</span></span>
<span data-ttu-id="b9caf-125">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="b9caf-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b9caf-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9caf-126">-InputObject</span></span>
<span data-ttu-id="b9caf-127">La risorsa hubvirtualnetworkconnection da modificare.</span><span class="sxs-lookup"><span data-stu-id="b9caf-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9caf-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b9caf-128">-Name</span></span>
<span data-ttu-id="b9caf-129">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b9caf-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9caf-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b9caf-130">-ParentResourceName</span></span>
<span data-ttu-id="b9caf-131">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="b9caf-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9caf-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9caf-132">-PassThru</span></span>
<span data-ttu-id="b9caf-133">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b9caf-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b9caf-134">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b9caf-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9caf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9caf-135">-ResourceGroupName</span></span>
<span data-ttu-id="b9caf-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b9caf-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9caf-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9caf-137">-ResourceId</span></span>
<span data-ttu-id="b9caf-138">ID risorsa della risorsa hubvirtualnetworkconnection da modificare.</span><span class="sxs-lookup"><span data-stu-id="b9caf-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9caf-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9caf-139">-Confirm</span></span>
<span data-ttu-id="b9caf-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9caf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9caf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9caf-141">-WhatIf</span></span>
<span data-ttu-id="b9caf-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9caf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9caf-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9caf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9caf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9caf-144">CommonParameters</span></span>
<span data-ttu-id="b9caf-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9caf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9caf-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9caf-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9caf-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="b9caf-147">INPUTS</span></span>

### <span data-ttu-id="b9caf-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="b9caf-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="b9caf-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b9caf-149">System.String</span></span>

## <span data-ttu-id="b9caf-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9caf-150">OUTPUTS</span></span>

### <span data-ttu-id="b9caf-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9caf-151">System.Boolean</span></span>

## <span data-ttu-id="b9caf-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="b9caf-152">NOTES</span></span>

## <span data-ttu-id="b9caf-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9caf-153">RELATED LINKS</span></span>

[<span data-ttu-id="b9caf-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b9caf-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="b9caf-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b9caf-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
