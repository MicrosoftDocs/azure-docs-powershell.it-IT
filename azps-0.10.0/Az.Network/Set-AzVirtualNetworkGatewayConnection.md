---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b38ef9d212ceeb519e29d99391b17099177236a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862725"
---
# <span data-ttu-id="e917f-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e917f-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e917f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e917f-102">SYNOPSIS</span></span>
<span data-ttu-id="e917f-103">Configura una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e917f-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="e917f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e917f-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e917f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e917f-105">DESCRIPTION</span></span>
<span data-ttu-id="e917f-106">Il cmdlet **set-AzVirtualNetworkGatewayConnection** configura una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e917f-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="e917f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e917f-107">EXAMPLES</span></span>

### <span data-ttu-id="e917f-108">1:</span><span class="sxs-lookup"><span data-stu-id="e917f-108">1:</span></span>
```

```

## <span data-ttu-id="e917f-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e917f-109">PARAMETERS</span></span>

### <span data-ttu-id="e917f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e917f-110">-AsJob</span></span>
<span data-ttu-id="e917f-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e917f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e917f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e917f-112">-DefaultProfile</span></span>
<span data-ttu-id="e917f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e917f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e917f-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="e917f-114">-EnableBgp</span></span>
<span data-ttu-id="e917f-115">Se usare una sessione BGP su un tunnel VPN di S2S</span><span class="sxs-lookup"><span data-stu-id="e917f-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="e917f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e917f-116">-Force</span></span>
<span data-ttu-id="e917f-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e917f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e917f-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="e917f-118">-IpsecPolicies</span></span>
<span data-ttu-id="e917f-119">Elenco di criteri IPSec.</span><span class="sxs-lookup"><span data-stu-id="e917f-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="e917f-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="e917f-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="e917f-121">Se usare i selettori del traffico basati su criteri per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="e917f-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="e917f-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e917f-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="e917f-123">Specifica l'oggetto PSVirtualNetworkGatewayConnection usato da questo cmdlet per modificare la connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e917f-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="e917f-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e917f-124">-Confirm</span></span>
<span data-ttu-id="e917f-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e917f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e917f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e917f-126">-WhatIf</span></span>
<span data-ttu-id="e917f-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e917f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e917f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e917f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e917f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e917f-129">CommonParameters</span></span>
<span data-ttu-id="e917f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e917f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e917f-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e917f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e917f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e917f-132">INPUTS</span></span>

### <span data-ttu-id="e917f-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e917f-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="e917f-134">Il parametro ' VirtualNetworkGatewayConnection ' accetta il valore di tipo ' PSVirtualNetworkGatewayConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e917f-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="e917f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e917f-135">OUTPUTS</span></span>

### <span data-ttu-id="e917f-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e917f-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e917f-137">Note</span><span class="sxs-lookup"><span data-stu-id="e917f-137">NOTES</span></span>

## <span data-ttu-id="e917f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e917f-138">RELATED LINKS</span></span>

[<span data-ttu-id="e917f-139">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e917f-139">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e917f-140">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e917f-140">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e917f-141">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e917f-141">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


