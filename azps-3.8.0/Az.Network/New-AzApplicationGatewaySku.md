---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022733"
---
# <span data-ttu-id="7f2e7-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7f2e7-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="7f2e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2e7-103">Crea un SKU per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f2e7-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="7f2e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f2e7-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f2e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f2e7-105">DESCRIPTION</span></span>
<span data-ttu-id="7f2e7-106">Il cmdlet **New-AzApplicationGatewaySku** crea un'unità di conservazione delle scorte (SKU) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7f2e7-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="7f2e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f2e7-107">EXAMPLES</span></span>

### <span data-ttu-id="7f2e7-108">Esempio 1: creare un SKU per un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="7f2e7-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="7f2e7-109">Questo comando crea un SKU denominato Standard_Small per un gateway di Azure Application e archivia il risultato nella variabile denominata $SKU.</span><span class="sxs-lookup"><span data-stu-id="7f2e7-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="7f2e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f2e7-110">PARAMETERS</span></span>

### <span data-ttu-id="7f2e7-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="7f2e7-111">-Capacity</span></span>
<span data-ttu-id="7f2e7-112">Specifica il numero di istanze di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f2e7-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="7f2e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2e7-113">-DefaultProfile</span></span>
<span data-ttu-id="7f2e7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f2e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f2e7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f2e7-115">-Name</span></span>
<span data-ttu-id="7f2e7-116">Specifica il nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="7f2e7-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="7f2e7-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f2e7-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f2e7-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="7f2e7-118">Standard_Small</span></span>
- <span data-ttu-id="7f2e7-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="7f2e7-119">Standard_Medium</span></span>
- <span data-ttu-id="7f2e7-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="7f2e7-120">Standard_Large</span></span>
- <span data-ttu-id="7f2e7-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="7f2e7-121">WAF_Medium</span></span>
- <span data-ttu-id="7f2e7-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="7f2e7-122">WAF_Large</span></span>
- <span data-ttu-id="7f2e7-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="7f2e7-123">Standard_v2</span></span>
- <span data-ttu-id="7f2e7-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="7f2e7-124">WAF_v2</span></span>

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

### <span data-ttu-id="7f2e7-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="7f2e7-125">-Tier</span></span>
<span data-ttu-id="7f2e7-126">Specifica il livello dell'USK.</span><span class="sxs-lookup"><span data-stu-id="7f2e7-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="7f2e7-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f2e7-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f2e7-128">Standard</span><span class="sxs-lookup"><span data-stu-id="7f2e7-128">Standard</span></span>
- <span data-ttu-id="7f2e7-129">WAF</span><span class="sxs-lookup"><span data-stu-id="7f2e7-129">WAF</span></span>
- <span data-ttu-id="7f2e7-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="7f2e7-130">Standard_v2</span></span>
- <span data-ttu-id="7f2e7-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="7f2e7-131">WAF_v2</span></span>

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

### <span data-ttu-id="7f2e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2e7-132">CommonParameters</span></span>
<span data-ttu-id="7f2e7-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f2e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2e7-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f2e7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2e7-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f2e7-135">INPUTS</span></span>

### <span data-ttu-id="7f2e7-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7f2e7-136">None</span></span>

## <span data-ttu-id="7f2e7-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f2e7-137">OUTPUTS</span></span>

### <span data-ttu-id="7f2e7-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7f2e7-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="7f2e7-139">Note</span><span class="sxs-lookup"><span data-stu-id="7f2e7-139">NOTES</span></span>

## <span data-ttu-id="7f2e7-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f2e7-140">RELATED LINKS</span></span>

[<span data-ttu-id="7f2e7-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7f2e7-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="7f2e7-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7f2e7-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


