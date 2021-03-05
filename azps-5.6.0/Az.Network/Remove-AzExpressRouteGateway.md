---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 77c41a4565a517a51b02c904d79953d79e908c39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996392"
---
# <span data-ttu-id="33763-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="33763-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="33763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33763-102">SYNOPSIS</span></span>
<span data-ttu-id="33763-103">Il cmdlet Remove-AzExpressRouteGateway rimuove un gateway di Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="33763-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="33763-104">Si tratta di un gateway specifico della connettività definita dal software della WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="33763-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="33763-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33763-105">SYNTAX</span></span>

### <span data-ttu-id="33763-106">ByExpressRouteGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33763-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33763-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="33763-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33763-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="33763-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33763-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33763-109">DESCRIPTION</span></span>
<span data-ttu-id="33763-110">Il cmdlet Remove-AzExpressRouteGateway rimuove un gateway di Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="33763-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="33763-111">Si tratta di un gateway specifico della connettività definita dal software della WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="33763-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="33763-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33763-112">EXAMPLES</span></span>

### <span data-ttu-id="33763-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="33763-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="33763-114">Questo esempio crea un gruppo di risorse, una WAN virtuale, un hub virtuale, un gateway ExpressRoute scalabile negli Stati Uniti centrali e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="33763-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="33763-115">Per eliminare la richiesta di conferma dell'eliminazione del Gateway virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="33763-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="33763-116">Verranno eliminati lo ExpressRouteGateway e tutte le connessioni ExpressRouteConnection ad esso associate.</span><span class="sxs-lookup"><span data-stu-id="33763-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="33763-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="33763-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="33763-118">Questo esempio crea un gruppo di risorse, una WAN virtuale, un hub virtuale, un gateway ExpressRoute scalabile negli Stati Uniti centrali occidentali e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="33763-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="33763-119">Questa eliminazione si verifica con l'uso delle piping di PowerShell, che usa l'oggetto ExpressRouteGateway restituito dal comando Get-AzExpressRouteGateway></span><span class="sxs-lookup"><span data-stu-id="33763-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="33763-120">Per eliminare la richiesta di conferma dell'eliminazione del Gateway virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="33763-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="33763-121">Verranno eliminati lo ExpressRouteGateway e tutte le connessioni ExpressRouteConnection ad esso associate.</span><span class="sxs-lookup"><span data-stu-id="33763-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="33763-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33763-122">PARAMETERS</span></span>

### <span data-ttu-id="33763-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33763-123">-DefaultProfile</span></span>
<span data-ttu-id="33763-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33763-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33763-125">-Force</span><span class="sxs-lookup"><span data-stu-id="33763-125">-Force</span></span>
<span data-ttu-id="33763-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="33763-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="33763-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33763-127">-InputObject</span></span>
<span data-ttu-id="33763-128">Oggetto ExpressRouteGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="33763-128">The ExpressRouteGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33763-129">-Name</span><span class="sxs-lookup"><span data-stu-id="33763-129">-Name</span></span>
<span data-ttu-id="33763-130">Nome di ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="33763-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33763-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33763-131">-PassThru</span></span>
<span data-ttu-id="33763-132">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="33763-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33763-133">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="33763-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33763-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33763-134">-ResourceGroupName</span></span>
<span data-ttu-id="33763-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33763-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33763-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33763-136">-ResourceId</span></span>
<span data-ttu-id="33763-137">ID della risorsa Azure per ExpressRouteGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="33763-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33763-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33763-138">-Confirm</span></span>
<span data-ttu-id="33763-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33763-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33763-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33763-140">-WhatIf</span></span>
<span data-ttu-id="33763-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33763-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33763-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33763-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33763-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33763-143">CommonParameters</span></span>
<span data-ttu-id="33763-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33763-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33763-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33763-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33763-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="33763-146">INPUTS</span></span>

### <span data-ttu-id="33763-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="33763-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="33763-148">System.String</span><span class="sxs-lookup"><span data-stu-id="33763-148">System.String</span></span>

## <span data-ttu-id="33763-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33763-149">OUTPUTS</span></span>

### <span data-ttu-id="33763-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33763-150">System.Boolean</span></span>

## <span data-ttu-id="33763-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="33763-151">NOTES</span></span>

## <span data-ttu-id="33763-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33763-152">RELATED LINKS</span></span>
