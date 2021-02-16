---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193518"
---
# <span data-ttu-id="34935-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="34935-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="34935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34935-102">SYNOPSIS</span></span>
<span data-ttu-id="34935-103">Rimuove una configurazione PrivateLink da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="34935-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="34935-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34935-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34935-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34935-105">DESCRIPTION</span></span>
<span data-ttu-id="34935-106">Il cmdlet **Remove-AzApplicationGatewayPrivateLinkConfiguration** rimuove una configurazione privateLink da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="34935-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="34935-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34935-107">EXAMPLES</span></span>

### <span data-ttu-id="34935-108">Esempio 1: Rimuovere la configurazione PrivateLink di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="34935-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="34935-109">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="34935-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="34935-110">Il secondo comando rimuove la configurazione privateLink denominata privateLinkConfig01 dal gateway di applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="34935-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="34935-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34935-111">PARAMETERS</span></span>

### <span data-ttu-id="34935-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34935-112">-ApplicationGateway</span></span>
<span data-ttu-id="34935-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34935-113">The applicationGateway</span></span>

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

### <span data-ttu-id="34935-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34935-114">-DefaultProfile</span></span>
<span data-ttu-id="34935-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34935-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34935-116">-Name</span><span class="sxs-lookup"><span data-stu-id="34935-116">-Name</span></span>
<span data-ttu-id="34935-117">Nome della configurazione PrivateLink del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="34935-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="34935-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34935-118">CommonParameters</span></span>
<span data-ttu-id="34935-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34935-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34935-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34935-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34935-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="34935-121">INPUTS</span></span>

### <span data-ttu-id="34935-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34935-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34935-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34935-123">OUTPUTS</span></span>

### <span data-ttu-id="34935-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34935-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34935-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="34935-125">NOTES</span></span>

## <span data-ttu-id="34935-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34935-126">RELATED LINKS</span></span>

[<span data-ttu-id="34935-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="34935-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="34935-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="34935-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="34935-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="34935-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="34935-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="34935-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)