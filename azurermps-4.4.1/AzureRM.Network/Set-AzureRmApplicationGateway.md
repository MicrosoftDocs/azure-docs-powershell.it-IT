---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: f755c08b880a9ec97315931843d6dca6f5fc3229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522104"
---
# <span data-ttu-id="66b1f-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66b1f-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="66b1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="66b1f-103">Aggiorna un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66b1f-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66b1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66b1f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66b1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="66b1f-106">Il cmdlet **set-AzureRmApplicationGateway** aggiorna un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="66b1f-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="66b1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66b1f-107">EXAMPLES</span></span>

### <span data-ttu-id="66b1f-108">Esempio 1: aggiornare un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="66b1f-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="66b1f-109">Questo comando Aggiorna il gateway dell'applicazione con le impostazioni nella variabile $AppGw e archivia il gateway aggiornato nella variabile $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="66b1f-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="66b1f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66b1f-110">PARAMETERS</span></span>

### <span data-ttu-id="66b1f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66b1f-111">-ApplicationGateway</span></span>
<span data-ttu-id="66b1f-112">Specifica un oggetto gateway dell'applicazione che rappresenta lo stato in cui deve essere impostato il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66b1f-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="66b1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b1f-113">-DefaultProfile</span></span>
<span data-ttu-id="66b1f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66b1f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b1f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b1f-115">CommonParameters</span></span>
<span data-ttu-id="66b1f-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b1f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b1f-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b1f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b1f-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66b1f-118">INPUTS</span></span>

### <span data-ttu-id="66b1f-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66b1f-119">PSApplicationGateway</span></span>
<span data-ttu-id="66b1f-120">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="66b1f-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="66b1f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66b1f-121">OUTPUTS</span></span>

### <span data-ttu-id="66b1f-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66b1f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66b1f-123">Note</span><span class="sxs-lookup"><span data-stu-id="66b1f-123">NOTES</span></span>

## <span data-ttu-id="66b1f-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66b1f-124">RELATED LINKS</span></span>

[<span data-ttu-id="66b1f-125">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66b1f-125">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


