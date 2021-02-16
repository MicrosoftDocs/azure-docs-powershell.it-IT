---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193934"
---
# <span data-ttu-id="5ba81-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ba81-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="5ba81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba81-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba81-103">Ottiene i criteri SSL di un profilo SSL del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ba81-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="5ba81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ba81-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba81-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ba81-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba81-106">Il cmdlet **Get-AzApplicationGatewaySslProfilePolicy** ottiene il criterio SSL di un profilo SSL del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ba81-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="5ba81-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ba81-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba81-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ba81-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="5ba81-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ba81-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="5ba81-110">Il secondo comando recupera il profilo SSL denominato SslProfile01 per $AppGw e lo archivia $SslProfile variabile.</span><span class="sxs-lookup"><span data-stu-id="5ba81-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="5ba81-111">L'ultimo comando recupera il criterio SSL dal profilo SSL $SslProfile e lo archivia nella $sslpolicy variabile.</span><span class="sxs-lookup"><span data-stu-id="5ba81-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="5ba81-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ba81-112">PARAMETERS</span></span>

### <span data-ttu-id="5ba81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba81-113">-DefaultProfile</span></span>
<span data-ttu-id="5ba81-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba81-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="5ba81-115">-SslProfile</span></span>
<span data-ttu-id="5ba81-116">Profilo SSL del Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5ba81-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="5ba81-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba81-117">CommonParameters</span></span>
<span data-ttu-id="5ba81-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba81-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba81-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ba81-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba81-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ba81-120">INPUTS</span></span>

### <span data-ttu-id="5ba81-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5ba81-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5ba81-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ba81-122">OUTPUTS</span></span>

### <span data-ttu-id="5ba81-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ba81-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5ba81-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ba81-124">NOTES</span></span>

## <span data-ttu-id="5ba81-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ba81-125">RELATED LINKS</span></span>

[<span data-ttu-id="5ba81-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ba81-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5ba81-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ba81-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5ba81-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ba81-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5ba81-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ba81-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)