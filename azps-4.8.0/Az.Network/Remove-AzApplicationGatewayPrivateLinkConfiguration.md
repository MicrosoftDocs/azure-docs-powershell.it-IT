---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032908"
---
# <span data-ttu-id="152c3-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="152c3-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="152c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="152c3-102">SYNOPSIS</span></span>
<span data-ttu-id="152c3-103">Rimuove una configurazione privateLink da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="152c3-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="152c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="152c3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="152c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="152c3-105">DESCRIPTION</span></span>
<span data-ttu-id="152c3-106">Il cmdlet **Remove-AzApplicationGatewayPrivateLinkConfiguration** rimuove una configurazione privateLink da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="152c3-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="152c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="152c3-107">EXAMPLES</span></span>

### <span data-ttu-id="152c3-108">Esempio 1: rimuovere una configurazione di PrivateLink gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="152c3-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="152c3-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="152c3-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="152c3-110">Il secondo comando rimuove la configurazione privateLink denominata privateLinkConfig01 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="152c3-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="152c3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="152c3-111">PARAMETERS</span></span>

### <span data-ttu-id="152c3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="152c3-112">-ApplicationGateway</span></span>
<span data-ttu-id="152c3-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="152c3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="152c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152c3-114">-DefaultProfile</span></span>
<span data-ttu-id="152c3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="152c3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="152c3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="152c3-116">-Name</span></span>
<span data-ttu-id="152c3-117">Nome della configurazione di privateLink del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="152c3-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="152c3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152c3-118">CommonParameters</span></span>
<span data-ttu-id="152c3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152c3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152c3-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="152c3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152c3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="152c3-121">INPUTS</span></span>

### <span data-ttu-id="152c3-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="152c3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="152c3-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="152c3-123">OUTPUTS</span></span>

### <span data-ttu-id="152c3-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="152c3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="152c3-125">Note</span><span class="sxs-lookup"><span data-stu-id="152c3-125">NOTES</span></span>

## <span data-ttu-id="152c3-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="152c3-126">RELATED LINKS</span></span>

[<span data-ttu-id="152c3-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="152c3-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="152c3-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="152c3-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="152c3-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="152c3-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="152c3-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="152c3-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)