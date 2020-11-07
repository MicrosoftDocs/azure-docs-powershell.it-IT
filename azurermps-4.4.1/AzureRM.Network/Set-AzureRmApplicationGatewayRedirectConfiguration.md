---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 23b27fc0b8b2a8d55a2af91d808b846e4de324a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686162"
---
# <span data-ttu-id="9bf27-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bf27-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9bf27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bf27-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf27-103">Imposta la configurazione di reindirizzamento in un gateway di applicazioni esistente.</span><span class="sxs-lookup"><span data-stu-id="9bf27-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bf27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bf27-104">SYNTAX</span></span>

### <span data-ttu-id="9bf27-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf27-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bf27-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9bf27-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bf27-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="9bf27-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf27-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bf27-108">DESCRIPTION</span></span>
<span data-ttu-id="9bf27-109">**Il cmdlet Set-AzureRmApplicationGatewayRequestRoutingRule** modifica una configurazione di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="9bf27-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="9bf27-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bf27-110">EXAMPLES</span></span>

### <span data-ttu-id="9bf27-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9bf27-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="9bf27-112">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9bf27-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9bf27-113">Il secondo comando modifica la configurazione di reindirizzamento per il gateway dell'applicazione per reindirizzare il tipo permanente e usare un URL di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9bf27-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="9bf27-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bf27-114">PARAMETERS</span></span>

### <span data-ttu-id="9bf27-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bf27-115">-ApplicationGateway</span></span>
<span data-ttu-id="9bf27-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bf27-116">The applicationGateway</span></span>

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

### <span data-ttu-id="9bf27-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="9bf27-117">-IncludePath</span></span>
<span data-ttu-id="9bf27-118">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="9bf27-118">Include path in the redirected url.</span></span>
<span data-ttu-id="9bf27-119">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="9bf27-119">Default is true.</span></span>

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

### <span data-ttu-id="9bf27-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="9bf27-120">-IncludeQueryString</span></span>
<span data-ttu-id="9bf27-121">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="9bf27-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="9bf27-122">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="9bf27-122">Default is true.</span></span>

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

### <span data-ttu-id="9bf27-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bf27-123">-Name</span></span>
<span data-ttu-id="9bf27-124">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="9bf27-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="9bf27-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="9bf27-125">-RedirectType</span></span>
<span data-ttu-id="9bf27-126">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="9bf27-126">The type of redirect</span></span>

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

### <span data-ttu-id="9bf27-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="9bf27-127">-TargetListener</span></span>
<span data-ttu-id="9bf27-128">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="9bf27-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="9bf27-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="9bf27-129">-TargetListenerID</span></span>
<span data-ttu-id="9bf27-130">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="9bf27-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="9bf27-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="9bf27-131">-TargetUrl</span></span>
<span data-ttu-id="9bf27-132">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="9bf27-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="9bf27-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf27-133">-DefaultProfile</span></span>
<span data-ttu-id="9bf27-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf27-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf27-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf27-135">CommonParameters</span></span>
<span data-ttu-id="9bf27-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf27-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf27-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf27-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf27-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bf27-138">INPUTS</span></span>

### <span data-ttu-id="9bf27-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bf27-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9bf27-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bf27-140">OUTPUTS</span></span>

### <span data-ttu-id="9bf27-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bf27-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9bf27-142">Note</span><span class="sxs-lookup"><span data-stu-id="9bf27-142">NOTES</span></span>

## <span data-ttu-id="9bf27-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bf27-143">RELATED LINKS</span></span>

