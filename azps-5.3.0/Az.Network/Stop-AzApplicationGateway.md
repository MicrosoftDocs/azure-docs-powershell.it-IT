---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486519"
---
# <span data-ttu-id="75f8b-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="75f8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="75f8b-103">Interrompe un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="75f8b-103">Stops an application gateway</span></span>

## <span data-ttu-id="75f8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75f8b-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f8b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="75f8b-106">Il cmdlet **Stop-AzApplicationGateway** arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="75f8b-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="75f8b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="75f8b-108">Esempio 1: arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="75f8b-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="75f8b-109">Questo comando Arresta il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="75f8b-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="75f8b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75f8b-110">PARAMETERS</span></span>

### <span data-ttu-id="75f8b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-111">-ApplicationGateway</span></span>
<span data-ttu-id="75f8b-112">Specifica il gateway dell'applicazione che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="75f8b-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="75f8b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75f8b-113">-AsJob</span></span>
<span data-ttu-id="75f8b-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="75f8b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75f8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f8b-115">-DefaultProfile</span></span>
<span data-ttu-id="75f8b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75f8b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75f8b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f8b-117">CommonParameters</span></span>
<span data-ttu-id="75f8b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f8b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f8b-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f8b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f8b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75f8b-120">INPUTS</span></span>

### <span data-ttu-id="75f8b-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75f8b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75f8b-122">OUTPUTS</span></span>

### <span data-ttu-id="75f8b-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75f8b-124">Note</span><span class="sxs-lookup"><span data-stu-id="75f8b-124">NOTES</span></span>

## <span data-ttu-id="75f8b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75f8b-125">RELATED LINKS</span></span>

[<span data-ttu-id="75f8b-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="75f8b-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="75f8b-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="75f8b-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="75f8b-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75f8b-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


