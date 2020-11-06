---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513604"
---
# <span data-ttu-id="c4b98-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c4b98-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="c4b98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4b98-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b98-103">Rimuove i criteri IPSec personalizzati VPN impostati sulla risorsa gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4b98-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4b98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4b98-104">SYNTAX</span></span>

### <span data-ttu-id="c4b98-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4b98-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4b98-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c4b98-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4b98-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4b98-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4b98-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4b98-108">DESCRIPTION</span></span>
<span data-ttu-id="c4b98-109">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b98-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="c4b98-110">Il cmdlet **Remove-AzureRmVpnClientIpsecParameter** rimuove i parametri IPSec personalizzati VPN impostati nel gateway di rete virtuale, che a sua volta imposta i criteri IPSec VPN predefiniti nel gateway VPN in base al nome di VirtualNetworkGateway e al nome del gruppo di risorse passato.</span><span class="sxs-lookup"><span data-stu-id="c4b98-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="c4b98-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4b98-111">EXAMPLES</span></span>

### <span data-ttu-id="c4b98-112">1: Elimina il set di parametri IPSec VPN impostati nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c4b98-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="c4b98-113">Elimina i parametri IPSec personalizzati VPN impostati nel gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="c4b98-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="c4b98-114">Questo comando restituisce l'oggetto bool che mostra se la rimozione ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="c4b98-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="c4b98-115">Nota: questo risultato sarà l'impostazione di criteri IPSec VPN predefiniti nel gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4b98-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="c4b98-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4b98-116">PARAMETERS</span></span>

### <span data-ttu-id="c4b98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b98-117">-DefaultProfile</span></span>
<span data-ttu-id="c4b98-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4b98-119">-InputObject</span></span>
<span data-ttu-id="c4b98-120">Oggetto gateaway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c4b98-120">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="c4b98-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b98-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4b98-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c4b98-122">The resource group name.</span></span>

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

### <span data-ttu-id="c4b98-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4b98-123">-ResourceId</span></span>
<span data-ttu-id="c4b98-124">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b98-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c4b98-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c4b98-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c4b98-126">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4b98-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="c4b98-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4b98-127">-Confirm</span></span>
<span data-ttu-id="c4b98-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b98-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b98-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b98-129">-WhatIf</span></span>
<span data-ttu-id="c4b98-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4b98-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4b98-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4b98-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b98-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b98-132">CommonParameters</span></span>
<span data-ttu-id="c4b98-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b98-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b98-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b98-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b98-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4b98-135">INPUTS</span></span>

### <span data-ttu-id="c4b98-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4b98-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="c4b98-137">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4b98-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c4b98-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b98-138">System.String</span></span>

## <span data-ttu-id="c4b98-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4b98-139">OUTPUTS</span></span>

### <span data-ttu-id="c4b98-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4b98-140">System.Boolean</span></span>

## <span data-ttu-id="c4b98-141">Note</span><span class="sxs-lookup"><span data-stu-id="c4b98-141">NOTES</span></span>

## <span data-ttu-id="c4b98-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4b98-142">RELATED LINKS</span></span>
