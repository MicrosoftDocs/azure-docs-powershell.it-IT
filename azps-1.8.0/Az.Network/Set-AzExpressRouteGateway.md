---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: c3d311cc091026bcd08225e5a11a8232102a03a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677975"
---
# <span data-ttu-id="7a0f4-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7a0f4-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="7a0f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0f4-103">Aggiorna un gateway ExpressRoute scalabile.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="7a0f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a0f4-104">SYNTAX</span></span>

### <span data-ttu-id="7a0f4-105">ByExpressRouteGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a0f4-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0f4-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7a0f4-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a0f4-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0f4-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a0f4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a0f4-108">DESCRIPTION</span></span>

<span data-ttu-id="7a0f4-109">Set-AzExpressRouteGateway aggiorna le unità di misura per ExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7a0f4-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="7a0f4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a0f4-110">EXAMPLES</span></span>

### <span data-ttu-id="7a0f4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a0f4-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="7a0f4-112">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7a0f4-113">Un gateway ExpressRoute verrà creato in seguito nell'hub virtuale con due unità di scala che verranno quindi modificate in 3 unità di misura</span><span class="sxs-lookup"><span data-stu-id="7a0f4-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="7a0f4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a0f4-114">PARAMETERS</span></span>

### <span data-ttu-id="7a0f4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a0f4-115">-AsJob</span></span>
<span data-ttu-id="7a0f4-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7a0f4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a0f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0f4-117">-DefaultProfile</span></span>
<span data-ttu-id="7a0f4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a0f4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a0f4-119">-InputObject</span></span>
<span data-ttu-id="7a0f4-120">ExpressRouteGateway che deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="7a0f4-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7a0f4-121">-MaxScaleUnits</span></span>
<span data-ttu-id="7a0f4-122">Numero massimo di unità di scala per questo ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7a0f4-123">Intervallo valido > 2</span><span class="sxs-lookup"><span data-stu-id="7a0f4-123">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f4-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7a0f4-124">-MinScaleUnits</span></span>
<span data-ttu-id="7a0f4-125">Il numero minimo di unità di scala per questo ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7a0f4-126">Intervallo valido > 2</span><span class="sxs-lookup"><span data-stu-id="7a0f4-126">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a0f4-127">-Name</span></span>
<span data-ttu-id="7a0f4-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0f4-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a0f4-130">Il nome del gruppo di risorse di ExpressRouteGateway da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="7a0f4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0f4-131">-ResourceId</span></span>
<span data-ttu-id="7a0f4-132">ID dell'ExpressRouteGateway che deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a0f4-133">-Tag</span></span>
<span data-ttu-id="7a0f4-134">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f4-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a0f4-135">-Confirm</span></span>
<span data-ttu-id="7a0f4-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0f4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0f4-137">-WhatIf</span></span>
<span data-ttu-id="7a0f4-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0f4-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0f4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0f4-140">CommonParameters</span></span>
<span data-ttu-id="7a0f4-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0f4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0f4-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0f4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0f4-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a0f4-143">INPUTS</span></span>

### <span data-ttu-id="7a0f4-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7a0f4-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="7a0f4-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7a0f4-145">System.String</span></span>

## <span data-ttu-id="7a0f4-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a0f4-146">OUTPUTS</span></span>

### <span data-ttu-id="7a0f4-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7a0f4-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="7a0f4-148">Note</span><span class="sxs-lookup"><span data-stu-id="7a0f4-148">NOTES</span></span>

## <span data-ttu-id="7a0f4-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a0f4-149">RELATED LINKS</span></span>