---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 513fbe1d973a75dbc1c967610d95882202bab147
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960270"
---
# <span data-ttu-id="00a93-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00a93-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="00a93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00a93-102">SYNOPSIS</span></span>
<span data-ttu-id="00a93-103">Rimuove il criterio IPSec personalizzato vpn impostato sulla risorsa Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="00a93-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="00a93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00a93-104">SYNTAX</span></span>

### <span data-ttu-id="00a93-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="00a93-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00a93-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="00a93-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00a93-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00a93-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00a93-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00a93-108">DESCRIPTION</span></span>
<span data-ttu-id="00a93-109">Il Gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="00a93-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="00a93-110">Il cmdlet **Remove-AzVpnClientIpsecParameter** rimuove i parametri ipsec personalizzati vpn impostati sul Gateway di rete virtuale, che a sua volta imposta i criteri ipsec vpn predefiniti nel gateway VPN in base al nome VirtualNetworkGateway e al nome del gruppo di risorse passato.</span><span class="sxs-lookup"><span data-stu-id="00a93-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="00a93-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00a93-111">EXAMPLES</span></span>

### <span data-ttu-id="00a93-112">Esempio 1: Elimina i parametri set vpn ipsec impostati nel Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="00a93-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="00a93-113">Elimina i parametri ipsec personalizzati vpn impostati nel Gateway di rete virtuale con il nome "myGateway" all'interno del gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="00a93-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="00a93-114">Questo comando restituisce l'oggetto Bool che indica se la rimozione è riuscita o non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="00a93-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="00a93-115">Nota: il risultato sarà l'impostazione del criterio ipsec vpn predefinito nel Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="00a93-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="00a93-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00a93-116">PARAMETERS</span></span>

### <span data-ttu-id="00a93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a93-117">-DefaultProfile</span></span>
<span data-ttu-id="00a93-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00a93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00a93-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00a93-119">-InputObject</span></span>
<span data-ttu-id="00a93-120">Oggetto Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="00a93-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="00a93-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00a93-121">-ResourceGroupName</span></span>
<span data-ttu-id="00a93-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="00a93-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a93-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00a93-123">-ResourceId</span></span>
<span data-ttu-id="00a93-124">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="00a93-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="00a93-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="00a93-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="00a93-126">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="00a93-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a93-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00a93-127">-Confirm</span></span>
<span data-ttu-id="00a93-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00a93-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00a93-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00a93-129">-WhatIf</span></span>
<span data-ttu-id="00a93-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00a93-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00a93-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00a93-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00a93-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a93-132">CommonParameters</span></span>
<span data-ttu-id="00a93-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00a93-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a93-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00a93-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a93-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="00a93-135">INPUTS</span></span>

### <span data-ttu-id="00a93-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="00a93-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="00a93-137">System.String</span><span class="sxs-lookup"><span data-stu-id="00a93-137">System.String</span></span>

## <span data-ttu-id="00a93-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00a93-138">OUTPUTS</span></span>

### <span data-ttu-id="00a93-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00a93-139">System.Boolean</span></span>

## <span data-ttu-id="00a93-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="00a93-140">NOTES</span></span>

## <span data-ttu-id="00a93-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00a93-141">RELATED LINKS</span></span>

[<span data-ttu-id="00a93-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00a93-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="00a93-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00a93-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="00a93-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00a93-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
