---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 218ef3115a4bc8325bc4dda37ae0a5e5820afae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512496"
---
# <span data-ttu-id="f397a-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f397a-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f397a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f397a-102">SYNOPSIS</span></span>
<span data-ttu-id="f397a-103">Configura una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f397a-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f397a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f397a-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f397a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f397a-105">DESCRIPTION</span></span>
<span data-ttu-id="f397a-106">Il cmdlet **set-AzureRmVirtualNetworkGatewayConnection** configura una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f397a-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="f397a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f397a-107">EXAMPLES</span></span>

## <span data-ttu-id="f397a-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f397a-108">PARAMETERS</span></span>

### <span data-ttu-id="f397a-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f397a-109">-AsJob</span></span>
<span data-ttu-id="f397a-110">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f397a-110">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f397a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f397a-111">-DefaultProfile</span></span>
<span data-ttu-id="f397a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f397a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f397a-113">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f397a-113">-EnableBgp</span></span>
<span data-ttu-id="f397a-114">Se usare una sessione BGP su un tunnel VPN di S2S</span><span class="sxs-lookup"><span data-stu-id="f397a-114">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f397a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f397a-115">-Force</span></span>
<span data-ttu-id="f397a-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f397a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f397a-117">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="f397a-117">-IpsecPolicies</span></span>
<span data-ttu-id="f397a-118">Elenco di criteri IPSec.</span><span class="sxs-lookup"><span data-stu-id="f397a-118">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f397a-119">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="f397a-119">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="f397a-120">Se usare i selettori del traffico basati su criteri per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="f397a-120">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f397a-121">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f397a-121">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="f397a-122">Specifica l'oggetto PSVirtualNetworkGatewayConnection usato da questo cmdlet per modificare la connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f397a-122">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f397a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f397a-123">-Confirm</span></span>
<span data-ttu-id="f397a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f397a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f397a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f397a-125">-WhatIf</span></span>
<span data-ttu-id="f397a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f397a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f397a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f397a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f397a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f397a-128">CommonParameters</span></span>
<span data-ttu-id="f397a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f397a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f397a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f397a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f397a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f397a-131">INPUTS</span></span>

### <span data-ttu-id="f397a-132">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f397a-132">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="f397a-133">Il parametro ' VirtualNetworkGatewayConnection ' accetta il valore di tipo ' PSVirtualNetworkGatewayConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f397a-133">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="f397a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f397a-134">OUTPUTS</span></span>

### <span data-ttu-id="f397a-135">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f397a-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f397a-136">Note</span><span class="sxs-lookup"><span data-stu-id="f397a-136">NOTES</span></span>

## <span data-ttu-id="f397a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f397a-137">RELATED LINKS</span></span>

[<span data-ttu-id="f397a-138">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f397a-138">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f397a-139">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f397a-139">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f397a-140">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f397a-140">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


