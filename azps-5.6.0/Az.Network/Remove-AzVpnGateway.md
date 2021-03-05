---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: c30ccf4f6e1f0d73112f5fc62ec6945baa9021a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001085"
---
# <span data-ttu-id="318de-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="318de-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="318de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="318de-102">SYNOPSIS</span></span>
<span data-ttu-id="318de-103">Il cmdlet Remove-AzVpnGateway rimuove un gateway VPN di Azure.</span><span class="sxs-lookup"><span data-stu-id="318de-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="318de-104">Si tratta di un gateway specifico della connettività definita dal software della WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="318de-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="318de-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="318de-105">SYNTAX</span></span>

### <span data-ttu-id="318de-106">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="318de-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="318de-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="318de-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="318de-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="318de-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="318de-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="318de-109">DESCRIPTION</span></span>
<span data-ttu-id="318de-110">Il cmdlet Remove-AzVpnGateway rimuove un gateway VPN di Azure.</span><span class="sxs-lookup"><span data-stu-id="318de-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="318de-111">Si tratta di un gateway specifico della connettività definita dal software della WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="318de-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="318de-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="318de-112">EXAMPLES</span></span>

### <span data-ttu-id="318de-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="318de-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="318de-114">Questo esempio crea un gruppo di risorse, una WAN virtuale, un hub virtuale, un gateway VPN scalabile negli Stati Uniti centrali e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="318de-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="318de-115">Per eliminare la richiesta di conferma dell'eliminazione del Gateway virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="318de-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="318de-116">Verranno eliminati vpngateway e tutti i VpnConnections associati.</span><span class="sxs-lookup"><span data-stu-id="318de-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="318de-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="318de-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="318de-118">Questo esempio crea un gruppo di risorse, una WAN virtuale, un hub virtuale, un gateway VPN scalabile negli Stati Uniti centrali e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="318de-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="318de-119">Questa eliminazione si verifica con l'uso delle funzionalità di piping di PowerShell, che usa l'oggetto VpnGateway restituito dal comando Get-AzVpnGateway>.</span><span class="sxs-lookup"><span data-stu-id="318de-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="318de-120">Per eliminare la richiesta di conferma dell'eliminazione del Gateway virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="318de-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="318de-121">Verranno eliminati vpngateway e tutti i VpnConnections associati.</span><span class="sxs-lookup"><span data-stu-id="318de-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="318de-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="318de-122">PARAMETERS</span></span>

### <span data-ttu-id="318de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318de-123">-DefaultProfile</span></span>
<span data-ttu-id="318de-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="318de-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318de-125">-Force</span><span class="sxs-lookup"><span data-stu-id="318de-125">-Force</span></span>
<span data-ttu-id="318de-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="318de-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="318de-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="318de-127">-InputObject</span></span>
<span data-ttu-id="318de-128">Oggetto vpnGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="318de-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="318de-129">-Name</span><span class="sxs-lookup"><span data-stu-id="318de-129">-Name</span></span>
<span data-ttu-id="318de-130">Nome vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="318de-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318de-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="318de-131">-PassThru</span></span>
<span data-ttu-id="318de-132">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="318de-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="318de-133">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="318de-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="318de-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318de-134">-ResourceGroupName</span></span>
<span data-ttu-id="318de-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="318de-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318de-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="318de-136">-ResourceId</span></span>
<span data-ttu-id="318de-137">ID della risorsa Azure per vpnGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="318de-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318de-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="318de-138">-Confirm</span></span>
<span data-ttu-id="318de-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="318de-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="318de-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318de-140">-WhatIf</span></span>
<span data-ttu-id="318de-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="318de-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="318de-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="318de-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="318de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318de-143">CommonParameters</span></span>
<span data-ttu-id="318de-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318de-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318de-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318de-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="318de-146">INPUTS</span></span>

### <span data-ttu-id="318de-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="318de-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="318de-148">System.String</span><span class="sxs-lookup"><span data-stu-id="318de-148">System.String</span></span>

## <span data-ttu-id="318de-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="318de-149">OUTPUTS</span></span>

### <span data-ttu-id="318de-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="318de-150">System.Boolean</span></span>

## <span data-ttu-id="318de-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="318de-151">NOTES</span></span>

## <span data-ttu-id="318de-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="318de-152">RELATED LINKS</span></span>

[<span data-ttu-id="318de-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="318de-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="318de-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="318de-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="318de-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="318de-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
