---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: d4f0b908a229ee47472d40eefe60c5771c0147d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984366"
---
# <span data-ttu-id="f7197-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="f7197-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="f7197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7197-102">SYNOPSIS</span></span>
<span data-ttu-id="f7197-103">Crea una regola NAT in una VpnGateway che può essere associata a VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="f7197-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="f7197-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7197-104">SYNTAX</span></span>

### <span data-ttu-id="f7197-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7197-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7197-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f7197-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7197-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f7197-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7197-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f7197-108">DESCRIPTION</span></span>
<span data-ttu-id="f7197-109">Crea una regola NAT in vpngateway che può essere associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f7197-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="f7197-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7197-110">EXAMPLES</span></span>

### <span data-ttu-id="f7197-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7197-111">Example 1</span></span>

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

<span data-ttu-id="f7197-112">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale e un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7197-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="f7197-113">Verrà quindi creato VpnGateway nell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7197-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="f7197-114">Quindi, usando questo comando: New-AzVpnGatewayNatRule, è possibile creare una regola NAT e associarle a VpnGateway create.</span><span class="sxs-lookup"><span data-stu-id="f7197-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="f7197-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7197-115">PARAMETERS</span></span>

### <span data-ttu-id="f7197-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7197-116">-AsJob</span></span>
<span data-ttu-id="f7197-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f7197-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7197-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7197-118">-DefaultProfile</span></span>
<span data-ttu-id="f7197-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7197-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7197-120">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="f7197-120">-ExternalMapping</span></span>
<span data-ttu-id="f7197-121">Elenco di mapping esterni subnet di indirizzi IP privati per NAT</span><span class="sxs-lookup"><span data-stu-id="f7197-121">The list of private IP address subnet external mappings for NAT</span></span>

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

### <span data-ttu-id="f7197-122">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="f7197-122">-InternalMapping</span></span>
<span data-ttu-id="f7197-123">Elenco dei mapping interni della subnet dell'indirizzo IP privato per NAT</span><span class="sxs-lookup"><span data-stu-id="f7197-123">The list of private IP address subnet internal mappings for NAT</span></span>

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

### <span data-ttu-id="f7197-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f7197-124">-IpConfigurationId</span></span>
<span data-ttu-id="f7197-125">L'ID di configurazione IP a cui si applica questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="f7197-125">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="f7197-126">-Mode</span><span class="sxs-lookup"><span data-stu-id="f7197-126">-Mode</span></span>
<span data-ttu-id="f7197-127">Direzione NAT di origine di un NAT VPN</span><span class="sxs-lookup"><span data-stu-id="f7197-127">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="f7197-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f7197-128">-Name</span></span>
<span data-ttu-id="f7197-129">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f7197-129">The resource name.</span></span>

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

### <span data-ttu-id="f7197-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f7197-130">-ParentObject</span></span>
<span data-ttu-id="f7197-131">VpnGateway padre per questa regola NAT.</span><span class="sxs-lookup"><span data-stu-id="f7197-131">The parent VpnGateway for this NAT Rule.</span></span>

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

### <span data-ttu-id="f7197-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f7197-132">-ParentResourceId</span></span>
<span data-ttu-id="f7197-133">ID risorsa della vpngateway padre per questa regola NAT.</span><span class="sxs-lookup"><span data-stu-id="f7197-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

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

### <span data-ttu-id="f7197-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f7197-134">-ParentResourceName</span></span>
<span data-ttu-id="f7197-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7197-135">The resource group name.</span></span>

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

### <span data-ttu-id="f7197-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7197-136">-ResourceGroupName</span></span>
<span data-ttu-id="f7197-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7197-137">The resource group name.</span></span>

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

### <span data-ttu-id="f7197-138">-Type</span><span class="sxs-lookup"><span data-stu-id="f7197-138">-Type</span></span>
<span data-ttu-id="f7197-139">Tipo di regola NAT per NAT VPN</span><span class="sxs-lookup"><span data-stu-id="f7197-139">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="f7197-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7197-140">-Confirm</span></span>
<span data-ttu-id="f7197-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7197-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7197-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7197-142">-WhatIf</span></span>
<span data-ttu-id="f7197-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7197-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7197-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7197-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7197-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7197-145">CommonParameters</span></span>
<span data-ttu-id="f7197-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7197-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7197-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7197-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7197-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="f7197-148">INPUTS</span></span>

### <span data-ttu-id="f7197-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f7197-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="f7197-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f7197-150">System.String</span></span>

## <span data-ttu-id="f7197-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7197-151">OUTPUTS</span></span>

### <span data-ttu-id="f7197-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="f7197-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="f7197-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="f7197-153">NOTES</span></span>

## <span data-ttu-id="f7197-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7197-154">RELATED LINKS</span></span>
