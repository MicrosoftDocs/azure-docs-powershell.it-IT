---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337855"
---
# <span data-ttu-id="c2a5b-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c2a5b-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="c2a5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a5b-103">Ottiene i criteri SSL del profilo SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2a5b-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="c2a5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2a5b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2a5b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a5b-106">Il cmdlet **Get-AzApplicationGatewaySslProfilePolicy** ottiene i criteri SSL di un profilo SSL del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2a5b-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="c2a5b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2a5b-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a5b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2a5b-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="c2a5b-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c2a5b-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="c2a5b-110">Il secondo comando ottiene il profilo SSL denominato SslProfile01 per $AppGw e lo archivia $SslProfile variabile.</span><span class="sxs-lookup"><span data-stu-id="c2a5b-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="c2a5b-111">L'ultimo comando ottiene i criteri SSL dal profilo SSL $SslProfile e lo archivia nella variabile $sslpolicy.</span><span class="sxs-lookup"><span data-stu-id="c2a5b-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="c2a5b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2a5b-112">PARAMETERS</span></span>

### <span data-ttu-id="c2a5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a5b-113">-DefaultProfile</span></span>
<span data-ttu-id="c2a5b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a5b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a5b-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c2a5b-115">-SslProfile</span></span>
<span data-ttu-id="c2a5b-116">Profilo SSL del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c2a5b-116">The application Gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a5b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a5b-117">CommonParameters</span></span>
<span data-ttu-id="c2a5b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a5b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a5b-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2a5b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a5b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2a5b-120">INPUTS</span></span>

### <span data-ttu-id="c2a5b-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c2a5b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c2a5b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2a5b-122">OUTPUTS</span></span>

### <span data-ttu-id="c2a5b-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c2a5b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c2a5b-124">Note</span><span class="sxs-lookup"><span data-stu-id="c2a5b-124">NOTES</span></span>

## <span data-ttu-id="c2a5b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2a5b-125">RELATED LINKS</span></span>

[<span data-ttu-id="c2a5b-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c2a5b-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="c2a5b-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c2a5b-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="c2a5b-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c2a5b-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="c2a5b-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c2a5b-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)