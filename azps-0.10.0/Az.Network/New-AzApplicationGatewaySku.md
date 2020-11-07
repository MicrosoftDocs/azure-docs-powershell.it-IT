---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 0b87119ccec521b85a210dc8685874bd4ba4b9ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860550"
---
# <span data-ttu-id="72459-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="72459-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="72459-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72459-102">SYNOPSIS</span></span>
<span data-ttu-id="72459-103">Crea un SKU per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="72459-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="72459-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72459-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72459-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72459-105">DESCRIPTION</span></span>
<span data-ttu-id="72459-106">Il cmdlet **New-AzApplicationGatewaySku** crea un'unità di conservazione delle scorte (SKU) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="72459-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="72459-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72459-107">EXAMPLES</span></span>

### <span data-ttu-id="72459-108">Esempio 1: creare un SKU per un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="72459-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="72459-109">Questo comando crea un SKU denominato Standard_Small per un gateway di Azure Application e archivia il risultato nella variabile denominata $SKU.</span><span class="sxs-lookup"><span data-stu-id="72459-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="72459-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72459-110">PARAMETERS</span></span>

### <span data-ttu-id="72459-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="72459-111">-Capacity</span></span>
<span data-ttu-id="72459-112">Specifica il numero di istanze di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="72459-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72459-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72459-113">-DefaultProfile</span></span>
<span data-ttu-id="72459-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72459-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72459-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="72459-115">-Name</span></span>
<span data-ttu-id="72459-116">Specifica il nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="72459-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="72459-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="72459-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72459-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="72459-118">Standard_Small</span></span>
- <span data-ttu-id="72459-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="72459-119">Standard_Medium</span></span>
- <span data-ttu-id="72459-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="72459-120">Standard_Large</span></span>
- <span data-ttu-id="72459-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="72459-121">WAF_Medium</span></span>
- <span data-ttu-id="72459-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="72459-122">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72459-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="72459-123">-Tier</span></span>
<span data-ttu-id="72459-124">Specifica il livello dell'USK.</span><span class="sxs-lookup"><span data-stu-id="72459-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="72459-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="72459-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72459-126">Standard</span><span class="sxs-lookup"><span data-stu-id="72459-126">Standard</span></span>
- <span data-ttu-id="72459-127">WAF</span><span class="sxs-lookup"><span data-stu-id="72459-127">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72459-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72459-128">CommonParameters</span></span>
<span data-ttu-id="72459-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72459-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72459-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72459-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72459-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72459-131">INPUTS</span></span>

### <span data-ttu-id="72459-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72459-132">System.String</span></span>

## <span data-ttu-id="72459-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72459-133">OUTPUTS</span></span>

### <span data-ttu-id="72459-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="72459-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="72459-135">Note</span><span class="sxs-lookup"><span data-stu-id="72459-135">NOTES</span></span>

## <span data-ttu-id="72459-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72459-136">RELATED LINKS</span></span>

[<span data-ttu-id="72459-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="72459-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="72459-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="72459-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


