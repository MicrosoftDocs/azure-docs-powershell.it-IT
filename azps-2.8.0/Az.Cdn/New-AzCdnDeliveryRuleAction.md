---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675545"
---
# <span data-ttu-id="71086-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="71086-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="71086-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71086-102">SYNOPSIS</span></span>
<span data-ttu-id="71086-103">Crea un'azione di recapito.</span><span class="sxs-lookup"><span data-stu-id="71086-103">Creates a delivery action.</span></span>

## <span data-ttu-id="71086-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71086-104">SYNTAX</span></span>

### <span data-ttu-id="71086-105">CacheExpirationActionParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71086-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71086-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="71086-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71086-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="71086-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71086-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71086-108">DESCRIPTION</span></span>
<span data-ttu-id="71086-109">Il cmdlet **New-AzCdnDeliveryRule** crea una regola di recapito per la creazione di endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="71086-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="71086-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71086-110">EXAMPLES</span></span>

### <span data-ttu-id="71086-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="71086-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="71086-112">Creare una semplice regola di recapito.</span><span class="sxs-lookup"><span data-stu-id="71086-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="71086-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71086-113">PARAMETERS</span></span>

### <span data-ttu-id="71086-114">-Azione</span><span class="sxs-lookup"><span data-stu-id="71086-114">-Action</span></span>
<span data-ttu-id="71086-115">Azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="71086-115">Action to perform.</span></span>

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

### <span data-ttu-id="71086-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="71086-116">-CacheBehavior</span></span>
<span data-ttu-id="71086-117">Comportamento di memorizzazione nella cache per l'azione</span><span class="sxs-lookup"><span data-stu-id="71086-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="71086-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="71086-118">-CacheDuration</span></span>
<span data-ttu-id="71086-119">La durata per cui il contenuto deve essere memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="71086-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="71086-120">Il formato consentito è \[ d. \] HH: mm: SS</span><span class="sxs-lookup"><span data-stu-id="71086-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="71086-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="71086-121">-CustomFragment</span></span>
<span data-ttu-id="71086-122">Frammento da aggiungere all'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="71086-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="71086-123">Fragment è la parte dell'URL che viene dopo #.</span><span class="sxs-lookup"><span data-stu-id="71086-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="71086-124">Non includere #.</span><span class="sxs-lookup"><span data-stu-id="71086-124">Do not include the #.</span></span>

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

### <span data-ttu-id="71086-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="71086-125">-CustomHostname</span></span>
<span data-ttu-id="71086-126">Host da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="71086-126">Host to redirect.</span></span>
<span data-ttu-id="71086-127">Lascia vuoto per usare l'host in arrivo come host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71086-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="71086-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="71086-128">-CustomPath</span></span>
<span data-ttu-id="71086-129">Il percorso completo da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="71086-129">The full path to redirect.</span></span>
<span data-ttu-id="71086-130">Il percorso non può essere vuoto e deve iniziare con/.</span><span class="sxs-lookup"><span data-stu-id="71086-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="71086-131">Lascia vuoto per usare il percorso in arrivo come percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71086-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="71086-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="71086-132">-CustomQueryString</span></span>
<span data-ttu-id="71086-133">Il set di stringhe di query da inserire nell'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="71086-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="71086-134">L'impostazione di questo valore sostituirebbe qualsiasi stringa di query esistente. lascia vuoto per mantenere la stringa di query in arrivo.</span><span class="sxs-lookup"><span data-stu-id="71086-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="71086-135">La stringa di query deve essere in \< \> = \< formato valore chiave \> .</span><span class="sxs-lookup"><span data-stu-id="71086-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="71086-136">?</span><span class="sxs-lookup"><span data-stu-id="71086-136">?</span></span> <span data-ttu-id="71086-137">e & verranno aggiunti automaticamente in modo da non includerli.</span><span class="sxs-lookup"><span data-stu-id="71086-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="71086-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71086-138">-DefaultProfile</span></span>
<span data-ttu-id="71086-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71086-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71086-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="71086-140">-DestinationProtocol</span></span>
<span data-ttu-id="71086-141">Protocollo da usare per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="71086-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="71086-142">Il valore predefinito è MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="71086-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="71086-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="71086-143">-HeaderActionType</span></span>
<span data-ttu-id="71086-144">Se modificare l'intestazione della richiesta o l'intestazione della risposta</span><span class="sxs-lookup"><span data-stu-id="71086-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="71086-145">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="71086-145">-HeaderName</span></span>
<span data-ttu-id="71086-146">Nome dell'intestazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="71086-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="71086-147">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="71086-147">-RedirectType</span></span>
<span data-ttu-id="71086-148">Il tipo di reindirizzamento che verrà usato dalla regola per reindirizzare il traffico</span><span class="sxs-lookup"><span data-stu-id="71086-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="71086-149">-Valore</span><span class="sxs-lookup"><span data-stu-id="71086-149">-Value</span></span>
<span data-ttu-id="71086-150">Valore per l'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="71086-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="71086-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71086-151">CommonParameters</span></span>
<span data-ttu-id="71086-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71086-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71086-153">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71086-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71086-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71086-154">INPUTS</span></span>

### <span data-ttu-id="71086-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="71086-155">None</span></span>

## <span data-ttu-id="71086-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71086-156">OUTPUTS</span></span>

### <span data-ttu-id="71086-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="71086-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="71086-158">Note</span><span class="sxs-lookup"><span data-stu-id="71086-158">NOTES</span></span>

## <span data-ttu-id="71086-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71086-159">RELATED LINKS</span></span>
