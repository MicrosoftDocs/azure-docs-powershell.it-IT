---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 9315b279fd7ac6842a65c78898f1d5da23a8e1c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678026"
---
# <span data-ttu-id="4e067-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e067-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4e067-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e067-102">SYNOPSIS</span></span>
<span data-ttu-id="4e067-103">Aggiorna un pool di indirizzi back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e067-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="4e067-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e067-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e067-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e067-105">DESCRIPTION</span></span>
<span data-ttu-id="4e067-106">Il cmdlet **set-AzApplicationGatewayBackendAddressPool** aggiorna un pool di indirizzi back-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="4e067-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="4e067-107">Gli indirizzi di back-end possono essere specificati come indirizzi IP, nomi di dominio completi (FQDN) o ID configurazioni IP.</span><span class="sxs-lookup"><span data-stu-id="4e067-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="4e067-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e067-108">EXAMPLES</span></span>

### <span data-ttu-id="4e067-109">Esempio 1: impostazione di un pool di indirizzi back-end tramite FQDN</span><span class="sxs-lookup"><span data-stu-id="4e067-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="4e067-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4e067-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4e067-111">Il secondo comando Aggiorna il pool di indirizzi back-end del gateway dell'applicazione in $AppGw usando FQDN.</span><span class="sxs-lookup"><span data-stu-id="4e067-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="4e067-112">Esempio 2: impostazione di un pool di indirizzi back-end tramite indirizzi IP del server di backend</span><span class="sxs-lookup"><span data-stu-id="4e067-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="4e067-113">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4e067-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4e067-114">Il secondo comando Aggiorna il pool di indirizzi back-end del gateway dell'applicazione in $AppGw usando gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="4e067-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="4e067-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e067-115">PARAMETERS</span></span>

### <span data-ttu-id="4e067-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e067-116">-ApplicationGateway</span></span>
<span data-ttu-id="4e067-117">Specifica il gateway dell'applicazione con cui questo cmdlet associa il pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="4e067-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="4e067-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="4e067-118">-BackendFqdns</span></span>
<span data-ttu-id="4e067-119">Specifica un elenco di indirizzi IP di back-end da usare come pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="4e067-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="4e067-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="4e067-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="4e067-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e067-121">-DefaultProfile</span></span>
<span data-ttu-id="4e067-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e067-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e067-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e067-123">-Name</span></span>
<span data-ttu-id="4e067-124">Specifica il nome del pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="4e067-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="4e067-125">Questo pool di indirizzi back-end deve esistere nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e067-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="4e067-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e067-126">-Confirm</span></span>
<span data-ttu-id="4e067-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e067-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e067-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e067-128">-WhatIf</span></span>
<span data-ttu-id="4e067-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e067-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e067-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e067-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e067-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e067-131">CommonParameters</span></span>
<span data-ttu-id="4e067-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e067-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e067-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e067-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e067-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e067-134">INPUTS</span></span>

### <span data-ttu-id="4e067-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e067-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e067-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e067-136">OUTPUTS</span></span>

### <span data-ttu-id="4e067-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e067-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e067-138">Note</span><span class="sxs-lookup"><span data-stu-id="4e067-138">NOTES</span></span>

## <span data-ttu-id="4e067-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e067-139">RELATED LINKS</span></span>

[<span data-ttu-id="4e067-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e067-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4e067-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e067-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4e067-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e067-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4e067-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e067-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

