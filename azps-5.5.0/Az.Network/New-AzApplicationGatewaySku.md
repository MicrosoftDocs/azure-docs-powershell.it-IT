---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206803"
---
# <span data-ttu-id="c3df9-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c3df9-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="c3df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3df9-102">SYNOPSIS</span></span>
<span data-ttu-id="c3df9-103">Crea uno SKU per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3df9-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="c3df9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3df9-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3df9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3df9-105">DESCRIPTION</span></span>
<span data-ttu-id="c3df9-106">Il cmdlet **New-AzApplicationGatewaySku crea** un'unità di conservazione titoli azionari per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3df9-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="c3df9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3df9-107">EXAMPLES</span></span>

### <span data-ttu-id="c3df9-108">Esempio 1: Creare uno SKU per un gateway applicazione di Azure</span><span class="sxs-lookup"><span data-stu-id="c3df9-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="c3df9-109">Questo comando crea uno SKU denominato Standard_Small per un gateway applicazione di Azure e archivia il risultato nella variabile $SKU.</span><span class="sxs-lookup"><span data-stu-id="c3df9-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="c3df9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3df9-110">PARAMETERS</span></span>

### <span data-ttu-id="c3df9-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="c3df9-111">-Capacity</span></span>
<span data-ttu-id="c3df9-112">Specifica il numero di istanze di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c3df9-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="c3df9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3df9-113">-DefaultProfile</span></span>
<span data-ttu-id="c3df9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3df9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3df9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c3df9-115">-Name</span></span>
<span data-ttu-id="c3df9-116">Specifica il nome dello SKU.</span><span class="sxs-lookup"><span data-stu-id="c3df9-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="c3df9-117">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="c3df9-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3df9-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="c3df9-118">Standard_Small</span></span>
- <span data-ttu-id="c3df9-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="c3df9-119">Standard_Medium</span></span>
- <span data-ttu-id="c3df9-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="c3df9-120">Standard_Large</span></span>
- <span data-ttu-id="c3df9-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="c3df9-121">WAF_Medium</span></span>
- <span data-ttu-id="c3df9-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="c3df9-122">WAF_Large</span></span>
- <span data-ttu-id="c3df9-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="c3df9-123">Standard_v2</span></span>
- <span data-ttu-id="c3df9-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c3df9-124">WAF_v2</span></span>

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

### <span data-ttu-id="c3df9-125">-Livello</span><span class="sxs-lookup"><span data-stu-id="c3df9-125">-Tier</span></span>
<span data-ttu-id="c3df9-126">Specifica il livello dello SKU.</span><span class="sxs-lookup"><span data-stu-id="c3df9-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="c3df9-127">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="c3df9-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3df9-128">Standard</span><span class="sxs-lookup"><span data-stu-id="c3df9-128">Standard</span></span>
- <span data-ttu-id="c3df9-129">WAF</span><span class="sxs-lookup"><span data-stu-id="c3df9-129">WAF</span></span>
- <span data-ttu-id="c3df9-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="c3df9-130">Standard_v2</span></span>
- <span data-ttu-id="c3df9-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c3df9-131">WAF_v2</span></span>

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

### <span data-ttu-id="c3df9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3df9-132">CommonParameters</span></span>
<span data-ttu-id="c3df9-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3df9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3df9-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3df9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3df9-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3df9-135">INPUTS</span></span>

### <span data-ttu-id="c3df9-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3df9-136">None</span></span>

## <span data-ttu-id="c3df9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3df9-137">OUTPUTS</span></span>

### <span data-ttu-id="c3df9-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c3df9-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="c3df9-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3df9-139">NOTES</span></span>

## <span data-ttu-id="c3df9-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3df9-140">RELATED LINKS</span></span>

[<span data-ttu-id="c3df9-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c3df9-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="c3df9-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c3df9-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


