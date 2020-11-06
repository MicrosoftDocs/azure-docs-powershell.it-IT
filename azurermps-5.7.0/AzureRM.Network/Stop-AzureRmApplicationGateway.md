---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: cf8a639b6ebbe2b5ea7c0e07f212de3c742e7556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515536"
---
# <span data-ttu-id="048aa-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048aa-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="048aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="048aa-102">SYNOPSIS</span></span>
<span data-ttu-id="048aa-103">Interrompe un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="048aa-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="048aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="048aa-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="048aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="048aa-105">DESCRIPTION</span></span>
<span data-ttu-id="048aa-106">Il cmdlet **Stop-AzureRmApplicationGateway** arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="048aa-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="048aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="048aa-107">EXAMPLES</span></span>

### <span data-ttu-id="048aa-108">Esempio 1: arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="048aa-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="048aa-109">Questo comando Arresta il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="048aa-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="048aa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="048aa-110">PARAMETERS</span></span>

### <span data-ttu-id="048aa-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048aa-111">-ApplicationGateway</span></span>
<span data-ttu-id="048aa-112">Specifica il gateway dell'applicazione che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="048aa-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="048aa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="048aa-113">-AsJob</span></span>
<span data-ttu-id="048aa-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="048aa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="048aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048aa-115">-DefaultProfile</span></span>
<span data-ttu-id="048aa-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="048aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="048aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048aa-117">CommonParameters</span></span>
<span data-ttu-id="048aa-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048aa-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048aa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048aa-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="048aa-120">INPUTS</span></span>

### <span data-ttu-id="048aa-121">System. String</span><span class="sxs-lookup"><span data-stu-id="048aa-121">System.String</span></span>

## <span data-ttu-id="048aa-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="048aa-122">OUTPUTS</span></span>

### <span data-ttu-id="048aa-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048aa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="048aa-124">Note</span><span class="sxs-lookup"><span data-stu-id="048aa-124">NOTES</span></span>

## <span data-ttu-id="048aa-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="048aa-125">RELATED LINKS</span></span>

[<span data-ttu-id="048aa-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048aa-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="048aa-127">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048aa-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="048aa-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048aa-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="048aa-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048aa-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="048aa-130">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048aa-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


