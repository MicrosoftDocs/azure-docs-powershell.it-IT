---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: b6bfe8b7064324dea353543e0e9debe77e4b2edd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022746"
---
# <span data-ttu-id="b2299-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2299-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b2299-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2299-102">SYNOPSIS</span></span>
<span data-ttu-id="b2299-103">Crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2299-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="b2299-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2299-104">SYNTAX</span></span>

### <span data-ttu-id="b2299-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2299-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2299-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b2299-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2299-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="b2299-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2299-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2299-108">DESCRIPTION</span></span>
<span data-ttu-id="b2299-109">**Il cmdlet New-AzApplicationGatewayRedirectConfiguration** crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2299-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="b2299-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2299-110">EXAMPLES</span></span>

### <span data-ttu-id="b2299-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2299-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="b2299-112">Questo comando crea una configurazione di reindirizzamento denominata Redirect01 e archivia il risultato nella variabile denominata $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="b2299-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="b2299-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2299-113">PARAMETERS</span></span>

### <span data-ttu-id="b2299-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2299-114">-DefaultProfile</span></span>
<span data-ttu-id="b2299-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2299-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2299-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="b2299-116">-IncludePath</span></span>
<span data-ttu-id="b2299-117">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="b2299-117">Include path in the redirected url.</span></span>
<span data-ttu-id="b2299-118">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="b2299-118">Default is true.</span></span>

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

### <span data-ttu-id="b2299-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="b2299-119">-IncludeQueryString</span></span>
<span data-ttu-id="b2299-120">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="b2299-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="b2299-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="b2299-121">Default is true.</span></span>

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

### <span data-ttu-id="b2299-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2299-122">-Name</span></span>
<span data-ttu-id="b2299-123">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b2299-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="b2299-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="b2299-124">-RedirectType</span></span>
<span data-ttu-id="b2299-125">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b2299-125">The type of redirect</span></span>

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

### <span data-ttu-id="b2299-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="b2299-126">-TargetListener</span></span>
<span data-ttu-id="b2299-127">Listener HTTP per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="b2299-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="b2299-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="b2299-128">-TargetListenerID</span></span>
<span data-ttu-id="b2299-129">ID del listener HTTP per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="b2299-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="b2299-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="b2299-130">-TargetUrl</span></span>
<span data-ttu-id="b2299-131">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b2299-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="b2299-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2299-132">CommonParameters</span></span>
<span data-ttu-id="b2299-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2299-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2299-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2299-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2299-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2299-135">INPUTS</span></span>

### <span data-ttu-id="b2299-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b2299-136">None</span></span>

## <span data-ttu-id="b2299-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2299-137">OUTPUTS</span></span>

### <span data-ttu-id="b2299-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2299-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b2299-139">Note</span><span class="sxs-lookup"><span data-stu-id="b2299-139">NOTES</span></span>

## <span data-ttu-id="b2299-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2299-140">RELATED LINKS</span></span>

[<span data-ttu-id="b2299-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2299-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="b2299-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2299-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="b2299-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2299-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="b2299-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2299-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
