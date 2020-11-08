---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199525"
---
# <span data-ttu-id="a5634-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a5634-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="a5634-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5634-102">SYNOPSIS</span></span>
<span data-ttu-id="a5634-103">Modifica l'USK di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5634-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="a5634-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5634-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5634-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5634-105">DESCRIPTION</span></span>
<span data-ttu-id="a5634-106">Il cmdlet **set-AzApplicationGatewaySku** modifica l'unità di conservazione delle scorte (SKU) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5634-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="a5634-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5634-107">EXAMPLES</span></span>

### <span data-ttu-id="a5634-108">Esempio 1: aggiornare la SKU gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="a5634-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="a5634-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a5634-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a5634-110">Il secondo comando Aggiorna l'USK del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5634-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="a5634-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5634-111">PARAMETERS</span></span>

### <span data-ttu-id="a5634-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5634-112">-ApplicationGateway</span></span>
<span data-ttu-id="a5634-113">Specifica l'oggetto gateway dell'applicazione con cui questo cmdlet associa l'USK.</span><span class="sxs-lookup"><span data-stu-id="a5634-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="a5634-114">-Capacità</span><span class="sxs-lookup"><span data-stu-id="a5634-114">-Capacity</span></span>
<span data-ttu-id="a5634-115">Specifica il conteggio delle istanze del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5634-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5634-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5634-116">-DefaultProfile</span></span>
<span data-ttu-id="a5634-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5634-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5634-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5634-118">-Name</span></span>
<span data-ttu-id="a5634-119">Specifica il nome del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5634-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="a5634-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5634-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a5634-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="a5634-121">Standard_Small</span></span>
- <span data-ttu-id="a5634-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="a5634-122">Standard_Medium</span></span>
- <span data-ttu-id="a5634-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="a5634-123">Standard_Large</span></span>
- <span data-ttu-id="a5634-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="a5634-124">WAF_Medium</span></span>
- <span data-ttu-id="a5634-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="a5634-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5634-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="a5634-126">-Tier</span></span>
<span data-ttu-id="a5634-127">Specifica il livello del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5634-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="a5634-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5634-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a5634-129">Standard</span><span class="sxs-lookup"><span data-stu-id="a5634-129">Standard</span></span>
- <span data-ttu-id="a5634-130">WAF</span><span class="sxs-lookup"><span data-stu-id="a5634-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5634-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5634-131">CommonParameters</span></span>
<span data-ttu-id="a5634-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5634-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5634-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5634-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5634-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5634-134">INPUTS</span></span>

### <span data-ttu-id="a5634-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5634-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5634-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5634-136">OUTPUTS</span></span>

### <span data-ttu-id="a5634-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5634-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5634-138">Note</span><span class="sxs-lookup"><span data-stu-id="a5634-138">NOTES</span></span>

## <span data-ttu-id="a5634-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5634-139">RELATED LINKS</span></span>

[<span data-ttu-id="a5634-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a5634-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="a5634-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a5634-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


