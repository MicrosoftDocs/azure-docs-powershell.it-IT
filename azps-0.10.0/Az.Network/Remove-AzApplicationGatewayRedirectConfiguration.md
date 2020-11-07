---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e965f2cdbd9909003a07ea6c6addd198110e456f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860354"
---
# <span data-ttu-id="cbd68-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbd68-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="cbd68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbd68-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd68-103">Rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="cbd68-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="cbd68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbd68-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbd68-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbd68-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd68-106">Il cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="cbd68-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="cbd68-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbd68-107">EXAMPLES</span></span>

### <span data-ttu-id="cbd68-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cbd68-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="cbd68-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cbd68-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="cbd68-110">Il secondo comando rimuove la configurazione di reindirizzamento denominata Redirect01 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cbd68-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="cbd68-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbd68-111">PARAMETERS</span></span>

### <span data-ttu-id="cbd68-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbd68-112">-ApplicationGateway</span></span>
<span data-ttu-id="cbd68-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbd68-113">The applicationGateway</span></span>

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

### <span data-ttu-id="cbd68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd68-114">-DefaultProfile</span></span>
<span data-ttu-id="cbd68-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd68-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbd68-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbd68-116">-Name</span></span>
<span data-ttu-id="cbd68-117">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="cbd68-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="cbd68-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd68-118">CommonParameters</span></span>
<span data-ttu-id="cbd68-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd68-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd68-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd68-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd68-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbd68-121">INPUTS</span></span>

### <span data-ttu-id="cbd68-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbd68-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cbd68-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbd68-123">OUTPUTS</span></span>

### <span data-ttu-id="cbd68-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbd68-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cbd68-125">Note</span><span class="sxs-lookup"><span data-stu-id="cbd68-125">NOTES</span></span>

## <span data-ttu-id="cbd68-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbd68-126">RELATED LINKS</span></span>

