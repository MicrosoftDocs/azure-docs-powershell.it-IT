---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513187"
---
# <span data-ttu-id="aa1df-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aa1df-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="aa1df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa1df-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1df-103">Configura una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="aa1df-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa1df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa1df-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa1df-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa1df-105">DESCRIPTION</span></span>
<span data-ttu-id="aa1df-106">Il cmdlet **set-AzureRmVirtualNetworkGatewayConnection** configura una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="aa1df-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="aa1df-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa1df-107">EXAMPLES</span></span>

## <span data-ttu-id="aa1df-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa1df-108">PARAMETERS</span></span>

### <span data-ttu-id="aa1df-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="aa1df-109">-EnableBgp</span></span>
<span data-ttu-id="aa1df-110">Se usare una sessione BGP su un tunnel VPN di S2S</span><span class="sxs-lookup"><span data-stu-id="aa1df-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1df-111">-Force</span><span class="sxs-lookup"><span data-stu-id="aa1df-111">-Force</span></span>
<span data-ttu-id="aa1df-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="aa1df-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa1df-113">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="aa1df-113">-IpsecPolicies</span></span>
<span data-ttu-id="aa1df-114">Elenco di criteri IPSec.</span><span class="sxs-lookup"><span data-stu-id="aa1df-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="aa1df-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="aa1df-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="aa1df-116">Se usare i selettori del traffico basati su criteri per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="aa1df-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa1df-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aa1df-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="aa1df-118">Specifica l'oggetto PSVirtualNetworkGatewayConnection usato da questo cmdlet per modificare la connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="aa1df-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1df-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa1df-119">-Confirm</span></span>
<span data-ttu-id="aa1df-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa1df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa1df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa1df-121">-WhatIf</span></span>
<span data-ttu-id="aa1df-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa1df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa1df-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa1df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa1df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1df-124">-DefaultProfile</span></span>
<span data-ttu-id="aa1df-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa1df-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa1df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1df-126">CommonParameters</span></span>
<span data-ttu-id="aa1df-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa1df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1df-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa1df-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1df-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa1df-129">INPUTS</span></span>

### <span data-ttu-id="aa1df-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aa1df-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="aa1df-131">Il parametro ' VirtualNetworkGatewayConnection ' accetta il valore di tipo ' PSVirtualNetworkGatewayConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="aa1df-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="aa1df-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa1df-132">OUTPUTS</span></span>

### <span data-ttu-id="aa1df-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aa1df-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="aa1df-134">Note</span><span class="sxs-lookup"><span data-stu-id="aa1df-134">NOTES</span></span>

## <span data-ttu-id="aa1df-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa1df-135">RELATED LINKS</span></span>

[<span data-ttu-id="aa1df-136">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aa1df-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="aa1df-137">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aa1df-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="aa1df-138">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aa1df-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


