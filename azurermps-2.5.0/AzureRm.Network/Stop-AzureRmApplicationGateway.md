---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 74b8664a9b57089fd116620779354515ea984c79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866028"
---
# <span data-ttu-id="7eeda-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eeda-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="7eeda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7eeda-102">SYNOPSIS</span></span>
<span data-ttu-id="7eeda-103">Interrompe un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7eeda-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eeda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7eeda-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eeda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eeda-105">DESCRIPTION</span></span>
<span data-ttu-id="7eeda-106">Il cmdlet **Stop-AzureRmApplicationGateway** arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7eeda-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="7eeda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7eeda-107">EXAMPLES</span></span>

### <span data-ttu-id="7eeda-108">Esempio 1: arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7eeda-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="7eeda-109">Questo comando Arresta il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7eeda-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="7eeda-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eeda-110">PARAMETERS</span></span>

### <span data-ttu-id="7eeda-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eeda-111">-ApplicationGateway</span></span>
<span data-ttu-id="7eeda-112">Specifica il gateway dell'applicazione che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="7eeda-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="7eeda-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7eeda-113">-AsJob</span></span>
<span data-ttu-id="7eeda-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7eeda-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7eeda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eeda-115">-DefaultProfile</span></span>
<span data-ttu-id="7eeda-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7eeda-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eeda-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eeda-117">CommonParameters</span></span>
<span data-ttu-id="7eeda-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eeda-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eeda-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eeda-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eeda-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7eeda-120">INPUTS</span></span>

### <span data-ttu-id="7eeda-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7eeda-121">System.String</span></span>

## <span data-ttu-id="7eeda-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7eeda-122">OUTPUTS</span></span>

### <span data-ttu-id="7eeda-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eeda-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7eeda-124">Note</span><span class="sxs-lookup"><span data-stu-id="7eeda-124">NOTES</span></span>

## <span data-ttu-id="7eeda-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7eeda-125">RELATED LINKS</span></span>

[<span data-ttu-id="7eeda-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eeda-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="7eeda-127">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eeda-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="7eeda-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eeda-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="7eeda-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eeda-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="7eeda-130">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eeda-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


