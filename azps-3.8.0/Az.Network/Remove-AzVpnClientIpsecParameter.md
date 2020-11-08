---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 505f9eb3b2402756b14fa8b8f49cb1a9ea2a3745
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021910"
---
# <span data-ttu-id="a55e9-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a55e9-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="a55e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a55e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a55e9-103">Rimuove i criteri IPSec personalizzati VPN impostati sulla risorsa gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a55e9-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="a55e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a55e9-104">SYNTAX</span></span>

### <span data-ttu-id="a55e9-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a55e9-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a55e9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a55e9-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a55e9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a55e9-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a55e9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a55e9-108">DESCRIPTION</span></span>
<span data-ttu-id="a55e9-109">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="a55e9-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="a55e9-110">Il cmdlet **Remove-AzVpnClientIpsecParameter** rimuove i parametri IPSec personalizzati VPN impostati nel gateway di rete virtuale, che a sua volta imposta i criteri IPSec VPN predefiniti nel gateway VPN in base al nome di VirtualNetworkGateway e al nome del gruppo di risorse passato.</span><span class="sxs-lookup"><span data-stu-id="a55e9-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="a55e9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a55e9-111">EXAMPLES</span></span>

### <span data-ttu-id="a55e9-112">1: Elimina il set di parametri IPSec VPN impostati nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a55e9-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="a55e9-113">Elimina i parametri IPSec personalizzati VPN impostati nel gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="a55e9-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="a55e9-114">Questo comando restituisce l'oggetto bool che mostra se la rimozione ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="a55e9-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="a55e9-115">Nota: questo risultato sarà l'impostazione di criteri IPSec VPN predefiniti nel gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a55e9-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="a55e9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a55e9-116">PARAMETERS</span></span>

### <span data-ttu-id="a55e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55e9-117">-DefaultProfile</span></span>
<span data-ttu-id="a55e9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a55e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a55e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a55e9-119">-InputObject</span></span>
<span data-ttu-id="a55e9-120">Oggetto gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a55e9-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="a55e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a55e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="a55e9-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a55e9-122">The resource group name.</span></span>

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

### <span data-ttu-id="a55e9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a55e9-123">-ResourceId</span></span>
<span data-ttu-id="a55e9-124">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="a55e9-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a55e9-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a55e9-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a55e9-126">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a55e9-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="a55e9-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a55e9-127">-Confirm</span></span>
<span data-ttu-id="a55e9-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a55e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a55e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a55e9-129">-WhatIf</span></span>
<span data-ttu-id="a55e9-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a55e9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a55e9-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a55e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a55e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55e9-132">CommonParameters</span></span>
<span data-ttu-id="a55e9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a55e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55e9-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a55e9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55e9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a55e9-135">INPUTS</span></span>

### <span data-ttu-id="a55e9-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a55e9-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a55e9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a55e9-137">System.String</span></span>

## <span data-ttu-id="a55e9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a55e9-138">OUTPUTS</span></span>

### <span data-ttu-id="a55e9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a55e9-139">System.Boolean</span></span>

## <span data-ttu-id="a55e9-140">Note</span><span class="sxs-lookup"><span data-stu-id="a55e9-140">NOTES</span></span>

## <span data-ttu-id="a55e9-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a55e9-141">RELATED LINKS</span></span>

[<span data-ttu-id="a55e9-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a55e9-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="a55e9-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a55e9-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="a55e9-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a55e9-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
