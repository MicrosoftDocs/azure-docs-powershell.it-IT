---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: 60f68795e79e751dda75ae4d549d2b25a43392e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186798"
---
# <span data-ttu-id="34a3e-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="34a3e-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="34a3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="34a3e-103">Aggiorna una regola NAT associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="34a3e-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="34a3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34a3e-104">SYNTAX</span></span>

### <span data-ttu-id="34a3e-105">ByVpnGatewayNatRuleName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34a3e-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34a3e-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="34a3e-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a3e-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="34a3e-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34a3e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34a3e-108">DESCRIPTION</span></span>
<span data-ttu-id="34a3e-109">Il cmdlet **Update-AzVpnGatewayNatRule** aggiorna una regola NAT associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="34a3e-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="34a3e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34a3e-110">EXAMPLES</span></span>

### <span data-ttu-id="34a3e-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="34a3e-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> $natRule = Update-AzVpnGatewayNatRule -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy
PS C:\> Update-AzVpnGatewayNatRule -InputObject $natRule -Type Dynamic -Mode IngressSnat

Type                      : Dynamic
Mode                      : IngressSnat
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

<span data-ttu-id="34a3e-112">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale e un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="34a3e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="34a3e-113">Verrà quindi creata VpnGateway nell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="34a3e-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="34a3e-114">Creare quindi una nuova regola NAT associata a VpnGateway creata.</span><span class="sxs-lookup"><span data-stu-id="34a3e-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="34a3e-115">Usare questo comando: Update-AzVpnGatewayNatRule, aggiornare la regola NAT.</span><span class="sxs-lookup"><span data-stu-id="34a3e-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="34a3e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34a3e-116">PARAMETERS</span></span>

### <span data-ttu-id="34a3e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34a3e-117">-AsJob</span></span>
<span data-ttu-id="34a3e-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="34a3e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34a3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a3e-119">-DefaultProfile</span></span>
<span data-ttu-id="34a3e-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34a3e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a3e-121">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="34a3e-121">-ExternalMapping</span></span>
<span data-ttu-id="34a3e-122">Elenco di mapping esterni subnet di indirizzi IP privati per NAT</span><span class="sxs-lookup"><span data-stu-id="34a3e-122">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34a3e-123">-InputObject</span></span>
<span data-ttu-id="34a3e-124">Oggetto VpnGatewayNatRule da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="34a3e-124">The VpnGatewayNatRule object to update.</span></span>

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

### <span data-ttu-id="34a3e-125">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="34a3e-125">-InternalMapping</span></span>
<span data-ttu-id="34a3e-126">Elenco dei mapping interni della subnet dell'indirizzo IP privato per NAT</span><span class="sxs-lookup"><span data-stu-id="34a3e-126">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a3e-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="34a3e-127">-IpConfigurationId</span></span>
<span data-ttu-id="34a3e-128">L'ID di configurazione IP a cui si applica questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="34a3e-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="34a3e-129">-Modalità</span><span class="sxs-lookup"><span data-stu-id="34a3e-129">-Mode</span></span>
<span data-ttu-id="34a3e-130">Direzione NAT di origine di un NAT VPN</span><span class="sxs-lookup"><span data-stu-id="34a3e-130">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="34a3e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="34a3e-131">-Name</span></span>
<span data-ttu-id="34a3e-132">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="34a3e-132">The resource name.</span></span>

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

### <span data-ttu-id="34a3e-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="34a3e-133">-ParentResourceName</span></span>
<span data-ttu-id="34a3e-134">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="34a3e-134">The parent resource name.</span></span>

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

### <span data-ttu-id="34a3e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a3e-135">-ResourceGroupName</span></span>
<span data-ttu-id="34a3e-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34a3e-136">The resource group name.</span></span>

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

### <span data-ttu-id="34a3e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34a3e-137">-ResourceId</span></span>
<span data-ttu-id="34a3e-138">ID risorsa dell'oggetto VpnGatewayNatRule da eliminare.</span><span class="sxs-lookup"><span data-stu-id="34a3e-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a3e-139">-Type</span><span class="sxs-lookup"><span data-stu-id="34a3e-139">-Type</span></span>
<span data-ttu-id="34a3e-140">Tipo di regola NAT per NAT VPN</span><span class="sxs-lookup"><span data-stu-id="34a3e-140">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="34a3e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34a3e-141">-Confirm</span></span>
<span data-ttu-id="34a3e-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34a3e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a3e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a3e-143">-WhatIf</span></span>
<span data-ttu-id="34a3e-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34a3e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34a3e-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34a3e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a3e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a3e-146">CommonParameters</span></span>
<span data-ttu-id="34a3e-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a3e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a3e-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34a3e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a3e-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="34a3e-149">INPUTS</span></span>

### <span data-ttu-id="34a3e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="34a3e-150">System.String</span></span>

### <span data-ttu-id="34a3e-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="34a3e-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="34a3e-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34a3e-152">OUTPUTS</span></span>

### <span data-ttu-id="34a3e-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="34a3e-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="34a3e-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="34a3e-154">NOTES</span></span>

## <span data-ttu-id="34a3e-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34a3e-155">RELATED LINKS</span></span>
