---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 9eba38f32d0bcb7414ddfeecc5ace8ed7ade4ca0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677903"
---
# <span data-ttu-id="e4982-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e4982-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="e4982-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4982-102">SYNOPSIS</span></span>
<span data-ttu-id="e4982-103">Imposta i parametri IPSec VPN per il gateway di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="e4982-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="e4982-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4982-104">SYNTAX</span></span>

### <span data-ttu-id="e4982-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4982-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4982-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e4982-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4982-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4982-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4982-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4982-108">DESCRIPTION</span></span>
<span data-ttu-id="e4982-109">Il cmdlet **set-AzVpnClientIpsecParameter** imposta i parametri IPSec VPN per il gateway di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="e4982-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="e4982-110">Quando viene creato il gateway di rete virtuale, viene impostato il set di criteri IPSec VPN predefiniti sul gateway.</span><span class="sxs-lookup"><span data-stu-id="e4982-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="e4982-111">Nel caso in cui l'utente del sito voglia usare determinati criteri IPSec personalizzati per la connessione al gateway VPN, l'utente deve prima impostare il criterio IPSec sul gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="e4982-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="e4982-112">**Set-AzVpnClientIpsecParameter** offre un modo per farlo.</span><span class="sxs-lookup"><span data-stu-id="e4982-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="e4982-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4982-113">EXAMPLES</span></span>

### <span data-ttu-id="e4982-114">Esempio 1: imposta un criterio IPSec VPN personalizzato per il gateway di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="e4982-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="e4982-115">Questo esempio imposta i criteri IPSec VPN personalizzati nel gateway di rete virtuale esistente denominato ContosoVirtualGateway dal gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4982-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="e4982-116">New-AzVpnClientIpsecParameter cmdlet viene usato per creare l'oggetto parametri IPSec VPN usando i valori passati di uno o tutti i parametri che l'utente può impostare per qualsiasi gateway di rete virtuale esistente in ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4982-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="e4982-117">Questo oggetto VpnClientIPsecParameters creato viene passato al comando Set-AzVpnClientIpsecParameter per impostare i criteri personalizzati IPSec VPN specificati nel gateway di rete virtuale, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="e4982-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="e4982-118">Questo comando restituisce l'oggetto di VpnClientIPsecParameters che mostra i parametri impostati.</span><span class="sxs-lookup"><span data-stu-id="e4982-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="e4982-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4982-119">PARAMETERS</span></span>

### <span data-ttu-id="e4982-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4982-120">-DefaultProfile</span></span>
<span data-ttu-id="e4982-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4982-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4982-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4982-122">-InputObject</span></span>
<span data-ttu-id="e4982-123">Oggetto gateaway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e4982-123">The virtual network gateaway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4982-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4982-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4982-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4982-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4982-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4982-126">-ResourceId</span></span>
<span data-ttu-id="e4982-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4982-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4982-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e4982-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e4982-129">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e4982-129">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4982-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="e4982-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="e4982-131">Parametri IPSec client VPN.</span><span class="sxs-lookup"><span data-stu-id="e4982-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="e4982-132">Questo valore di parametro può essere costruito usando il comando PS Let: New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e4982-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4982-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4982-133">-Confirm</span></span>
<span data-ttu-id="e4982-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4982-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4982-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4982-135">-WhatIf</span></span>
<span data-ttu-id="e4982-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4982-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4982-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4982-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4982-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4982-138">CommonParameters</span></span>
<span data-ttu-id="e4982-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4982-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4982-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4982-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4982-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4982-141">INPUTS</span></span>

### <span data-ttu-id="e4982-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="e4982-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="e4982-143">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4982-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="e4982-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e4982-144">System.String</span></span>

## <span data-ttu-id="e4982-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4982-145">OUTPUTS</span></span>

### <span data-ttu-id="e4982-146">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="e4982-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="e4982-147">Note</span><span class="sxs-lookup"><span data-stu-id="e4982-147">NOTES</span></span>

## <span data-ttu-id="e4982-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4982-148">RELATED LINKS</span></span>

[<span data-ttu-id="e4982-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e4982-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="e4982-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e4982-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="e4982-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e4982-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)