---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 2490896fa66a3d06a8887e386c2bf6db6ff2f829
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993984"
---
# <span data-ttu-id="adf2f-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="adf2f-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="adf2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="adf2f-103">Ottiene il profilo SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="adf2f-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="adf2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adf2f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adf2f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="adf2f-105">DESCRIPTION</span></span>
<span data-ttu-id="adf2f-106">Il cmdlet **Get-AzApplicationGatewaySslProfile** ottiene il profilo SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="adf2f-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="adf2f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adf2f-107">EXAMPLES</span></span>

### <span data-ttu-id="adf2f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="adf2f-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="adf2f-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile. Il secondo comando recupera il profilo SSLProfile01 per $AppGw e lo archivia nella variabile $profile SSL.</span><span class="sxs-lookup"><span data-stu-id="adf2f-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="adf2f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adf2f-110">PARAMETERS</span></span>

### <span data-ttu-id="adf2f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adf2f-111">-ApplicationGateway</span></span>
<span data-ttu-id="adf2f-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adf2f-112">The applicationGateway</span></span>

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

### <span data-ttu-id="adf2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf2f-113">-DefaultProfile</span></span>
<span data-ttu-id="adf2f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adf2f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adf2f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="adf2f-115">-Name</span></span>
<span data-ttu-id="adf2f-116">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="adf2f-116">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf2f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf2f-117">CommonParameters</span></span>
<span data-ttu-id="adf2f-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adf2f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf2f-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="adf2f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf2f-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="adf2f-120">INPUTS</span></span>

### <span data-ttu-id="adf2f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adf2f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="adf2f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adf2f-122">OUTPUTS</span></span>

### <span data-ttu-id="adf2f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="adf2f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="adf2f-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="adf2f-124">NOTES</span></span>

## <span data-ttu-id="adf2f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adf2f-125">RELATED LINKS</span></span>

[<span data-ttu-id="adf2f-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="adf2f-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="adf2f-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="adf2f-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="adf2f-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="adf2f-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="adf2f-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="adf2f-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)