---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: b62a41c2c97055f0ef090ed5def3dc771ae3c1ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862878"
---
# <span data-ttu-id="6afd4-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afd4-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="6afd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6afd4-102">SYNOPSIS</span></span>
<span data-ttu-id="6afd4-103">Aggiorna un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6afd4-103">Updates an application gateway.</span></span>

## <span data-ttu-id="6afd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6afd4-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6afd4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6afd4-105">DESCRIPTION</span></span>
<span data-ttu-id="6afd4-106">Il cmdlet **set-AzApplicationGateway** aggiorna un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="6afd4-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="6afd4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6afd4-107">EXAMPLES</span></span>

### <span data-ttu-id="6afd4-108">Esempio 1: aggiornare un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="6afd4-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="6afd4-109">Questo comando Aggiorna il gateway dell'applicazione con le impostazioni nella variabile $AppGw e archivia il gateway aggiornato nella variabile $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="6afd4-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="6afd4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6afd4-110">PARAMETERS</span></span>

### <span data-ttu-id="6afd4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afd4-111">-ApplicationGateway</span></span>
<span data-ttu-id="6afd4-112">Specifica un oggetto gateway dell'applicazione che rappresenta lo stato in cui deve essere impostato il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6afd4-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6afd4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6afd4-113">-AsJob</span></span>
<span data-ttu-id="6afd4-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6afd4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6afd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afd4-115">-DefaultProfile</span></span>
<span data-ttu-id="6afd4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6afd4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6afd4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afd4-117">CommonParameters</span></span>
<span data-ttu-id="6afd4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6afd4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afd4-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6afd4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afd4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6afd4-120">INPUTS</span></span>

### <span data-ttu-id="6afd4-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afd4-121">PSApplicationGateway</span></span>
<span data-ttu-id="6afd4-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6afd4-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="6afd4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6afd4-123">OUTPUTS</span></span>

### <span data-ttu-id="6afd4-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afd4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6afd4-125">Note</span><span class="sxs-lookup"><span data-stu-id="6afd4-125">NOTES</span></span>

## <span data-ttu-id="6afd4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6afd4-126">RELATED LINKS</span></span>

[<span data-ttu-id="6afd4-127">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afd4-127">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


