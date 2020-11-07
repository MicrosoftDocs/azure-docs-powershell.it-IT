---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: c9443c93745c1f6db9372b8f845f3ac399e51398
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860869"
---
# <span data-ttu-id="9c71f-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c71f-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9c71f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c71f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c71f-103">Ottiene una configurazione di reindirizzamento esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c71f-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="9c71f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c71f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c71f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c71f-105">DESCRIPTION</span></span>
<span data-ttu-id="9c71f-106">Il cmdlet **Get-AzApplicationGatewayRedirectConfiguration** ottiene una configurazione di reindirizzamento esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c71f-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="9c71f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c71f-107">EXAMPLES</span></span>

### <span data-ttu-id="9c71f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c71f-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="9c71f-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9c71f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="9c71f-110">Il secondo comando consente di ottenere la configurazione di reindirizzamento denominata Redirect01 dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9c71f-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="9c71f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c71f-111">PARAMETERS</span></span>

### <span data-ttu-id="9c71f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c71f-112">-ApplicationGateway</span></span>
<span data-ttu-id="9c71f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c71f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9c71f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c71f-114">-DefaultProfile</span></span>
<span data-ttu-id="9c71f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c71f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c71f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c71f-116">-Name</span></span>
<span data-ttu-id="9c71f-117">Nome della regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="9c71f-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="9c71f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c71f-118">CommonParameters</span></span>
<span data-ttu-id="9c71f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c71f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c71f-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c71f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c71f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c71f-121">INPUTS</span></span>

### <span data-ttu-id="9c71f-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c71f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c71f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c71f-123">OUTPUTS</span></span>

### <span data-ttu-id="9c71f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c71f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="9c71f-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9c71f-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9c71f-126">Note</span><span class="sxs-lookup"><span data-stu-id="9c71f-126">NOTES</span></span>

## <span data-ttu-id="9c71f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c71f-127">RELATED LINKS</span></span>

