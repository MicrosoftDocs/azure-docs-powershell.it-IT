---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193414"
---
# <span data-ttu-id="19c8b-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="19c8b-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="19c8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="19c8b-103">Aggiorna un pool di indirizzi back-end per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="19c8b-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="19c8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19c8b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c8b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="19c8b-105">DESCRIPTION</span></span>
<span data-ttu-id="19c8b-106">Il cmdlet **Set-AzApplicationGatewayBackendAddressPool** aggiorna un pool di indirizzi back-end per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="19c8b-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="19c8b-107">Gli indirizzi back-end possono essere specificati come indirizzi IP, nomi di dominio completi (FQDN) o ID di configurazioni IP.</span><span class="sxs-lookup"><span data-stu-id="19c8b-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="19c8b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19c8b-108">EXAMPLES</span></span>

### <span data-ttu-id="19c8b-109">Esempio 1: Impostazione di un pool di indirizzi back-end tramite FQDN</span><span class="sxs-lookup"><span data-stu-id="19c8b-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="19c8b-110">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="19c8b-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="19c8b-111">Il secondo comando aggiorna il pool di indirizzi back-end del gateway applicazione in $AppGw tramite FQDN.</span><span class="sxs-lookup"><span data-stu-id="19c8b-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="19c8b-112">Esempio 2: Impostazione di un pool di indirizzi back-end tramite indirizzi IP del server back-end</span><span class="sxs-lookup"><span data-stu-id="19c8b-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="19c8b-113">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="19c8b-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="19c8b-114">Il secondo comando aggiorna il pool di indirizzi back-end del gateway applicazione in $AppGw tramite indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="19c8b-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="19c8b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19c8b-115">PARAMETERS</span></span>

### <span data-ttu-id="19c8b-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19c8b-116">-ApplicationGateway</span></span>
<span data-ttu-id="19c8b-117">Specifica il gateway applicazione a cui questo cmdlet associa il pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="19c8b-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="19c8b-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="19c8b-118">-BackendFqdns</span></span>
<span data-ttu-id="19c8b-119">Specifica un elenco di indirizzi IP back-end da usare come pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="19c8b-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="19c8b-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="19c8b-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="19c8b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c8b-121">-DefaultProfile</span></span>
<span data-ttu-id="19c8b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19c8b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19c8b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="19c8b-123">-Name</span></span>
<span data-ttu-id="19c8b-124">Specifica il nome del pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="19c8b-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="19c8b-125">Questo pool di indirizzi back-end deve esistere nel gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="19c8b-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="19c8b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19c8b-126">-Confirm</span></span>
<span data-ttu-id="19c8b-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c8b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c8b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c8b-128">-WhatIf</span></span>
<span data-ttu-id="19c8b-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19c8b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c8b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19c8b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c8b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c8b-131">CommonParameters</span></span>
<span data-ttu-id="19c8b-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c8b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c8b-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c8b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c8b-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="19c8b-134">INPUTS</span></span>

### <span data-ttu-id="19c8b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19c8b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19c8b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19c8b-136">OUTPUTS</span></span>

### <span data-ttu-id="19c8b-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19c8b-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19c8b-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="19c8b-138">NOTES</span></span>

## <span data-ttu-id="19c8b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19c8b-139">RELATED LINKS</span></span>

[<span data-ttu-id="19c8b-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="19c8b-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="19c8b-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="19c8b-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="19c8b-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="19c8b-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="19c8b-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="19c8b-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


