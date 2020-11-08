---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192048"
---
# <span data-ttu-id="bea40-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="bea40-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="bea40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bea40-102">SYNOPSIS</span></span>
<span data-ttu-id="bea40-103">Il cmdlet Remove-AzExpressRouteGateway rimuove un gateway di Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bea40-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="bea40-104">Si tratta di un gateway specifico della connettività definita dal software di Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="bea40-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="bea40-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bea40-105">SYNTAX</span></span>

### <span data-ttu-id="bea40-106">ByExpressRouteGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bea40-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bea40-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="bea40-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bea40-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="bea40-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bea40-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bea40-109">DESCRIPTION</span></span>
<span data-ttu-id="bea40-110">Il cmdlet Remove-AzExpressRouteGateway rimuove un gateway di Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bea40-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="bea40-111">Si tratta di un gateway specifico della connettività definita dal software di Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="bea40-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="bea40-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bea40-112">EXAMPLES</span></span>

### <span data-ttu-id="bea40-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bea40-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="bea40-114">Questo esempio crea un gruppo di risorse, una WAN virtuale, un hub virtuale, un gateway ExpressRoute scalabile nel centro degli Stati Uniti e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="bea40-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="bea40-115">Per eliminare il prompt quando si elimina il gateway virtuale, usare il flag-Force.</span><span class="sxs-lookup"><span data-stu-id="bea40-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="bea40-116">Questo eliminerà ExpressRouteGateway e tutti gli ExpressRouteConnections allegati.</span><span class="sxs-lookup"><span data-stu-id="bea40-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="bea40-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bea40-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="bea40-118">Questo esempio crea un gruppo di risorse, una WAN virtuale, un hub virtuale, un gateway ExpressRoute scalabile in West Central US e lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="bea40-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="bea40-119">Questa operazione viene eseguita usando il piping di PowerShell, che usa l'oggetto ExpressRouteGateway restituito dal comando Get-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="bea40-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="bea40-120">Per eliminare il prompt quando si elimina il gateway virtuale, usare il flag-Force.</span><span class="sxs-lookup"><span data-stu-id="bea40-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="bea40-121">Questo eliminerà ExpressRouteGateway e tutti gli ExpressRouteConnections allegati.</span><span class="sxs-lookup"><span data-stu-id="bea40-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="bea40-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bea40-122">PARAMETERS</span></span>

### <span data-ttu-id="bea40-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea40-123">-DefaultProfile</span></span>
<span data-ttu-id="bea40-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bea40-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea40-125">-Force</span><span class="sxs-lookup"><span data-stu-id="bea40-125">-Force</span></span>
<span data-ttu-id="bea40-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="bea40-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bea40-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bea40-127">-InputObject</span></span>
<span data-ttu-id="bea40-128">Oggetto ExpressRouteGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bea40-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="bea40-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="bea40-129">-Name</span></span>
<span data-ttu-id="bea40-130">Il nome ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="bea40-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="bea40-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bea40-131">-PassThru</span></span>
<span data-ttu-id="bea40-132">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="bea40-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bea40-133">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="bea40-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bea40-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea40-134">-ResourceGroupName</span></span>
<span data-ttu-id="bea40-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bea40-135">The resource group name.</span></span>

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

### <span data-ttu-id="bea40-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bea40-136">-ResourceId</span></span>
<span data-ttu-id="bea40-137">ID risorsa di Azure per l'ExpressRouteGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bea40-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="bea40-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bea40-138">-Confirm</span></span>
<span data-ttu-id="bea40-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea40-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea40-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea40-140">-WhatIf</span></span>
<span data-ttu-id="bea40-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bea40-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bea40-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bea40-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea40-143">CommonParameters</span></span>
<span data-ttu-id="bea40-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea40-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea40-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea40-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bea40-146">INPUTS</span></span>

### <span data-ttu-id="bea40-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="bea40-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="bea40-148">System. String</span><span class="sxs-lookup"><span data-stu-id="bea40-148">System.String</span></span>

## <span data-ttu-id="bea40-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bea40-149">OUTPUTS</span></span>

### <span data-ttu-id="bea40-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bea40-150">System.Boolean</span></span>

## <span data-ttu-id="bea40-151">Note</span><span class="sxs-lookup"><span data-stu-id="bea40-151">NOTES</span></span>

## <span data-ttu-id="bea40-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bea40-152">RELATED LINKS</span></span>