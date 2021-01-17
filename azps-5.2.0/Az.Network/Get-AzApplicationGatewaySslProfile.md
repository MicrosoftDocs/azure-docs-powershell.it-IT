---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337867"
---
# <span data-ttu-id="05dfb-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="05dfb-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="05dfb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="05dfb-103">Ottiene il profilo SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05dfb-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="05dfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05dfb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05dfb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="05dfb-106">Il cmdlet **Get-AzApplicationGatewaySslProfile** ottiene il profilo SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05dfb-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="05dfb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05dfb-107">EXAMPLES</span></span>

### <span data-ttu-id="05dfb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05dfb-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="05dfb-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene il profilo SSL SslProfile01 per $AppGw e lo archivia nella variabile $profile.</span><span class="sxs-lookup"><span data-stu-id="05dfb-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="05dfb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05dfb-110">PARAMETERS</span></span>

### <span data-ttu-id="05dfb-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05dfb-111">-ApplicationGateway</span></span>
<span data-ttu-id="05dfb-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05dfb-112">The applicationGateway</span></span>

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

### <span data-ttu-id="05dfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05dfb-113">-DefaultProfile</span></span>
<span data-ttu-id="05dfb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05dfb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05dfb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="05dfb-115">-Name</span></span>
<span data-ttu-id="05dfb-116">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="05dfb-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="05dfb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05dfb-117">CommonParameters</span></span>
<span data-ttu-id="05dfb-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05dfb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05dfb-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05dfb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05dfb-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05dfb-120">INPUTS</span></span>

### <span data-ttu-id="05dfb-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05dfb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="05dfb-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05dfb-122">OUTPUTS</span></span>

### <span data-ttu-id="05dfb-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="05dfb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="05dfb-124">Note</span><span class="sxs-lookup"><span data-stu-id="05dfb-124">NOTES</span></span>

## <span data-ttu-id="05dfb-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05dfb-125">RELATED LINKS</span></span>

[<span data-ttu-id="05dfb-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="05dfb-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="05dfb-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="05dfb-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="05dfb-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="05dfb-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="05dfb-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="05dfb-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)