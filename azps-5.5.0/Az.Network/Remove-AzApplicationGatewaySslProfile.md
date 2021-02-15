---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202599"
---
# <span data-ttu-id="16c83-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="16c83-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="16c83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c83-102">SYNOPSIS</span></span>
<span data-ttu-id="16c83-103">Rimuove il profilo SSL da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="16c83-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="16c83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16c83-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16c83-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16c83-105">DESCRIPTION</span></span>
<span data-ttu-id="16c83-106">Il cmdlet **Remove-AzApplicationGatewaySslProfile** rimuove il profilo SSL da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="16c83-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="16c83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16c83-107">EXAMPLES</span></span>

### <span data-ttu-id="16c83-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16c83-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="16c83-109">Il primo comando ottiene un gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="16c83-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="16c83-110">Il secondo comando rimuove il profilo SSL denominato SslProfile01 dal gateway applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="16c83-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="16c83-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c83-111">PARAMETERS</span></span>

### <span data-ttu-id="16c83-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16c83-112">-ApplicationGateway</span></span>
<span data-ttu-id="16c83-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16c83-113">The applicationGateway</span></span>

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

### <span data-ttu-id="16c83-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c83-114">-DefaultProfile</span></span>
<span data-ttu-id="16c83-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16c83-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c83-116">-Name</span><span class="sxs-lookup"><span data-stu-id="16c83-116">-Name</span></span>
<span data-ttu-id="16c83-117">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="16c83-117">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c83-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c83-118">CommonParameters</span></span>
<span data-ttu-id="16c83-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c83-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c83-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16c83-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c83-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="16c83-121">INPUTS</span></span>

### <span data-ttu-id="16c83-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16c83-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16c83-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16c83-123">OUTPUTS</span></span>

### <span data-ttu-id="16c83-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16c83-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16c83-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="16c83-125">NOTES</span></span>

## <span data-ttu-id="16c83-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16c83-126">RELATED LINKS</span></span>

[<span data-ttu-id="16c83-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="16c83-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="16c83-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="16c83-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="16c83-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="16c83-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="16c83-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="16c83-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)