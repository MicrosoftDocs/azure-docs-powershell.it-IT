---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 3be41be3c62b0676ea10e9fe7c9d89927c4de757
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021195"
---
# <span data-ttu-id="5ce01-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5ce01-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="5ce01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ce01-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce01-103">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce01-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="5ce01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ce01-104">SYNTAX</span></span>

### <span data-ttu-id="5ce01-105">ByVirtualHubNameByRemoteVirtualNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ce01-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce01-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5ce01-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce01-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="5ce01-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce01-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5ce01-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce01-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="5ce01-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce01-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5ce01-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ce01-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ce01-111">DESCRIPTION</span></span>
<span data-ttu-id="5ce01-112">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce01-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="5ce01-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ce01-113">EXAMPLES</span></span>

### <span data-ttu-id="5ce01-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ce01-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
```

<span data-ttu-id="5ce01-115">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce01-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="5ce01-116">Verrà creata successivamente una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="5ce01-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="5ce01-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ce01-117">PARAMETERS</span></span>

### <span data-ttu-id="5ce01-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ce01-118">-AsJob</span></span>
<span data-ttu-id="5ce01-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5ce01-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce01-120">-DefaultProfile</span></span>
<span data-ttu-id="5ce01-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce01-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-122">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5ce01-122">-EnableInternetSecurity</span></span>
<span data-ttu-id="5ce01-123">Abilitare la sicurezza Internet per la connessione</span><span class="sxs-lookup"><span data-stu-id="5ce01-123">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ce01-124">-Name</span></span>
<span data-ttu-id="5ce01-125">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ce01-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ce01-126">-ParentObject</span></span>
<span data-ttu-id="5ce01-127">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="5ce01-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ce01-128">-ParentResourceId</span></span>
<span data-ttu-id="5ce01-129">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="5ce01-129">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5ce01-130">-ParentResourceName</span></span>
<span data-ttu-id="5ce01-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ce01-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-132">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5ce01-132">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="5ce01-133">Rete virtuale remota a cui è connessa la connessione di rete virtuale Hub.</span><span class="sxs-lookup"><span data-stu-id="5ce01-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-134">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5ce01-134">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="5ce01-135">Rete virtuale remota a cui è connessa la connessione di rete virtuale Hub.</span><span class="sxs-lookup"><span data-stu-id="5ce01-135">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce01-136">-ResourceGroupName</span></span>
<span data-ttu-id="5ce01-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ce01-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ce01-138">-Confirm</span></span>
<span data-ttu-id="5ce01-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ce01-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce01-140">-WhatIf</span></span>
<span data-ttu-id="5ce01-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ce01-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce01-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ce01-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce01-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce01-143">CommonParameters</span></span>
<span data-ttu-id="5ce01-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce01-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce01-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ce01-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce01-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ce01-146">INPUTS</span></span>

### <span data-ttu-id="5ce01-147">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5ce01-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="5ce01-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5ce01-148">System.String</span></span>

## <span data-ttu-id="5ce01-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ce01-149">OUTPUTS</span></span>

### <span data-ttu-id="5ce01-150">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="5ce01-150">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="5ce01-151">Note</span><span class="sxs-lookup"><span data-stu-id="5ce01-151">NOTES</span></span>

## <span data-ttu-id="5ce01-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ce01-152">RELATED LINKS</span></span>

[<span data-ttu-id="5ce01-153">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5ce01-153">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="5ce01-154">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5ce01-154">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
