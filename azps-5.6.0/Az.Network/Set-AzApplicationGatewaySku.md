---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: d8b7e4280ae9c73486fd5a62fe866c2241cb16a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003453"
---
# <span data-ttu-id="7ded2-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7ded2-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="7ded2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ded2-102">SYNOPSIS</span></span>
<span data-ttu-id="7ded2-103">Modifica lo SKU di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7ded2-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="7ded2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ded2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ded2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7ded2-105">DESCRIPTION</span></span>
<span data-ttu-id="7ded2-106">Il cmdlet **Set-AzApplicationGatewaySku** modifica l'unità di conservazione dei titoli azionari (SKU) di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ded2-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="7ded2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ded2-107">EXAMPLES</span></span>

### <span data-ttu-id="7ded2-108">Esempio 1: Aggiornare lo SKU del gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="7ded2-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="7ded2-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="7ded2-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7ded2-110">Il secondo comando aggiorna lo SKU del gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7ded2-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="7ded2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ded2-111">PARAMETERS</span></span>

### <span data-ttu-id="7ded2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ded2-112">-ApplicationGateway</span></span>
<span data-ttu-id="7ded2-113">Specifica l'oggetto gateway applicazione a cui questo cmdlet associa la SKU.</span><span class="sxs-lookup"><span data-stu-id="7ded2-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="7ded2-114">-Capacità</span><span class="sxs-lookup"><span data-stu-id="7ded2-114">-Capacity</span></span>
<span data-ttu-id="7ded2-115">Specifica il numero di istanze del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ded2-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="7ded2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ded2-116">-DefaultProfile</span></span>
<span data-ttu-id="7ded2-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ded2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ded2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7ded2-118">-Name</span></span>
<span data-ttu-id="7ded2-119">Specifica il nome del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ded2-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="7ded2-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7ded2-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ded2-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="7ded2-121">Standard_Small</span></span>
- <span data-ttu-id="7ded2-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="7ded2-122">Standard_Medium</span></span>
- <span data-ttu-id="7ded2-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="7ded2-123">Standard_Large</span></span>
- <span data-ttu-id="7ded2-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="7ded2-124">WAF_Medium</span></span>
- <span data-ttu-id="7ded2-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="7ded2-125">WAF_Large</span></span>

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

### <span data-ttu-id="7ded2-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="7ded2-126">-Tier</span></span>
<span data-ttu-id="7ded2-127">Specifica il livello del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ded2-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="7ded2-128">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7ded2-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ded2-129">Standard</span><span class="sxs-lookup"><span data-stu-id="7ded2-129">Standard</span></span>
- <span data-ttu-id="7ded2-130">WAF</span><span class="sxs-lookup"><span data-stu-id="7ded2-130">WAF</span></span>

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

### <span data-ttu-id="7ded2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ded2-131">CommonParameters</span></span>
<span data-ttu-id="7ded2-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ded2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ded2-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ded2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ded2-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="7ded2-134">INPUTS</span></span>

### <span data-ttu-id="7ded2-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ded2-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ded2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ded2-136">OUTPUTS</span></span>

### <span data-ttu-id="7ded2-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ded2-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ded2-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="7ded2-138">NOTES</span></span>

## <span data-ttu-id="7ded2-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ded2-139">RELATED LINKS</span></span>

[<span data-ttu-id="7ded2-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7ded2-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="7ded2-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7ded2-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


