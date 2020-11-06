---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520490"
---
# <span data-ttu-id="a7d32-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a7d32-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="a7d32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7d32-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d32-103">Crea un SKU per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7d32-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7d32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7d32-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d32-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7d32-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d32-106">Il cmdlet **New-AzureRmApplicationGatewaySku** crea un'unità di conservazione delle scorte (SKU) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d32-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="a7d32-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7d32-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d32-108">Esempio 1: creare un SKU per un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="a7d32-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="a7d32-109">Questo comando crea un SKU denominato Standard_Small per un gateway di Azure Application e archivia il risultato nella variabile denominata $SKU.</span><span class="sxs-lookup"><span data-stu-id="a7d32-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="a7d32-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7d32-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d32-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="a7d32-111">-Capacity</span></span>
<span data-ttu-id="a7d32-112">Specifica il numero di istanze di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7d32-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="a7d32-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7d32-113">-Name</span></span>
<span data-ttu-id="a7d32-114">Specifica il nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="a7d32-114">Specifies the name of the SKU.</span></span>

<span data-ttu-id="a7d32-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7d32-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7d32-116">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="a7d32-116">Standard_Small</span></span>
- <span data-ttu-id="a7d32-117">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="a7d32-117">Standard_Medium</span></span>
- <span data-ttu-id="a7d32-118">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="a7d32-118">Standard_Large</span></span>
- <span data-ttu-id="a7d32-119">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="a7d32-119">WAF_Medium</span></span>
- <span data-ttu-id="a7d32-120">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="a7d32-120">WAF_Large</span></span>

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

### <span data-ttu-id="a7d32-121">-Tier</span><span class="sxs-lookup"><span data-stu-id="a7d32-121">-Tier</span></span>
<span data-ttu-id="a7d32-122">Specifica il livello dell'USK.</span><span class="sxs-lookup"><span data-stu-id="a7d32-122">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="a7d32-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7d32-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7d32-124">Standard</span><span class="sxs-lookup"><span data-stu-id="a7d32-124">Standard</span></span>
- <span data-ttu-id="a7d32-125">WAF</span><span class="sxs-lookup"><span data-stu-id="a7d32-125">WAF</span></span>

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

### <span data-ttu-id="a7d32-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d32-126">-DefaultProfile</span></span>
<span data-ttu-id="a7d32-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d32-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d32-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d32-128">CommonParameters</span></span>
<span data-ttu-id="a7d32-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d32-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d32-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d32-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d32-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7d32-131">INPUTS</span></span>

### <span data-ttu-id="a7d32-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a7d32-132">System.String</span></span>

## <span data-ttu-id="a7d32-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7d32-133">OUTPUTS</span></span>

### <span data-ttu-id="a7d32-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a7d32-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="a7d32-135">Note</span><span class="sxs-lookup"><span data-stu-id="a7d32-135">NOTES</span></span>

## <span data-ttu-id="a7d32-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7d32-136">RELATED LINKS</span></span>

[<span data-ttu-id="a7d32-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a7d32-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="a7d32-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a7d32-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


