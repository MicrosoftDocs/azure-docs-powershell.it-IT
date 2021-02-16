---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177871"
---
# <span data-ttu-id="9f874-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="9f874-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="9f874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f874-102">SYNOPSIS</span></span>
<span data-ttu-id="9f874-103">Crea un'azione di recapito.</span><span class="sxs-lookup"><span data-stu-id="9f874-103">Creates a delivery action.</span></span>

## <span data-ttu-id="9f874-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f874-104">SYNTAX</span></span>

### <span data-ttu-id="9f874-105">CacheExpirationActionParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f874-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f874-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f874-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f874-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f874-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f874-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f874-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f874-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f874-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f874-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9f874-110">DESCRIPTION</span></span>
<span data-ttu-id="9f874-111">Il cmdlet **New-AzCdnDeliveryRule** crea una regola di recapito per la creazione dell'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="9f874-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="9f874-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f874-112">EXAMPLES</span></span>

### <span data-ttu-id="9f874-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f874-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="9f874-114">Creare una regola di recapito semplice.</span><span class="sxs-lookup"><span data-stu-id="9f874-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="9f874-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f874-115">PARAMETERS</span></span>

### <span data-ttu-id="9f874-116">-Action</span><span class="sxs-lookup"><span data-stu-id="9f874-116">-Action</span></span>
<span data-ttu-id="9f874-117">Azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="9f874-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="9f874-118">-CacheBehavior</span></span>
<span data-ttu-id="9f874-119">Comportamento della memorizzazione nella cache per l'azione</span><span class="sxs-lookup"><span data-stu-id="9f874-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="9f874-120">-CacheDuration</span></span>
<span data-ttu-id="9f874-121">Durata per cui il contenuto deve essere memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="9f874-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="9f874-122">Il formato consentito è \[ d. \] hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="9f874-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-123">-Custom Deframment</span><span class="sxs-lookup"><span data-stu-id="9f874-123">-CustomFragment</span></span>
<span data-ttu-id="9f874-124">Frammento da aggiungere all'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="9f874-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="9f874-125">Frammento è la parte dell'URL che viene dopo #.</span><span class="sxs-lookup"><span data-stu-id="9f874-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="9f874-126">Non includere il valore di errore #.</span><span class="sxs-lookup"><span data-stu-id="9f874-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="9f874-127">-CustomHostname</span></span>
<span data-ttu-id="9f874-128">Host da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="9f874-128">Host to redirect.</span></span>
<span data-ttu-id="9f874-129">Lasciare vuoto per usare l'host della posta in arrivo come host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9f874-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="9f874-130">-CustomPath</span></span>
<span data-ttu-id="9f874-131">Percorso completo da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="9f874-131">The full path to redirect.</span></span>
<span data-ttu-id="9f874-132">Il percorso non può essere vuoto e deve iniziare con /.</span><span class="sxs-lookup"><span data-stu-id="9f874-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="9f874-133">Lasciare vuoto per usare il percorso in ingresso come percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9f874-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="9f874-134">-CustomQueryString</span></span>
<span data-ttu-id="9f874-135">Set di stringhe di query da inserire nell'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="9f874-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="9f874-136">L'impostazione di questo valore sostituirebbe qualsiasi stringa di query esistente; lasciare vuoto per mantenere la stringa di query in ingresso.</span><span class="sxs-lookup"><span data-stu-id="9f874-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="9f874-137">La stringa di query deve essere nel \<key\> = \<value\> formato.</span><span class="sxs-lookup"><span data-stu-id="9f874-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="9f874-138">?</span><span class="sxs-lookup"><span data-stu-id="9f874-138">?</span></span> <span data-ttu-id="9f874-139">e & verranno aggiunti automaticamente, in modo da non includerli.</span><span class="sxs-lookup"><span data-stu-id="9f874-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f874-140">-DefaultProfile</span></span>
<span data-ttu-id="9f874-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f874-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f874-142">-Destination</span><span class="sxs-lookup"><span data-stu-id="9f874-142">-Destination</span></span>
<span data-ttu-id="9f874-143">Definire l'URL relativo con cui verranno riscritte le richieste precedenti.</span><span class="sxs-lookup"><span data-stu-id="9f874-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="9f874-144">-DestinationProtocol</span></span>
<span data-ttu-id="9f874-145">Protocollo da usare per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="9f874-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="9f874-146">Il valore predefinito è MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="9f874-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="9f874-147">-HeaderActionType</span></span>
<span data-ttu-id="9f874-148">Se modificare l'intestazione della richiesta o della risposta</span><span class="sxs-lookup"><span data-stu-id="9f874-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="9f874-149">-HeaderName</span></span>
<span data-ttu-id="9f874-150">Nome dell'intestazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="9f874-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="9f874-151">-PreservePath</span></span>
<span data-ttu-id="9f874-152">Se mantenere il percorso non corrispondente.</span><span class="sxs-lookup"><span data-stu-id="9f874-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="9f874-153">-QueryParameter</span></span>
<span data-ttu-id="9f874-154">Parametri della query da includere o escludere (separati da virgola).</span><span class="sxs-lookup"><span data-stu-id="9f874-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="9f874-155">-QueryStringBehavior</span></span>
<span data-ttu-id="9f874-156">Comportamento di QueryString per le richieste</span><span class="sxs-lookup"><span data-stu-id="9f874-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="9f874-157">-RedirectType</span></span>
<span data-ttu-id="9f874-158">Tipo di reindirizzamento che la regola userà per il reindirizzamento del traffico</span><span class="sxs-lookup"><span data-stu-id="9f874-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-159">-Source Sistema</span><span class="sxs-lookup"><span data-stu-id="9f874-159">-SourcePattern</span></span>
<span data-ttu-id="9f874-160">Definire un criterio URI della richiesta che identifichi il tipo di richieste che possono essere riscritte.</span><span class="sxs-lookup"><span data-stu-id="9f874-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="9f874-161">Se il valore è vuoto, viene trovata una corrispondenza per tutte le stringhe.</span><span class="sxs-lookup"><span data-stu-id="9f874-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-162">-Value</span><span class="sxs-lookup"><span data-stu-id="9f874-162">-Value</span></span>
<span data-ttu-id="9f874-163">Valore per l'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="9f874-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f874-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f874-164">CommonParameters</span></span>
<span data-ttu-id="9f874-165">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f874-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f874-166">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9f874-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f874-167">INPUT</span><span class="sxs-lookup"><span data-stu-id="9f874-167">INPUTS</span></span>

### <span data-ttu-id="9f874-168">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9f874-168">None</span></span>

## <span data-ttu-id="9f874-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f874-169">OUTPUTS</span></span>

### <span data-ttu-id="9f874-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="9f874-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="9f874-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="9f874-171">NOTES</span></span>

## <span data-ttu-id="9f874-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f874-172">RELATED LINKS</span></span>
