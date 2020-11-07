---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853562"
---
# <span data-ttu-id="e9b10-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b10-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e9b10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9b10-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b10-103">Crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9b10-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="e9b10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9b10-104">SYNTAX</span></span>

### <span data-ttu-id="e9b10-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b10-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9b10-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e9b10-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9b10-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="e9b10-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b10-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9b10-108">DESCRIPTION</span></span>
<span data-ttu-id="e9b10-109">**Il cmdlet New-AzApplicationGatewayRedirectConfiguration** crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9b10-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="e9b10-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9b10-110">EXAMPLES</span></span>

### <span data-ttu-id="e9b10-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9b10-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="e9b10-112">Questo comando crea una configurazione di reindirizzamento denominata Redirect01 e archivia il risultato nella variabile denominata $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="e9b10-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="e9b10-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9b10-113">PARAMETERS</span></span>

### <span data-ttu-id="e9b10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b10-114">-DefaultProfile</span></span>
<span data-ttu-id="e9b10-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b10-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b10-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="e9b10-116">-IncludePath</span></span>
<span data-ttu-id="e9b10-117">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="e9b10-117">Include path in the redirected url.</span></span>
<span data-ttu-id="e9b10-118">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="e9b10-118">Default is true.</span></span>

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

### <span data-ttu-id="e9b10-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="e9b10-119">-IncludeQueryString</span></span>
<span data-ttu-id="e9b10-120">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="e9b10-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="e9b10-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="e9b10-121">Default is true.</span></span>

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

### <span data-ttu-id="e9b10-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9b10-122">-Name</span></span>
<span data-ttu-id="e9b10-123">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="e9b10-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="e9b10-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="e9b10-124">-RedirectType</span></span>
<span data-ttu-id="e9b10-125">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="e9b10-125">The type of redirect</span></span>

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

### <span data-ttu-id="e9b10-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="e9b10-126">-TargetListener</span></span>
<span data-ttu-id="e9b10-127">Listener HTTP per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="e9b10-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="e9b10-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="e9b10-128">-TargetListenerID</span></span>
<span data-ttu-id="e9b10-129">ID del listener HTTP per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="e9b10-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="e9b10-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="e9b10-130">-TargetUrl</span></span>
<span data-ttu-id="e9b10-131">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="e9b10-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="e9b10-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b10-132">CommonParameters</span></span>
<span data-ttu-id="e9b10-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b10-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b10-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b10-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b10-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9b10-135">INPUTS</span></span>

### <span data-ttu-id="e9b10-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e9b10-136">None</span></span>

## <span data-ttu-id="e9b10-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9b10-137">OUTPUTS</span></span>

### <span data-ttu-id="e9b10-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b10-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e9b10-139">Note</span><span class="sxs-lookup"><span data-stu-id="e9b10-139">NOTES</span></span>

## <span data-ttu-id="e9b10-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9b10-140">RELATED LINKS</span></span>

[<span data-ttu-id="e9b10-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b10-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e9b10-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b10-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e9b10-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b10-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e9b10-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b10-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
