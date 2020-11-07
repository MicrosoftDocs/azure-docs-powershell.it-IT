---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: ba979a12584d526ba7e3a36d13c44b51704b44f6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866062"
---
# <span data-ttu-id="bb593-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb593-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bb593-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb593-102">SYNOPSIS</span></span>
<span data-ttu-id="bb593-103">Rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="bb593-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb593-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb593-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb593-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb593-105">DESCRIPTION</span></span>
<span data-ttu-id="bb593-106">Il cmdlet **Remove-AzureRmApplicationGatewayRedirectConfiguration** rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="bb593-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="bb593-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb593-107">EXAMPLES</span></span>

### <span data-ttu-id="bb593-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb593-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="bb593-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bb593-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="bb593-110">Il secondo comando rimuove la configurazione di reindirizzamento denominata Redirect01 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bb593-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="bb593-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb593-111">PARAMETERS</span></span>

### <span data-ttu-id="bb593-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb593-112">-ApplicationGateway</span></span>
<span data-ttu-id="bb593-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb593-113">The applicationGateway</span></span>

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

### <span data-ttu-id="bb593-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb593-114">-DefaultProfile</span></span>
<span data-ttu-id="bb593-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb593-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb593-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb593-116">-Name</span></span>
<span data-ttu-id="bb593-117">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="bb593-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="bb593-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb593-118">CommonParameters</span></span>
<span data-ttu-id="bb593-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb593-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb593-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb593-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb593-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb593-121">INPUTS</span></span>

### <span data-ttu-id="bb593-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb593-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb593-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb593-123">OUTPUTS</span></span>

### <span data-ttu-id="bb593-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb593-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb593-125">Note</span><span class="sxs-lookup"><span data-stu-id="bb593-125">NOTES</span></span>

## <span data-ttu-id="bb593-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb593-126">RELATED LINKS</span></span>

