---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e8b824e889965ca608a589c52d72c8f383678ca8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678223"
---
# <span data-ttu-id="49627-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="49627-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="49627-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49627-102">SYNOPSIS</span></span>
<span data-ttu-id="49627-103">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="49627-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="49627-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49627-104">SYNTAX</span></span>

### <span data-ttu-id="49627-105">ByVirtualHubNameByRemoteVirtualNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49627-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49627-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="49627-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49627-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="49627-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49627-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="49627-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49627-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="49627-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49627-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="49627-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49627-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49627-111">DESCRIPTION</span></span>
<span data-ttu-id="49627-112">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="49627-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="49627-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49627-113">EXAMPLES</span></span>

### <span data-ttu-id="49627-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49627-114">Example 1</span></span>

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
ProvisioningState    : Succeeded
```

<span data-ttu-id="49627-115">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="49627-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="49627-116">Verrà creata successivamente una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="49627-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="49627-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49627-117">PARAMETERS</span></span>

### <span data-ttu-id="49627-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49627-118">-AsJob</span></span>
<span data-ttu-id="49627-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="49627-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49627-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49627-120">-DefaultProfile</span></span>
<span data-ttu-id="49627-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49627-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49627-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="49627-122">-Name</span></span>
<span data-ttu-id="49627-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="49627-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49627-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="49627-124">-ParentObject</span></span>
<span data-ttu-id="49627-125">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="49627-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49627-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="49627-126">-ParentResourceId</span></span>
<span data-ttu-id="49627-127">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="49627-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49627-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="49627-128">-ParentResourceName</span></span>
<span data-ttu-id="49627-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49627-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49627-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="49627-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="49627-131">Rete virtuale remota a cui è connessa la connessione di rete virtuale Hub.</span><span class="sxs-lookup"><span data-stu-id="49627-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49627-132">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="49627-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="49627-133">Rete virtuale remota a cui è connessa la connessione di rete virtuale Hub.</span><span class="sxs-lookup"><span data-stu-id="49627-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49627-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49627-134">-ResourceGroupName</span></span>
<span data-ttu-id="49627-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49627-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49627-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49627-136">-Confirm</span></span>
<span data-ttu-id="49627-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49627-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49627-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49627-138">-WhatIf</span></span>
<span data-ttu-id="49627-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49627-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49627-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49627-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49627-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49627-141">CommonParameters</span></span>
<span data-ttu-id="49627-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49627-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49627-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49627-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49627-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49627-144">INPUTS</span></span>

### <span data-ttu-id="49627-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="49627-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="49627-146">System. String</span><span class="sxs-lookup"><span data-stu-id="49627-146">System.String</span></span>

## <span data-ttu-id="49627-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49627-147">OUTPUTS</span></span>

### <span data-ttu-id="49627-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="49627-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="49627-149">Note</span><span class="sxs-lookup"><span data-stu-id="49627-149">NOTES</span></span>

## <span data-ttu-id="49627-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49627-150">RELATED LINKS</span></span>

[<span data-ttu-id="49627-151">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="49627-151">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="49627-152">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="49627-152">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)