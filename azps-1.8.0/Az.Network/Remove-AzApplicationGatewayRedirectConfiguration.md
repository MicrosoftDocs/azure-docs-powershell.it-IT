---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d75cbcbf89fde83419b9a1f97c0f66805258c82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678163"
---
# <span data-ttu-id="34e59-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e59-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="34e59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34e59-102">SYNOPSIS</span></span>
<span data-ttu-id="34e59-103">Rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="34e59-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="34e59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34e59-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34e59-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e59-105">DESCRIPTION</span></span>
<span data-ttu-id="34e59-106">Il cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="34e59-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="34e59-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34e59-107">EXAMPLES</span></span>

### <span data-ttu-id="34e59-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34e59-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="34e59-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="34e59-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="34e59-110">Il secondo comando rimuove la configurazione di reindirizzamento denominata Redirect01 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="34e59-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="34e59-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34e59-111">PARAMETERS</span></span>

### <span data-ttu-id="34e59-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e59-112">-ApplicationGateway</span></span>
<span data-ttu-id="34e59-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e59-113">The applicationGateway</span></span>

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

### <span data-ttu-id="34e59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e59-114">-DefaultProfile</span></span>
<span data-ttu-id="34e59-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34e59-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e59-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="34e59-116">-Name</span></span>
<span data-ttu-id="34e59-117">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="34e59-117">The name of the redirect configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e59-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e59-118">CommonParameters</span></span>
<span data-ttu-id="34e59-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e59-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e59-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e59-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e59-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34e59-121">INPUTS</span></span>

### <span data-ttu-id="34e59-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e59-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34e59-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34e59-123">OUTPUTS</span></span>

### <span data-ttu-id="34e59-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e59-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34e59-125">Note</span><span class="sxs-lookup"><span data-stu-id="34e59-125">NOTES</span></span>

## <span data-ttu-id="34e59-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34e59-126">RELATED LINKS</span></span>

[<span data-ttu-id="34e59-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e59-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="34e59-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e59-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="34e59-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e59-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="34e59-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e59-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
