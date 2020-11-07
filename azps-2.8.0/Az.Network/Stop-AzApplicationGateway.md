---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 921c770cce5d1f597fa0af96dd30014f9dacb2fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855126"
---
# <span data-ttu-id="cb429-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="cb429-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb429-102">SYNOPSIS</span></span>
<span data-ttu-id="cb429-103">Interrompe un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="cb429-103">Stops an application gateway</span></span>

## <span data-ttu-id="cb429-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb429-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb429-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb429-105">DESCRIPTION</span></span>
<span data-ttu-id="cb429-106">Il cmdlet **Stop-AzApplicationGateway** arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb429-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="cb429-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb429-107">EXAMPLES</span></span>

### <span data-ttu-id="cb429-108">Esempio 1: arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="cb429-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="cb429-109">Questo comando Arresta il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cb429-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="cb429-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb429-110">PARAMETERS</span></span>

### <span data-ttu-id="cb429-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-111">-ApplicationGateway</span></span>
<span data-ttu-id="cb429-112">Specifica il gateway dell'applicazione che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="cb429-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="cb429-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb429-113">-AsJob</span></span>
<span data-ttu-id="cb429-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cb429-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb429-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb429-115">-DefaultProfile</span></span>
<span data-ttu-id="cb429-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb429-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb429-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb429-117">CommonParameters</span></span>
<span data-ttu-id="cb429-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb429-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb429-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb429-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb429-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb429-120">INPUTS</span></span>

### <span data-ttu-id="cb429-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb429-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb429-122">OUTPUTS</span></span>

### <span data-ttu-id="cb429-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb429-124">Note</span><span class="sxs-lookup"><span data-stu-id="cb429-124">NOTES</span></span>

## <span data-ttu-id="cb429-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb429-125">RELATED LINKS</span></span>

[<span data-ttu-id="cb429-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="cb429-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="cb429-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="cb429-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="cb429-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb429-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


