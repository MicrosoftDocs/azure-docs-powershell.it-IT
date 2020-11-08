---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192341"
---
# <span data-ttu-id="a9357-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a9357-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="a9357-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9357-102">SYNOPSIS</span></span>
<span data-ttu-id="a9357-103">Crea un SKU per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a9357-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="a9357-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9357-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9357-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9357-105">DESCRIPTION</span></span>
<span data-ttu-id="a9357-106">Il cmdlet **New-AzApplicationGatewaySku** crea un'unità di conservazione delle scorte (SKU) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="a9357-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="a9357-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9357-107">EXAMPLES</span></span>

### <span data-ttu-id="a9357-108">Esempio 1: creare un SKU per un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="a9357-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="a9357-109">Questo comando crea un SKU denominato Standard_Small per un gateway di Azure Application e archivia il risultato nella variabile denominata $SKU.</span><span class="sxs-lookup"><span data-stu-id="a9357-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="a9357-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9357-110">PARAMETERS</span></span>

### <span data-ttu-id="a9357-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="a9357-111">-Capacity</span></span>
<span data-ttu-id="a9357-112">Specifica il numero di istanze di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a9357-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="a9357-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9357-113">-DefaultProfile</span></span>
<span data-ttu-id="a9357-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9357-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9357-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9357-115">-Name</span></span>
<span data-ttu-id="a9357-116">Specifica il nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="a9357-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="a9357-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9357-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9357-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="a9357-118">Standard_Small</span></span>
- <span data-ttu-id="a9357-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="a9357-119">Standard_Medium</span></span>
- <span data-ttu-id="a9357-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="a9357-120">Standard_Large</span></span>
- <span data-ttu-id="a9357-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="a9357-121">WAF_Medium</span></span>
- <span data-ttu-id="a9357-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="a9357-122">WAF_Large</span></span>
- <span data-ttu-id="a9357-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="a9357-123">Standard_v2</span></span>
- <span data-ttu-id="a9357-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="a9357-124">WAF_v2</span></span>

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

### <span data-ttu-id="a9357-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="a9357-125">-Tier</span></span>
<span data-ttu-id="a9357-126">Specifica il livello dell'USK.</span><span class="sxs-lookup"><span data-stu-id="a9357-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="a9357-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9357-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9357-128">Standard</span><span class="sxs-lookup"><span data-stu-id="a9357-128">Standard</span></span>
- <span data-ttu-id="a9357-129">WAF</span><span class="sxs-lookup"><span data-stu-id="a9357-129">WAF</span></span>
- <span data-ttu-id="a9357-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="a9357-130">Standard_v2</span></span>
- <span data-ttu-id="a9357-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="a9357-131">WAF_v2</span></span>

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

### <span data-ttu-id="a9357-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9357-132">CommonParameters</span></span>
<span data-ttu-id="a9357-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9357-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9357-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9357-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9357-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9357-135">INPUTS</span></span>

### <span data-ttu-id="a9357-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a9357-136">None</span></span>

## <span data-ttu-id="a9357-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9357-137">OUTPUTS</span></span>

### <span data-ttu-id="a9357-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a9357-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="a9357-139">Note</span><span class="sxs-lookup"><span data-stu-id="a9357-139">NOTES</span></span>

## <span data-ttu-id="a9357-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9357-140">RELATED LINKS</span></span>

[<span data-ttu-id="a9357-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a9357-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="a9357-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a9357-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


