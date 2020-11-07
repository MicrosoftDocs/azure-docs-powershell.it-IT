---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: f5a0c703640d540dfd5a47f643694f56f87e0438
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687042"
---
# <span data-ttu-id="0810c-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0810c-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="0810c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0810c-102">SYNOPSIS</span></span>
<span data-ttu-id="0810c-103">Rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="0810c-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0810c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0810c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0810c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0810c-105">DESCRIPTION</span></span>
<span data-ttu-id="0810c-106">Il cmdlet **Remove-AzureRmApplicationGatewayRedirectConfiguration** rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="0810c-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="0810c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0810c-107">EXAMPLES</span></span>

### <span data-ttu-id="0810c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0810c-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="0810c-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0810c-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0810c-110">Il secondo comando rimuove la configurazione di reindirizzamento denominata Redirect01 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0810c-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0810c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0810c-111">PARAMETERS</span></span>

### <span data-ttu-id="0810c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0810c-112">-ApplicationGateway</span></span>
<span data-ttu-id="0810c-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0810c-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0810c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0810c-114">-DefaultProfile</span></span>
<span data-ttu-id="0810c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0810c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0810c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0810c-116">-Name</span></span>
<span data-ttu-id="0810c-117">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="0810c-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="0810c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0810c-118">CommonParameters</span></span>
<span data-ttu-id="0810c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0810c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0810c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0810c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0810c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0810c-121">INPUTS</span></span>

### <span data-ttu-id="0810c-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0810c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0810c-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0810c-123">OUTPUTS</span></span>

### <span data-ttu-id="0810c-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0810c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0810c-125">Note</span><span class="sxs-lookup"><span data-stu-id="0810c-125">NOTES</span></span>

## <span data-ttu-id="0810c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0810c-126">RELATED LINKS</span></span>

