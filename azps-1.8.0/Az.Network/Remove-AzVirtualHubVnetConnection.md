---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 16a17ed437194963f3cfd715a6e5364c8f4348c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678071"
---
# <span data-ttu-id="e20b5-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e20b5-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="e20b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e20b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e20b5-103">Il cmdlet Remove-AzVirtualHubVnetConnection consente di rimuovere una connessione di rete virtuale di Azure che peer un VNET remoto all'hub VNET.</span><span class="sxs-lookup"><span data-stu-id="e20b5-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="e20b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e20b5-104">SYNTAX</span></span>

### <span data-ttu-id="e20b5-105">ByHubVirtualNetworkConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e20b5-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e20b5-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="e20b5-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e20b5-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="e20b5-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e20b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e20b5-108">DESCRIPTION</span></span>
<span data-ttu-id="e20b5-109">Il cmdlet Remove-AzVirtualHubVnetConnection consente di rimuovere una connessione di rete virtuale di Azure che peer un VNET remoto all'hub VNET.</span><span class="sxs-lookup"><span data-stu-id="e20b5-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="e20b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e20b5-110">EXAMPLES</span></span>

### <span data-ttu-id="e20b5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e20b5-111">Example 1</span></span>

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

<span data-ttu-id="e20b5-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="e20b5-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e20b5-113">Verrà creata successivamente una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e20b5-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="e20b5-114">Dopo la creazione della connessione di rete virtuale Hub, la connessione di rete virtuale Hub viene rimossa usando il nome del gruppo di risorse, il nome dell'hub e il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="e20b5-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="e20b5-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e20b5-115">Example 2</span></span>

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

<span data-ttu-id="e20b5-116">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="e20b5-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e20b5-117">Verrà creata successivamente una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e20b5-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="e20b5-118">Dopo la creazione della connessione di rete virtuale Hub, la connessione di rete virtuale Hub viene rimossa usando il piping di PowerShell nell'output di Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="e20b5-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="e20b5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e20b5-119">PARAMETERS</span></span>

### <span data-ttu-id="e20b5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e20b5-120">-AsJob</span></span>
<span data-ttu-id="e20b5-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e20b5-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e20b5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e20b5-122">-DefaultProfile</span></span>
<span data-ttu-id="e20b5-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e20b5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e20b5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e20b5-124">-Force</span></span>
<span data-ttu-id="e20b5-125">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="e20b5-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e20b5-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e20b5-126">-InputObject</span></span>
<span data-ttu-id="e20b5-127">La risorsa hubvirtualnetworkconnection da modificare.</span><span class="sxs-lookup"><span data-stu-id="e20b5-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="e20b5-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e20b5-128">-Name</span></span>
<span data-ttu-id="e20b5-129">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e20b5-129">The resource name.</span></span>

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

### <span data-ttu-id="e20b5-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e20b5-130">-ParentResourceName</span></span>
<span data-ttu-id="e20b5-131">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="e20b5-131">The parent resource name.</span></span>

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

### <span data-ttu-id="e20b5-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e20b5-132">-PassThru</span></span>
<span data-ttu-id="e20b5-133">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e20b5-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e20b5-134">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e20b5-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e20b5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e20b5-135">-ResourceGroupName</span></span>
<span data-ttu-id="e20b5-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e20b5-136">The resource group name.</span></span>

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

### <span data-ttu-id="e20b5-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e20b5-137">-ResourceId</span></span>
<span data-ttu-id="e20b5-138">ID risorsa della risorsa hubvirtualnetworkconnection da modificare.</span><span class="sxs-lookup"><span data-stu-id="e20b5-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="e20b5-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e20b5-139">-Confirm</span></span>
<span data-ttu-id="e20b5-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e20b5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e20b5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e20b5-141">-WhatIf</span></span>
<span data-ttu-id="e20b5-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e20b5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e20b5-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e20b5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e20b5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e20b5-144">CommonParameters</span></span>
<span data-ttu-id="e20b5-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e20b5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e20b5-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e20b5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e20b5-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e20b5-147">INPUTS</span></span>

### <span data-ttu-id="e20b5-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e20b5-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="e20b5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e20b5-149">System.String</span></span>

## <span data-ttu-id="e20b5-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e20b5-150">OUTPUTS</span></span>

### <span data-ttu-id="e20b5-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e20b5-151">System.Boolean</span></span>

## <span data-ttu-id="e20b5-152">Note</span><span class="sxs-lookup"><span data-stu-id="e20b5-152">NOTES</span></span>

## <span data-ttu-id="e20b5-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e20b5-153">RELATED LINKS</span></span>

[<span data-ttu-id="e20b5-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e20b5-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e20b5-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e20b5-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)