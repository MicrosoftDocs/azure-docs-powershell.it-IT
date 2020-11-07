---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 1b852be30b513963f5d311940162078bdf6f692a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866978"
---
# <span data-ttu-id="9db61-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9db61-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="9db61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9db61-102">SYNOPSIS</span></span>
<span data-ttu-id="9db61-103">Aggiorna un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9db61-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9db61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9db61-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9db61-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9db61-105">DESCRIPTION</span></span>
<span data-ttu-id="9db61-106">Il cmdlet **set-AzureRmApplicationGateway** aggiorna un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="9db61-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="9db61-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9db61-107">EXAMPLES</span></span>

### <span data-ttu-id="9db61-108">Esempio 1: aggiornare un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="9db61-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9db61-109">Questo comando Aggiorna il gateway dell'applicazione con le impostazioni nella variabile $AppGw e archivia il gateway aggiornato nella variabile $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="9db61-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="9db61-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9db61-110">PARAMETERS</span></span>

### <span data-ttu-id="9db61-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9db61-111">-ApplicationGateway</span></span>
<span data-ttu-id="9db61-112">Specifica un oggetto gateway dell'applicazione che rappresenta lo stato in cui deve essere impostato il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9db61-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="9db61-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9db61-113">-AsJob</span></span>
<span data-ttu-id="9db61-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9db61-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9db61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db61-115">-DefaultProfile</span></span>
<span data-ttu-id="9db61-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9db61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9db61-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db61-117">CommonParameters</span></span>
<span data-ttu-id="9db61-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db61-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db61-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db61-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db61-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9db61-120">INPUTS</span></span>

### <span data-ttu-id="9db61-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9db61-121">PSApplicationGateway</span></span>
<span data-ttu-id="9db61-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9db61-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="9db61-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9db61-123">OUTPUTS</span></span>

### <span data-ttu-id="9db61-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9db61-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9db61-125">Note</span><span class="sxs-lookup"><span data-stu-id="9db61-125">NOTES</span></span>

## <span data-ttu-id="9db61-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9db61-126">RELATED LINKS</span></span>

[<span data-ttu-id="9db61-127">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9db61-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


