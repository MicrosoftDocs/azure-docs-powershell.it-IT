---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206987"
---
# <span data-ttu-id="ef0e9-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="ef0e9-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="ef0e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0e9-103">Ottenere l'identità assegnata al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef0e9-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="ef0e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef0e9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef0e9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ef0e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ef0e9-106">Il cmdlet **Get-AzApplicationGatewayIdentity** ottiene l'identità assegnata al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef0e9-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="ef0e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef0e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ef0e9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef0e9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="ef0e9-109">In questo esempio viene illustrato come ottenere l'identità del gateway applicazione da Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ef0e9-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="ef0e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef0e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ef0e9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef0e9-111">-ApplicationGateway</span></span>
<span data-ttu-id="ef0e9-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef0e9-112">The applicationGateway</span></span>

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

### <span data-ttu-id="ef0e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0e9-113">-DefaultProfile</span></span>
<span data-ttu-id="ef0e9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef0e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef0e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0e9-115">CommonParameters</span></span>
<span data-ttu-id="ef0e9-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0e9-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef0e9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0e9-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="ef0e9-118">INPUTS</span></span>

### <span data-ttu-id="ef0e9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef0e9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef0e9-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef0e9-120">OUTPUTS</span></span>

### <span data-ttu-id="ef0e9-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ef0e9-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="ef0e9-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="ef0e9-122">NOTES</span></span>

## <span data-ttu-id="ef0e9-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef0e9-123">RELATED LINKS</span></span>
