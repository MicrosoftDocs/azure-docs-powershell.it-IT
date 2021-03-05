---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ab8afdb01a2993330c75b23b02392ee583cad297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996462"
---
# <span data-ttu-id="1d81d-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1d81d-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1d81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d81d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d81d-103">Rimuove il profilo SSL da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d81d-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="1d81d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d81d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d81d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d81d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d81d-106">Il cmdlet **Remove-AzApplicationGatewaySslProfile** rimuove il profilo SSL da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d81d-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="1d81d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d81d-107">EXAMPLES</span></span>

### <span data-ttu-id="1d81d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d81d-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="1d81d-109">Il primo comando ottiene un gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="1d81d-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="1d81d-110">Il secondo comando rimuove il profilo SSL denominato SslProfile01 dal gateway applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1d81d-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1d81d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d81d-111">PARAMETERS</span></span>

### <span data-ttu-id="1d81d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d81d-112">-ApplicationGateway</span></span>
<span data-ttu-id="1d81d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d81d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1d81d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d81d-114">-DefaultProfile</span></span>
<span data-ttu-id="1d81d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d81d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d81d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1d81d-116">-Name</span></span>
<span data-ttu-id="1d81d-117">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="1d81d-117">The name of the ssl profile</span></span>

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

### <span data-ttu-id="1d81d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d81d-118">CommonParameters</span></span>
<span data-ttu-id="1d81d-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d81d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d81d-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d81d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d81d-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d81d-121">INPUTS</span></span>

### <span data-ttu-id="1d81d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d81d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1d81d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d81d-123">OUTPUTS</span></span>

### <span data-ttu-id="1d81d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d81d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1d81d-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d81d-125">NOTES</span></span>

## <span data-ttu-id="1d81d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d81d-126">RELATED LINKS</span></span>

[<span data-ttu-id="1d81d-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1d81d-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1d81d-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1d81d-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1d81d-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1d81d-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1d81d-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1d81d-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)