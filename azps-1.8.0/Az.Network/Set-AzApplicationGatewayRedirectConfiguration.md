---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 746d1bb37bd49acfdc0a353c9985508f50514073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678002"
---
# <span data-ttu-id="03bd3-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bd3-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="03bd3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="03bd3-103">Imposta la configurazione di reindirizzamento in un gateway di applicazioni esistente.</span><span class="sxs-lookup"><span data-stu-id="03bd3-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="03bd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03bd3-104">SYNTAX</span></span>

### <span data-ttu-id="03bd3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="03bd3-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03bd3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="03bd3-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03bd3-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="03bd3-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03bd3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03bd3-108">DESCRIPTION</span></span>
<span data-ttu-id="03bd3-109">**Il cmdlet Set-AzApplicationGatewayRequestRoutingRule** modifica una configurazione di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="03bd3-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="03bd3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03bd3-110">EXAMPLES</span></span>

### <span data-ttu-id="03bd3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03bd3-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="03bd3-112">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="03bd3-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="03bd3-113">Il secondo comando modifica la configurazione di reindirizzamento per il gateway dell'applicazione per reindirizzare il tipo permanente e usare un URL di destinazione.</span><span class="sxs-lookup"><span data-stu-id="03bd3-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="03bd3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03bd3-114">PARAMETERS</span></span>

### <span data-ttu-id="03bd3-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03bd3-115">-ApplicationGateway</span></span>
<span data-ttu-id="03bd3-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03bd3-116">The applicationGateway</span></span>

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

### <span data-ttu-id="03bd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bd3-117">-DefaultProfile</span></span>
<span data-ttu-id="03bd3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03bd3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03bd3-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="03bd3-119">-IncludePath</span></span>
<span data-ttu-id="03bd3-120">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="03bd3-120">Include path in the redirected url.</span></span>
<span data-ttu-id="03bd3-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="03bd3-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bd3-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="03bd3-122">-IncludeQueryString</span></span>
<span data-ttu-id="03bd3-123">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="03bd3-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="03bd3-124">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="03bd3-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bd3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="03bd3-125">-Name</span></span>
<span data-ttu-id="03bd3-126">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="03bd3-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="03bd3-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="03bd3-127">-RedirectType</span></span>
<span data-ttu-id="03bd3-128">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="03bd3-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bd3-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="03bd3-129">-TargetListener</span></span>
<span data-ttu-id="03bd3-130">Listener HTTP per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="03bd3-130">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bd3-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="03bd3-131">-TargetListenerID</span></span>
<span data-ttu-id="03bd3-132">ID del listener HTTP per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="03bd3-132">ID of HTTP listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bd3-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="03bd3-133">-TargetUrl</span></span>
<span data-ttu-id="03bd3-134">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="03bd3-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bd3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bd3-135">CommonParameters</span></span>
<span data-ttu-id="03bd3-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bd3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bd3-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bd3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bd3-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03bd3-138">INPUTS</span></span>

### <span data-ttu-id="03bd3-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03bd3-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="03bd3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03bd3-140">OUTPUTS</span></span>

### <span data-ttu-id="03bd3-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03bd3-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="03bd3-142">Note</span><span class="sxs-lookup"><span data-stu-id="03bd3-142">NOTES</span></span>

## <span data-ttu-id="03bd3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03bd3-143">RELATED LINKS</span></span>

[<span data-ttu-id="03bd3-144">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bd3-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="03bd3-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bd3-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="03bd3-146">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bd3-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="03bd3-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bd3-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
