---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: 45ec34bf437c64b96c3c46afa142d5e5b12f6010
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193535"
---
# <span data-ttu-id="f6750-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="f6750-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="f6750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6750-102">SYNOPSIS</span></span>
<span data-ttu-id="f6750-103">Crea una regola NAT in una VpnGateway che può essere associata a VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="f6750-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="f6750-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6750-104">SYNTAX</span></span>

### <span data-ttu-id="f6750-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6750-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6750-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f6750-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6750-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f6750-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6750-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f6750-108">DESCRIPTION</span></span>
<span data-ttu-id="f6750-109">Crea una regola NAT in vpngateway che può essere associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f6750-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="f6750-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6750-110">EXAMPLES</span></span>

### <span data-ttu-id="f6750-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f6750-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule
```

<span data-ttu-id="f6750-112">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale e un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f6750-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="f6750-113">Verrà quindi creata VpnGateway nell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f6750-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="f6750-114">Quindi, usando questo comando: New-AzVpnGatewayNatRule, la regola NAT può essere creata e associata a VpnGateway creata.</span><span class="sxs-lookup"><span data-stu-id="f6750-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="f6750-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6750-115">PARAMETERS</span></span>

### <span data-ttu-id="f6750-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6750-116">-AsJob</span></span>
<span data-ttu-id="f6750-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f6750-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6750-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6750-118">-DefaultProfile</span></span>
<span data-ttu-id="f6750-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6750-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6750-120">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="f6750-120">-ExternalMapping</span></span>
<span data-ttu-id="f6750-121">Elenco di mapping esterni subnet di indirizzi IP privati per NAT</span><span class="sxs-lookup"><span data-stu-id="f6750-121">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-122">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="f6750-122">-InternalMapping</span></span>
<span data-ttu-id="f6750-123">Elenco dei mapping interni della subnet dell'indirizzo IP privato per NAT</span><span class="sxs-lookup"><span data-stu-id="f6750-123">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f6750-124">-IpConfigurationId</span></span>
<span data-ttu-id="f6750-125">L'ID di configurazione IP a cui si applica questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="f6750-125">The IP Configuration ID this NAT rule applies to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-126">-Modalità</span><span class="sxs-lookup"><span data-stu-id="f6750-126">-Mode</span></span>
<span data-ttu-id="f6750-127">Direzione NAT di origine di un NAT VPN</span><span class="sxs-lookup"><span data-stu-id="f6750-127">The Source NAT direction of a VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EgressSnat, IngressSnat

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f6750-128">-Name</span></span>
<span data-ttu-id="f6750-129">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f6750-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f6750-130">-ParentObject</span></span>
<span data-ttu-id="f6750-131">VpnGateway padre per questa regola NAT.</span><span class="sxs-lookup"><span data-stu-id="f6750-131">The parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f6750-132">-ParentResourceId</span></span>
<span data-ttu-id="f6750-133">ID risorsa della vpngateway padre per questa regola NAT.</span><span class="sxs-lookup"><span data-stu-id="f6750-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f6750-134">-ParentResourceName</span></span>
<span data-ttu-id="f6750-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6750-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6750-136">-ResourceGroupName</span></span>
<span data-ttu-id="f6750-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6750-137">The resource group name.</span></span>

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

### <span data-ttu-id="f6750-138">-Type</span><span class="sxs-lookup"><span data-stu-id="f6750-138">-Type</span></span>
<span data-ttu-id="f6750-139">Tipo di regola NAT per NAT VPN</span><span class="sxs-lookup"><span data-stu-id="f6750-139">The type of NAT rule for VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6750-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6750-140">-Confirm</span></span>
<span data-ttu-id="f6750-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6750-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6750-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6750-142">-WhatIf</span></span>
<span data-ttu-id="f6750-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6750-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6750-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6750-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6750-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6750-145">CommonParameters</span></span>
<span data-ttu-id="f6750-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6750-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6750-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6750-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6750-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="f6750-148">INPUTS</span></span>

### <span data-ttu-id="f6750-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f6750-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="f6750-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f6750-150">System.String</span></span>

## <span data-ttu-id="f6750-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6750-151">OUTPUTS</span></span>

### <span data-ttu-id="f6750-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="f6750-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="f6750-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="f6750-153">NOTES</span></span>

## <span data-ttu-id="f6750-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6750-154">RELATED LINKS</span></span>
