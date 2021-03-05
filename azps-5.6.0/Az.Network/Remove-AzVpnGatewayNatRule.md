---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 5c91ba0dbca881e7e6a6909ef1b7200adf2ba1ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990008"
---
# <span data-ttu-id="a7f3a-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="a7f3a-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="a7f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f3a-103">Rimuove una regola NAT associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="a7f3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7f3a-104">SYNTAX</span></span>

### <span data-ttu-id="a7f3a-105">ByVpnGatewayNatRuleName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7f3a-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f3a-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="a7f3a-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f3a-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="a7f3a-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f3a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7f3a-108">DESCRIPTION</span></span>
<span data-ttu-id="a7f3a-109">Rimuove una regola NAT associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="a7f3a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7f3a-110">EXAMPLES</span></span>

### <span data-ttu-id="a7f3a-111">Esempio1</span><span class="sxs-lookup"><span data-stu-id="a7f3a-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="a7f3a-112">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale, una VpnGateway e una regola NAT associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="a7f3a-113">Quindi rimuove la regola NAT con il nome della regola NAT.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="a7f3a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7f3a-114">PARAMETERS</span></span>

### <span data-ttu-id="a7f3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f3a-115">-DefaultProfile</span></span>
<span data-ttu-id="a7f3a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f3a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a7f3a-117">-Force</span></span>
<span data-ttu-id="a7f3a-118">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="a7f3a-118">Do not ask for confirmation if you want to delete a resource</span></span>

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

### <span data-ttu-id="a7f3a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7f3a-119">-InputObject</span></span>
<span data-ttu-id="a7f3a-120">Oggetto VpnGatewayNatRule da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-120">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f3a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a7f3a-121">-Name</span></span>
<span data-ttu-id="a7f3a-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f3a-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a7f3a-123">-ParentResourceName</span></span>
<span data-ttu-id="a7f3a-124">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f3a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7f3a-125">-PassThru</span></span>
<span data-ttu-id="a7f3a-126">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="a7f3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="a7f3a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f3a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7f3a-129">-ResourceId</span></span>
<span data-ttu-id="a7f3a-130">ID risorsa dell'oggetto VpnGatewayNatRule da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f3a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7f3a-131">-Confirm</span></span>
<span data-ttu-id="a7f3a-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f3a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f3a-133">-WhatIf</span></span>
<span data-ttu-id="a7f3a-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f3a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f3a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f3a-136">CommonParameters</span></span>
<span data-ttu-id="a7f3a-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f3a-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7f3a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f3a-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7f3a-139">INPUTS</span></span>

### <span data-ttu-id="a7f3a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a7f3a-140">System.String</span></span>

### <span data-ttu-id="a7f3a-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="a7f3a-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="a7f3a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7f3a-142">OUTPUTS</span></span>

### <span data-ttu-id="a7f3a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7f3a-143">System.Boolean</span></span>

## <span data-ttu-id="a7f3a-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7f3a-144">NOTES</span></span>

## <span data-ttu-id="a7f3a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7f3a-145">RELATED LINKS</span></span>
