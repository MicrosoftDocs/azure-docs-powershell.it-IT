---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1f99fe982496fc6cef3ee9579d8e0be555880aaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006205"
---
# <span data-ttu-id="94925-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="94925-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="94925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94925-102">SYNOPSIS</span></span>
<span data-ttu-id="94925-103">Crea uno SKU per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="94925-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="94925-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94925-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94925-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94925-105">DESCRIPTION</span></span>
<span data-ttu-id="94925-106">Il cmdlet **New-AzApplicationGatewaySku crea** una SKU (Stock Keeping Unit) per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="94925-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="94925-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94925-107">EXAMPLES</span></span>

### <span data-ttu-id="94925-108">Esempio 1: Creare uno SKU per un gateway applicazione di Azure</span><span class="sxs-lookup"><span data-stu-id="94925-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="94925-109">Questo comando crea uno SKU denominato Standard_Small per un gateway applicazione di Azure e archivia il risultato nella variabile $SKU.</span><span class="sxs-lookup"><span data-stu-id="94925-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="94925-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94925-110">PARAMETERS</span></span>

### <span data-ttu-id="94925-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="94925-111">-Capacity</span></span>
<span data-ttu-id="94925-112">Specifica il numero di istanze di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="94925-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="94925-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94925-113">-DefaultProfile</span></span>
<span data-ttu-id="94925-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94925-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94925-115">-Name</span><span class="sxs-lookup"><span data-stu-id="94925-115">-Name</span></span>
<span data-ttu-id="94925-116">Specifica il nome dello SKU.</span><span class="sxs-lookup"><span data-stu-id="94925-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="94925-117">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94925-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94925-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="94925-118">Standard_Small</span></span>
- <span data-ttu-id="94925-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="94925-119">Standard_Medium</span></span>
- <span data-ttu-id="94925-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="94925-120">Standard_Large</span></span>
- <span data-ttu-id="94925-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="94925-121">WAF_Medium</span></span>
- <span data-ttu-id="94925-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="94925-122">WAF_Large</span></span>
- <span data-ttu-id="94925-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="94925-123">Standard_v2</span></span>
- <span data-ttu-id="94925-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="94925-124">WAF_v2</span></span>

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

### <span data-ttu-id="94925-125">-Livello</span><span class="sxs-lookup"><span data-stu-id="94925-125">-Tier</span></span>
<span data-ttu-id="94925-126">Specifica il livello dello SKU.</span><span class="sxs-lookup"><span data-stu-id="94925-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="94925-127">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94925-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94925-128">Standard</span><span class="sxs-lookup"><span data-stu-id="94925-128">Standard</span></span>
- <span data-ttu-id="94925-129">WAF</span><span class="sxs-lookup"><span data-stu-id="94925-129">WAF</span></span>
- <span data-ttu-id="94925-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="94925-130">Standard_v2</span></span>
- <span data-ttu-id="94925-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="94925-131">WAF_v2</span></span>

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

### <span data-ttu-id="94925-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94925-132">CommonParameters</span></span>
<span data-ttu-id="94925-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94925-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94925-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94925-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94925-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="94925-135">INPUTS</span></span>

### <span data-ttu-id="94925-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94925-136">None</span></span>

## <span data-ttu-id="94925-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94925-137">OUTPUTS</span></span>

### <span data-ttu-id="94925-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="94925-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="94925-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="94925-139">NOTES</span></span>

## <span data-ttu-id="94925-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94925-140">RELATED LINKS</span></span>

[<span data-ttu-id="94925-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="94925-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="94925-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="94925-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


