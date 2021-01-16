---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327541"
---
# <span data-ttu-id="8dfec-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8dfec-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="8dfec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dfec-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfec-103">Rimuove il profilo SSL da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8dfec-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="8dfec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dfec-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dfec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dfec-105">DESCRIPTION</span></span>
<span data-ttu-id="8dfec-106">Il cmdlet **Remove-AzApplicationGatewaySslProfile** rimuove il profilo SSL da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8dfec-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="8dfec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dfec-107">EXAMPLES</span></span>

### <span data-ttu-id="8dfec-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8dfec-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="8dfec-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8dfec-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="8dfec-110">Il secondo comando rimuove il profilo SSL denominato SslProfile01 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8dfec-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8dfec-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dfec-111">PARAMETERS</span></span>

### <span data-ttu-id="8dfec-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8dfec-112">-ApplicationGateway</span></span>
<span data-ttu-id="8dfec-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8dfec-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8dfec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfec-114">-DefaultProfile</span></span>
<span data-ttu-id="8dfec-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfec-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dfec-116">-Name</span></span>
<span data-ttu-id="8dfec-117">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="8dfec-117">The name of the ssl profile</span></span>

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

### <span data-ttu-id="8dfec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfec-118">CommonParameters</span></span>
<span data-ttu-id="8dfec-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dfec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfec-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dfec-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfec-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dfec-121">INPUTS</span></span>

### <span data-ttu-id="8dfec-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8dfec-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8dfec-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dfec-123">OUTPUTS</span></span>

### <span data-ttu-id="8dfec-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8dfec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8dfec-125">Note</span><span class="sxs-lookup"><span data-stu-id="8dfec-125">NOTES</span></span>

## <span data-ttu-id="8dfec-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dfec-126">RELATED LINKS</span></span>

[<span data-ttu-id="8dfec-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8dfec-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8dfec-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8dfec-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8dfec-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8dfec-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8dfec-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8dfec-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)