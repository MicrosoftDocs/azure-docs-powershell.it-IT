---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2f6af6dbbe8a7241cb25e1715859a68bec24598c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512495"
---
# <span data-ttu-id="a20d3-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a20d3-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="a20d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a20d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a20d3-103">Configura la chiave condivisa della connessione Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="a20d3-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a20d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a20d3-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a20d3-105">DESCRIPTION</span></span>
<span data-ttu-id="a20d3-106">Il cmdlet **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** configura la chiave condivisa della connessione Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="a20d3-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="a20d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a20d3-107">EXAMPLES</span></span>

## <span data-ttu-id="a20d3-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a20d3-108">PARAMETERS</span></span>

### <span data-ttu-id="a20d3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20d3-109">-DefaultProfile</span></span>
<span data-ttu-id="a20d3-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a20d3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a20d3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a20d3-111">-Force</span></span>
<span data-ttu-id="a20d3-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a20d3-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a20d3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a20d3-113">-Name</span></span>
<span data-ttu-id="a20d3-114">Specifica il nome della chiave condivisa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a20d3-114">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="a20d3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20d3-115">-ResourceGroupName</span></span>
<span data-ttu-id="a20d3-116">Specifica il nome del gruppo di risorse a cui appartiene il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a20d3-116">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="a20d3-117">-Valore</span><span class="sxs-lookup"><span data-stu-id="a20d3-117">-Value</span></span>
<span data-ttu-id="a20d3-118">Specifica il valore della chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="a20d3-118">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="a20d3-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a20d3-119">-Confirm</span></span>
<span data-ttu-id="a20d3-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a20d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20d3-121">-WhatIf</span></span>
<span data-ttu-id="a20d3-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a20d3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a20d3-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a20d3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20d3-124">CommonParameters</span></span>
<span data-ttu-id="a20d3-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20d3-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a20d3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20d3-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a20d3-127">INPUTS</span></span>

### <span data-ttu-id="a20d3-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a20d3-128">None</span></span>
<span data-ttu-id="a20d3-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a20d3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a20d3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a20d3-130">OUTPUTS</span></span>

### <span data-ttu-id="a20d3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a20d3-131">System.String</span></span>

## <span data-ttu-id="a20d3-132">Note</span><span class="sxs-lookup"><span data-stu-id="a20d3-132">NOTES</span></span>

## <span data-ttu-id="a20d3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a20d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="a20d3-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a20d3-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="a20d3-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a20d3-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


