---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: be59f9ec0728b60314f137dcc5a57c7883935e52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866649"
---
# <span data-ttu-id="6a660-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6a660-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="6a660-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a660-102">SYNOPSIS</span></span>
<span data-ttu-id="6a660-103">Configura la chiave condivisa della connessione Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="6a660-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a660-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a660-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a660-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a660-105">DESCRIPTION</span></span>
<span data-ttu-id="6a660-106">Il cmdlet **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** configura la chiave condivisa della connessione Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="6a660-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="6a660-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a660-107">EXAMPLES</span></span>

### <span data-ttu-id="6a660-108">1:</span><span class="sxs-lookup"><span data-stu-id="6a660-108">1:</span></span>
```

```

## <span data-ttu-id="6a660-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a660-109">PARAMETERS</span></span>

### <span data-ttu-id="6a660-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a660-110">-DefaultProfile</span></span>
<span data-ttu-id="6a660-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a660-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a660-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6a660-112">-Force</span></span>
<span data-ttu-id="6a660-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6a660-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a660-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a660-114">-Name</span></span>
<span data-ttu-id="6a660-115">Specifica il nome della chiave condivisa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6a660-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a660-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a660-116">-ResourceGroupName</span></span>
<span data-ttu-id="6a660-117">Specifica il nome del gruppo di risorse a cui appartiene il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="6a660-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a660-118">-Valore</span><span class="sxs-lookup"><span data-stu-id="6a660-118">-Value</span></span>
<span data-ttu-id="6a660-119">Specifica il valore della chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="6a660-119">Specifies the value of the shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a660-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a660-120">-Confirm</span></span>
<span data-ttu-id="6a660-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a660-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a660-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a660-122">-WhatIf</span></span>
<span data-ttu-id="6a660-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a660-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a660-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a660-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a660-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a660-125">CommonParameters</span></span>
<span data-ttu-id="6a660-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a660-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a660-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a660-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a660-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a660-128">INPUTS</span></span>

## <span data-ttu-id="6a660-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a660-129">OUTPUTS</span></span>

### <span data-ttu-id="6a660-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6a660-130">System.String</span></span>

## <span data-ttu-id="6a660-131">Note</span><span class="sxs-lookup"><span data-stu-id="6a660-131">NOTES</span></span>

## <span data-ttu-id="6a660-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a660-132">RELATED LINKS</span></span>

[<span data-ttu-id="6a660-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6a660-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="6a660-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6a660-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


