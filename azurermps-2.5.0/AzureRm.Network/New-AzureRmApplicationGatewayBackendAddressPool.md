---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: dcce5b85fc9d3e8046ecc90330da5f3d40b88e33
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866266"
---
# <span data-ttu-id="7291d-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7291d-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7291d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7291d-102">SYNOPSIS</span></span>
<span data-ttu-id="7291d-103">Crea un pool di indirizzi back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7291d-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7291d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7291d-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7291d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7291d-105">DESCRIPTION</span></span>
<span data-ttu-id="7291d-106">Il cmdlet **New-AzureRmApplicationGatewayBackendAddressPool** crea un pool di indirizzi back-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7291d-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="7291d-107">Un indirizzo di back-end può essere specificato come indirizzo IP, un nome di dominio completo (FQDN) o un ID di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="7291d-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="7291d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7291d-108">EXAMPLES</span></span>

### <span data-ttu-id="7291d-109">Esempio 1: creare un pool di indirizzi back-end utilizzando il nome di dominio completo di un server back-end</span><span class="sxs-lookup"><span data-stu-id="7291d-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="7291d-110">Questo comando crea un pool di indirizzi back-end denominato Pool01 usando i nomi FQDN dei server back-end e lo archivia nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="7291d-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="7291d-111">Esempio 2: creare un pool di indirizzi back-end usando l'indirizzo IP di un server back-end</span><span class="sxs-lookup"><span data-stu-id="7291d-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="7291d-112">Questo comando crea un pool di indirizzi back-end denominato Pool02 usando gli indirizzi IP dei server back-end e lo archivia nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="7291d-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="7291d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7291d-113">PARAMETERS</span></span>

### <span data-ttu-id="7291d-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="7291d-114">-BackendFqdns</span></span>
<span data-ttu-id="7291d-115">Specifica un elenco di FQDN di back-end che questo cmdlet associa al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="7291d-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="7291d-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="7291d-116">-BackendIPAddresses</span></span>
<span data-ttu-id="7291d-117">Specifica un elenco di indirizzi IP di back-end che questo cmdlet associa al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="7291d-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="7291d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7291d-118">-DefaultProfile</span></span>
<span data-ttu-id="7291d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7291d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7291d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7291d-120">-Name</span></span>
<span data-ttu-id="7291d-121">Specifica il nome del pool di server back-end creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7291d-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7291d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7291d-122">-Confirm</span></span>
<span data-ttu-id="7291d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7291d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7291d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7291d-124">-WhatIf</span></span>
<span data-ttu-id="7291d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7291d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7291d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7291d-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7291d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7291d-127">CommonParameters</span></span>
<span data-ttu-id="7291d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7291d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7291d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7291d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7291d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7291d-130">INPUTS</span></span>

### <span data-ttu-id="7291d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7291d-131">System.String</span></span>

## <span data-ttu-id="7291d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7291d-132">OUTPUTS</span></span>

### <span data-ttu-id="7291d-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7291d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7291d-134">Note</span><span class="sxs-lookup"><span data-stu-id="7291d-134">NOTES</span></span>

## <span data-ttu-id="7291d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7291d-135">RELATED LINKS</span></span>

[<span data-ttu-id="7291d-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7291d-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7291d-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7291d-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7291d-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7291d-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7291d-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7291d-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


