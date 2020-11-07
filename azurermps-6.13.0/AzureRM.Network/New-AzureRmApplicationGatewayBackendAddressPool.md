---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1d6c207fe009133db03136ca09840fb0a8646750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517480"
---
# <span data-ttu-id="f12e9-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f12e9-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f12e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f12e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f12e9-103">Crea un pool di indirizzi back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f12e9-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f12e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f12e9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f12e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f12e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f12e9-106">Il cmdlet **New-AzureRmApplicationGatewayBackendAddressPool** crea un pool di indirizzi back-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="f12e9-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="f12e9-107">Un indirizzo di back-end può essere specificato come indirizzo IP, un nome di dominio completo (FQDN) o un ID di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f12e9-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="f12e9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f12e9-108">EXAMPLES</span></span>

### <span data-ttu-id="f12e9-109">Esempio 1: creare un pool di indirizzi back-end utilizzando il nome di dominio completo di un server back-end</span><span class="sxs-lookup"><span data-stu-id="f12e9-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="f12e9-110">Questo comando crea un pool di indirizzi back-end denominato Pool01 usando i nomi FQDN dei server back-end e lo archivia nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="f12e9-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="f12e9-111">Esempio 2: creare un pool di indirizzi back-end usando l'indirizzo IP di un server back-end</span><span class="sxs-lookup"><span data-stu-id="f12e9-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="f12e9-112">Questo comando crea un pool di indirizzi back-end denominato Pool02 usando gli indirizzi IP dei server back-end e lo archivia nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="f12e9-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="f12e9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f12e9-113">PARAMETERS</span></span>

### <span data-ttu-id="f12e9-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="f12e9-114">-BackendFqdns</span></span>
<span data-ttu-id="f12e9-115">Specifica un elenco di FQDN di back-end che questo cmdlet associa al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f12e9-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f12e9-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f12e9-116">-BackendIPAddresses</span></span>
<span data-ttu-id="f12e9-117">Specifica un elenco di indirizzi IP di back-end che questo cmdlet associa al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f12e9-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f12e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f12e9-118">-DefaultProfile</span></span>
<span data-ttu-id="f12e9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f12e9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f12e9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f12e9-120">-Name</span></span>
<span data-ttu-id="f12e9-121">Specifica il nome del pool di server back-end creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12e9-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f12e9-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f12e9-122">-Confirm</span></span>
<span data-ttu-id="f12e9-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f12e9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f12e9-124">-WhatIf</span></span>
<span data-ttu-id="f12e9-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f12e9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f12e9-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f12e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f12e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12e9-127">CommonParameters</span></span>
<span data-ttu-id="f12e9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f12e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12e9-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f12e9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12e9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f12e9-130">INPUTS</span></span>

### <span data-ttu-id="f12e9-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f12e9-131">None</span></span>

## <span data-ttu-id="f12e9-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f12e9-132">OUTPUTS</span></span>

### <span data-ttu-id="f12e9-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f12e9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f12e9-134">Note</span><span class="sxs-lookup"><span data-stu-id="f12e9-134">NOTES</span></span>

## <span data-ttu-id="f12e9-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f12e9-135">RELATED LINKS</span></span>

[<span data-ttu-id="f12e9-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f12e9-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f12e9-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f12e9-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f12e9-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f12e9-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f12e9-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f12e9-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)

