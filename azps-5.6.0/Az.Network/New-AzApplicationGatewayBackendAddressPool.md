---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 3ce9cb761bb945c777a39e728ac8ebea2c40b885
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010350"
---
# <span data-ttu-id="1b342-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b342-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="1b342-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b342-102">SYNOPSIS</span></span>
<span data-ttu-id="1b342-103">Crea un pool di indirizzi back-end per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1b342-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="1b342-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b342-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b342-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b342-105">DESCRIPTION</span></span>
<span data-ttu-id="1b342-106">Il cmdlet **New-AzApplicationGatewayBackendAddressPool** crea un pool di indirizzi back-end per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b342-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="1b342-107">È possibile specificare un indirizzo back-end come indirizzo IP, nome di dominio completo (FQDN) o ID di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="1b342-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="1b342-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b342-108">EXAMPLES</span></span>

### <span data-ttu-id="1b342-109">Esempio 1: Creare un pool di indirizzi back-end usando l'FQDN di un server back-end</span><span class="sxs-lookup"><span data-stu-id="1b342-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="1b342-110">Questo comando crea un pool di indirizzi back-end denominato Pool01 usando gli FQDN dei server back-end e lo archivia nella variabile $Pool locale.</span><span class="sxs-lookup"><span data-stu-id="1b342-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="1b342-111">Esempio 2: Creare un pool di indirizzi back-end usando l'indirizzo IP di un server back-end</span><span class="sxs-lookup"><span data-stu-id="1b342-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="1b342-112">Questo comando crea un pool di indirizzi back-end denominato Pool02 usando gli indirizzi IP dei server back-end e lo archivia nella variabile $Pool back-end.</span><span class="sxs-lookup"><span data-stu-id="1b342-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="1b342-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b342-113">PARAMETERS</span></span>

### <span data-ttu-id="1b342-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="1b342-114">-BackendFqdns</span></span>
<span data-ttu-id="1b342-115">Specifica un elenco di FQDN back-end associati al cmdlet al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="1b342-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="1b342-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="1b342-116">-BackendIPAddresses</span></span>
<span data-ttu-id="1b342-117">Specifica un elenco di indirizzi IP di back-end associati al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="1b342-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="1b342-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b342-118">-DefaultProfile</span></span>
<span data-ttu-id="1b342-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b342-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b342-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1b342-120">-Name</span></span>
<span data-ttu-id="1b342-121">Specifica il nome del pool di server back-end creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b342-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1b342-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b342-122">-Confirm</span></span>
<span data-ttu-id="1b342-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b342-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b342-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b342-124">-WhatIf</span></span>
<span data-ttu-id="1b342-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b342-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b342-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b342-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b342-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b342-127">CommonParameters</span></span>
<span data-ttu-id="1b342-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b342-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b342-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b342-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b342-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b342-130">INPUTS</span></span>

### <span data-ttu-id="1b342-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b342-131">None</span></span>

## <span data-ttu-id="1b342-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b342-132">OUTPUTS</span></span>

### <span data-ttu-id="1b342-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b342-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="1b342-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b342-134">NOTES</span></span>

## <span data-ttu-id="1b342-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b342-135">RELATED LINKS</span></span>

[<span data-ttu-id="1b342-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b342-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1b342-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b342-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1b342-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b342-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1b342-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b342-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


