---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: b1680d18e11851718ca6d9d49acf4dc9501e1aad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516195"
---
# <span data-ttu-id="f87ee-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f87ee-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="f87ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f87ee-102">SYNOPSIS</span></span>
<span data-ttu-id="f87ee-103">Modifica l'USK di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f87ee-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f87ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f87ee-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f87ee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f87ee-105">DESCRIPTION</span></span>
<span data-ttu-id="f87ee-106">Il cmdlet **set-AzureRmApplicationGatewaySku** modifica l'unità di conservazione delle scorte (SKU) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f87ee-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="f87ee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f87ee-107">EXAMPLES</span></span>

### <span data-ttu-id="f87ee-108">Esempio 1: aggiornare la SKU gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f87ee-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="f87ee-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f87ee-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f87ee-110">Il secondo comando Aggiorna l'USK del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f87ee-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="f87ee-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f87ee-111">PARAMETERS</span></span>

### <span data-ttu-id="f87ee-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f87ee-112">-ApplicationGateway</span></span>
<span data-ttu-id="f87ee-113">Specifica l'oggetto gateway dell'applicazione con cui questo cmdlet associa l'USK.</span><span class="sxs-lookup"><span data-stu-id="f87ee-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="f87ee-114">-Capacità</span><span class="sxs-lookup"><span data-stu-id="f87ee-114">-Capacity</span></span>
<span data-ttu-id="f87ee-115">Specifica il conteggio delle istanze del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f87ee-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87ee-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f87ee-116">-Name</span></span>
<span data-ttu-id="f87ee-117">Specifica il nome del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f87ee-117">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="f87ee-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f87ee-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f87ee-119">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="f87ee-119">Standard_Small</span></span>
- <span data-ttu-id="f87ee-120">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="f87ee-120">Standard_Medium</span></span>
- <span data-ttu-id="f87ee-121">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="f87ee-121">Standard_Large</span></span>
- <span data-ttu-id="f87ee-122">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="f87ee-122">WAF_Medium</span></span>
- <span data-ttu-id="f87ee-123">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="f87ee-123">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87ee-124">-Tier</span><span class="sxs-lookup"><span data-stu-id="f87ee-124">-Tier</span></span>
<span data-ttu-id="f87ee-125">Specifica il livello del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f87ee-125">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="f87ee-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f87ee-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f87ee-127">Standard</span><span class="sxs-lookup"><span data-stu-id="f87ee-127">Standard</span></span>
- <span data-ttu-id="f87ee-128">WAF</span><span class="sxs-lookup"><span data-stu-id="f87ee-128">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87ee-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87ee-129">-DefaultProfile</span></span>
<span data-ttu-id="f87ee-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f87ee-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f87ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87ee-131">CommonParameters</span></span>
<span data-ttu-id="f87ee-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87ee-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f87ee-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87ee-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f87ee-134">INPUTS</span></span>

### <span data-ttu-id="f87ee-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f87ee-135">System.String</span></span>

## <span data-ttu-id="f87ee-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f87ee-136">OUTPUTS</span></span>

### <span data-ttu-id="f87ee-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f87ee-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f87ee-138">Note</span><span class="sxs-lookup"><span data-stu-id="f87ee-138">NOTES</span></span>

## <span data-ttu-id="f87ee-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f87ee-139">RELATED LINKS</span></span>

[<span data-ttu-id="f87ee-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f87ee-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="f87ee-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f87ee-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

