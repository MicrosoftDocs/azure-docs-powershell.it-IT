---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 9c5da09a801e78ad93ad609dc91f0c254309aa6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968014"
---
# <span data-ttu-id="0214a-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0214a-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="0214a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0214a-102">SYNOPSIS</span></span>
<span data-ttu-id="0214a-103">Aggiunge un pool di indirizzi back-end a un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0214a-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="0214a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0214a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0214a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0214a-105">DESCRIPTION</span></span>
<span data-ttu-id="0214a-106">Il cmdlet **Add-AzApplicationGatewayBackendAddressPool aggiunge** un pool di indirizzi back-end a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="0214a-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="0214a-107">È possibile specificare un indirizzo back-end usando un indirizzo IP, un nome di dominio completo (FQDN) o ID di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="0214a-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="0214a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0214a-108">EXAMPLES</span></span>

### <span data-ttu-id="0214a-109">Esempio 1: Aggiungere un pool di indirizzi back-end usando l'FQDN di un server back-end</span><span class="sxs-lookup"><span data-stu-id="0214a-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="0214a-110">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile. Il secondo comando aggiunge il pool di indirizzi back-end del gateway applicazione archiviato in $AppGw tramite FQDN.</span><span class="sxs-lookup"><span data-stu-id="0214a-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="0214a-111">Esempio 2: Aggiungere un pool di indirizzi back-end usando gli indirizzi IP del server back-end</span><span class="sxs-lookup"><span data-stu-id="0214a-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="0214a-112">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile. Il secondo comando aggiunge il pool di indirizzi back-end del gateway applicazione archiviato in $AppGw tramite indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="0214a-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="0214a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0214a-113">PARAMETERS</span></span>

### <span data-ttu-id="0214a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0214a-114">-ApplicationGateway</span></span>
<span data-ttu-id="0214a-115">Specifica il gateway applicazione a cui questo cmdlet aggiunge un pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="0214a-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0214a-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="0214a-116">-BackendFqdns</span></span>
<span data-ttu-id="0214a-117">Specifica un elenco di FQDN back-end che questo cmdlet aggiunge come pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="0214a-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="0214a-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="0214a-118">-BackendIPAddresses</span></span>
<span data-ttu-id="0214a-119">Specifica un elenco di indirizzi IP back-end che questo cmdlet aggiunge come pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="0214a-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="0214a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0214a-120">-DefaultProfile</span></span>
<span data-ttu-id="0214a-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0214a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0214a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0214a-122">-Name</span></span>
<span data-ttu-id="0214a-123">Specifica il nome del pool di server back-end aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0214a-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0214a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0214a-124">-Confirm</span></span>
<span data-ttu-id="0214a-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0214a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0214a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0214a-126">-WhatIf</span></span>
<span data-ttu-id="0214a-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0214a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0214a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0214a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0214a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0214a-129">CommonParameters</span></span>
<span data-ttu-id="0214a-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0214a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0214a-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0214a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0214a-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="0214a-132">INPUTS</span></span>

### <span data-ttu-id="0214a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0214a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0214a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0214a-134">OUTPUTS</span></span>

### <span data-ttu-id="0214a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0214a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0214a-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="0214a-136">NOTES</span></span>

## <span data-ttu-id="0214a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0214a-137">RELATED LINKS</span></span>

[<span data-ttu-id="0214a-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0214a-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0214a-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0214a-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0214a-140">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0214a-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0214a-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0214a-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0214a-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0214a-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0214a-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0214a-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
