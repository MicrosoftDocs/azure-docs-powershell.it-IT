---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
ms.openlocfilehash: 5aff9382cbeac47c8d4423769d6256d34d5d109a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969070"
---
# <span data-ttu-id="bb920-101">Get-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="bb920-101">Get-AzFunctionAppSetting</span></span>

## <span data-ttu-id="bb920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb920-102">SYNOPSIS</span></span>
<span data-ttu-id="bb920-103">Recupera le impostazioni dell'app per un'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="bb920-103">Gets app settings for a function app.</span></span>

## <span data-ttu-id="bb920-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb920-104">SYNTAX</span></span>

### <span data-ttu-id="bb920-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb920-105">ByName (Default)</span></span>
```
Get-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb920-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="bb920-106">ByObjectInput</span></span>
```
Get-AzFunctionAppSetting -InputObject <ISite> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bb920-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb920-107">DESCRIPTION</span></span>
<span data-ttu-id="bb920-108">Recupera le impostazioni dell'app per un'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="bb920-108">Gets app settings for a function app.</span></span>

## <span data-ttu-id="bb920-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb920-109">EXAMPLES</span></span>

### <span data-ttu-id="bb920-110">Esempio 1: Ottenere le impostazioni dell'app di un'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="bb920-110">Example 1: Get the app settings of a function app.</span></span>
```powershell
PS C:\> Get-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="bb920-111">Questo comando ottiene le impostazioni dell'app di un'app per funzioni.</span><span class="sxs-lookup"><span data-stu-id="bb920-111">This command gets the app settings of a function app.</span></span>

## <span data-ttu-id="bb920-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb920-112">PARAMETERS</span></span>

### <span data-ttu-id="bb920-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb920-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb920-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb920-114">-InputObject</span></span>
<span data-ttu-id="bb920-115">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bb920-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb920-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bb920-116">-Name</span></span>
<span data-ttu-id="bb920-117">Nome dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="bb920-117">Name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb920-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb920-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb920-119">Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="bb920-119">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb920-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb920-120">-SubscriptionId</span></span>
<span data-ttu-id="bb920-121">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb920-121">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb920-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb920-122">-Confirm</span></span>
<span data-ttu-id="bb920-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb920-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb920-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb920-124">-WhatIf</span></span>
<span data-ttu-id="bb920-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb920-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb920-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb920-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb920-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb920-127">CommonParameters</span></span>
<span data-ttu-id="bb920-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb920-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb920-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb920-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb920-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb920-130">INPUTS</span></span>

### <span data-ttu-id="bb920-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="bb920-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="bb920-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb920-132">OUTPUTS</span></span>

### <span data-ttu-id="bb920-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="bb920-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="bb920-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb920-134">NOTES</span></span>

<span data-ttu-id="bb920-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bb920-135">ALIASES</span></span>

<span data-ttu-id="bb920-136">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="bb920-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb920-137">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bb920-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb920-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb920-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb920-139">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="bb920-139">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="bb920-140">`Location <String>`: Posizione risorsa.</span><span class="sxs-lookup"><span data-stu-id="bb920-140">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="bb920-141">`CloningInfoSourceWebAppId <String>`: ARM ID risorsa dell'app di origine.</span><span class="sxs-lookup"><span data-stu-id="bb920-141">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="bb920-142">L'ID risorsa app ha il formato /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} per gli slot di produzione e /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} per altri slot.</span><span class="sxs-lookup"><span data-stu-id="bb920-142">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="bb920-143">`[Kind <String>]`: tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="bb920-143">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="bb920-144">`[Tag <IResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="bb920-144">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="bb920-145">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb920-145">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bb920-146">`[ClientAffinityEnabled <Boolean?>]`: per abilitare l'affinità client, interrompere l'invio di cookie di affinità di sessione, che instradino le richieste client nella stessa sessione <code>true</code> <code>false</code> alla stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="bb920-146">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="bb920-147">L'impostazione predefinita è <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-147">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="bb920-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> per abilitare l'autenticazione del certificato client (autenticazione a comune TLS); in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="bb920-149">L'impostazione predefinita è <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-149">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="bb920-150">`[ClientCertExclusionPath <String>]`: percorsi di esclusione separati da virgola per l'autenticazione del certificato client</span><span class="sxs-lookup"><span data-stu-id="bb920-150">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="bb920-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: gli override delle impostazioni dell'applicazione per l'app clonata.</span><span class="sxs-lookup"><span data-stu-id="bb920-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="bb920-152">Se specificato, queste impostazioni sostituiscono le impostazioni clonate dall'app di origine.</span><span class="sxs-lookup"><span data-stu-id="bb920-152">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="bb920-153">In caso contrario, le impostazioni dell'app di origine vengono conservate.</span><span class="sxs-lookup"><span data-stu-id="bb920-153">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="bb920-154">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb920-154">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bb920-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> per clonare nomi host personalizzati dall'app di origine; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="bb920-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> per clonare il controllo del codice sorgente dall'app di origine; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="bb920-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> per configurare il bilanciamento del carico per l'app di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bb920-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="bb920-158">`[CloningInfoCorrelationId <String>]`: ID di correlazione dell'operazione di clonazione.</span><span class="sxs-lookup"><span data-stu-id="bb920-158">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="bb920-159">Questo ID consente di creare più operazioni di clonazione per usare lo stesso snapshot.</span><span class="sxs-lookup"><span data-stu-id="bb920-159">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="bb920-160">`[CloningInfoHostingEnvironment <String>]`: ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="bb920-160">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="bb920-161">`[CloningInfoOverwrite <Boolean?>]`: per <code>true</code> sovrascrivere l'app di destinazione; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-161">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="bb920-162">`[CloningInfoSourceWebAppLocation <String>]`: posizione dell'app di origine, ad esempio Stati Uniti occidentali o Europa del Nord</span><span class="sxs-lookup"><span data-stu-id="bb920-162">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="bb920-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ID risorsa del profilo di Gestione traffico da usare, se presente.</span><span class="sxs-lookup"><span data-stu-id="bb920-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="bb920-164">L'ID risorsa di Gestione traffico ha il formato /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="bb920-164">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="bb920-165">`[CloningInfoTrafficManagerProfileName <String>]`: nome del profilo di Gestione traffico da creare.</span><span class="sxs-lookup"><span data-stu-id="bb920-165">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="bb920-166">Questa operazione è necessaria solo se il profilo di Gestione traffico non esiste già.</span><span class="sxs-lookup"><span data-stu-id="bb920-166">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="bb920-167">`[Config <ISiteConfig>]`: configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="bb920-167">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="bb920-168">`IsPushEnabled <Boolean>`: ottiene o imposta un flag che indica se l'endpoint Push è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bb920-168">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="bb920-169">`[ActionMinProcessExecutionTime <String>]`: il tempo minimo necessario per l'esecuzione del processo prima di eseguire l'azione</span><span class="sxs-lookup"><span data-stu-id="bb920-169">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="bb920-170">`[ActionType <AutoHealActionType?>]`: azione predefinita da eseguire.</span><span class="sxs-lookup"><span data-stu-id="bb920-170">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="bb920-171">`[AlwaysOn <Boolean?>]`: <code>true</code> se l'opzione Sempre attivato è abilitata; in caso contrario. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="bb920-171">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-172">`[ApiDefinitionUrl <String>]`: URL della definizione dell'API.</span><span class="sxs-lookup"><span data-stu-id="bb920-172">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="bb920-173">`[ApiManagementConfigId <String>]`: APIM-Api identificatore.</span><span class="sxs-lookup"><span data-stu-id="bb920-173">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="bb920-174">`[AppCommandLine <String>]`: riga di comando dell'app per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="bb920-174">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="bb920-175">`[AppSetting <INameValuePair[]>]`: impostazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb920-175">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="bb920-176">`[Name <String>]`: per associare il nome.</span><span class="sxs-lookup"><span data-stu-id="bb920-176">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="bb920-177">`[Value <String>]`: per associare il valore.</span><span class="sxs-lookup"><span data-stu-id="bb920-177">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="bb920-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> se è abilitata l'opzione Correzione automatica; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-179">`[AutoSwapSlotName <String>]`: consente di scambiare automaticamente il nome dello slot.</span><span class="sxs-lookup"><span data-stu-id="bb920-179">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="bb920-180">`[ConnectionString <IConnStringInfo[]>]`: stringhe di connessione.</span><span class="sxs-lookup"><span data-stu-id="bb920-180">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="bb920-181">`[ConnectionString <String>]`: valore della stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="bb920-181">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="bb920-182">`[Name <String>]`: nome della stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="bb920-182">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="bb920-183">`[Type <ConnectionStringType?>]`: tipo di database.</span><span class="sxs-lookup"><span data-stu-id="bb920-183">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="bb920-184">`[CorAllowedOrigin <String[]>]`: ottiene o imposta l'elenco di origini che dovrebbe essere consentito per effettuare chiamate tra origini (ad esempio: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="bb920-184">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="bb920-185">Usare "\*" per consentire tutto.</span><span class="sxs-lookup"><span data-stu-id="bb920-185">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="bb920-186">`[CorSupportCredentials <Boolean?>]`: ottiene o imposta se le richieste CORS con credenziali sono consentite.</span><span class="sxs-lookup"><span data-stu-id="bb920-186">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="bb920-187">Per         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="bb920-187">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="bb920-188">`[CustomActionExe <String>]`: eseguibile da eseguire.</span><span class="sxs-lookup"><span data-stu-id="bb920-188">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="bb920-189">`[CustomActionParameter <String>]`: parametri per l'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="bb920-189">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="bb920-190">`[DefaultDocument <String[]>]`: documenti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="bb920-190">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="bb920-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se è abilitata la registrazione degli errori dettagliata; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-192">`[DocumentRoot <String>]`: radice del documento.</span><span class="sxs-lookup"><span data-stu-id="bb920-192">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="bb920-193">`[DynamicTagsJson <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag dinamici che verranno valutati dalle attestazioni degli utenti nell'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="bb920-193">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="bb920-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: elenco di regole di configurazione.</span><span class="sxs-lookup"><span data-stu-id="bb920-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="bb920-195">`[ActionHostName <String>]`: nome host di uno slot a cui verrà reindirizzato il traffico, se deciso.</span><span class="sxs-lookup"><span data-stu-id="bb920-195">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="bb920-196">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="bb920-196">E.g.</span></span> <span data-ttu-id="bb920-197">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="bb920-197">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="bb920-198">`[ChangeDecisionCallbackUrl <String>]`: nell'estensione del sito TiPGle è possibile specificare l'URL per l'algoritmo di decisione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bb920-198">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="bb920-199">Vedere l'estensione del sito TiPTip per l'ambito e i contratti.</span><span class="sxs-lookup"><span data-stu-id="bb920-199">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="bb920-200"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="bb920-200">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="bb920-201">`[ChangeIntervalInMinute <Int32?>]`: specifica l'intervallo in minuti per la valutazione di ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="bb920-201">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="bb920-202">`[ChangeStep <Double?>]`: nello scenario di avvio automatico questo è il passaggio da cui aggiungere/rimuovere fino a <code>ReroutePercentage</code> raggiungere \n <code>MinReroutePercentage</code> o         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-202">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="bb920-203">Le metriche del sito vengono controllate ogni N minuti specificati in .\nCustom decision algorithm può essere fornito nell'estensione del sito TiPTip, in cui è possibile <code>ChangeIntervalInMinutes</code> specificare l'URL. <code>ChangeDecisionCallbackUrl</code></span><span class="sxs-lookup"><span data-stu-id="bb920-203">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="bb920-204">`[MaxReroutePercentage <Double?>]`: specifica il limite superiore sotto il quale reroutePercentage rimarrà.</span><span class="sxs-lookup"><span data-stu-id="bb920-204">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="bb920-205">`[MinReroutePercentage <Double?>]`: specifica il limite inferiore al di sopra del quale resterà ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="bb920-205">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="bb920-206">`[Name <String>]`: nome della regola di routing.</span><span class="sxs-lookup"><span data-stu-id="bb920-206">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="bb920-207">Il nome consigliato deve puntare all'slot che riceverà il traffico nell'esperimento.</span><span class="sxs-lookup"><span data-stu-id="bb920-207">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="bb920-208">`[ReroutePercentage <Double?>]`: percentuale del traffico a cui verrà reindirizzato <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-208">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="bb920-209">`[FtpsState <FtpsState?>]`: stato del servizio FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="bb920-209">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="bb920-210">`[HandlerMapping <IHandlerMapping[]>]`: mapping del gestore.</span><span class="sxs-lookup"><span data-stu-id="bb920-210">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="bb920-211">`[Argument <String>]`: gli argomenti della riga di comando da passare al processore script.</span><span class="sxs-lookup"><span data-stu-id="bb920-211">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="bb920-212">`[Extension <String>]`: le richieste con questa estensione verranno gestite con l'applicazione FastCGI specificata.</span><span class="sxs-lookup"><span data-stu-id="bb920-212">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="bb920-213">`[ScriptProcessor <String>]`: il percorso assoluto dell'applicazione FastCGI.</span><span class="sxs-lookup"><span data-stu-id="bb920-213">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="bb920-214">`[HealthCheckPath <String>]`: percorso per la verifica dell'integrità</span><span class="sxs-lookup"><span data-stu-id="bb920-214">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="bb920-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: configura un sito Web per consentire ai client di connettersi tramite http2.0</span><span class="sxs-lookup"><span data-stu-id="bb920-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="bb920-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se è abilitata la registrazione HTTP; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: restrizioni di sicurezza IP per principale.</span><span class="sxs-lookup"><span data-stu-id="bb920-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="bb920-218">`[Action <String>]`: consente o nega l'accesso per l'intervallo IP.</span><span class="sxs-lookup"><span data-stu-id="bb920-218">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="bb920-219">`[Description <String>]`: descrizione della regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="bb920-219">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="bb920-220">`[IPAddress <String>]`: indirizzo IP per cui la restrizione di sicurezza è valida.</span><span class="sxs-lookup"><span data-stu-id="bb920-220">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="bb920-221">Può essere in forma di indirizzo ipv4 (proprietà SubnetMask obbligatoria) o notazione CIDR, ad esempio ipv4/mask (corrispondenza di bit iniziale).</span><span class="sxs-lookup"><span data-stu-id="bb920-221">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="bb920-222">Per ciDR, non è necessario specificare la proprietà SubnetMask.</span><span class="sxs-lookup"><span data-stu-id="bb920-222">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="bb920-223">`[Name <String>]`: nome della regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="bb920-223">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="bb920-224">`[Priority <Int32?>]`: priorità della regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="bb920-224">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="bb920-225">`[SubnetMask <String>]`: maschera di subnet per l'intervallo di indirizzi IP per cui la restrizione è valida.</span><span class="sxs-lookup"><span data-stu-id="bb920-225">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="bb920-226">`[SubnetTrafficTag <Int32?>]`: (interno) Tag di traffico subnet</span><span class="sxs-lookup"><span data-stu-id="bb920-226">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="bb920-227">`[Tag <IPFilterTag?>]`: definisce per cosa verrà usato questo filtro IP.</span><span class="sxs-lookup"><span data-stu-id="bb920-227">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="bb920-228">In questo modo vengono supportati i filtri IP nei proxy.</span><span class="sxs-lookup"><span data-stu-id="bb920-228">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="bb920-229">`[VnetSubnetResourceId <String>]`: ID risorsa di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="bb920-229">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="bb920-230">`[VnetTrafficTag <Int32?>]`: tag traffico Vnet (interno)</span><span class="sxs-lookup"><span data-stu-id="bb920-230">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="bb920-231">`[JavaContainer <String>]`: Java contenitore.</span><span class="sxs-lookup"><span data-stu-id="bb920-231">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="bb920-232">`[JavaContainerVersion <String>]`: Java versione del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bb920-232">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="bb920-233">`[JavaVersion <String>]`: Java versione.</span><span class="sxs-lookup"><span data-stu-id="bb920-233">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="bb920-234">`[LimitMaxDiskSizeInMb <Int64?>]`: utilizzo massimo consentito delle dimensioni del disco in MB.</span><span class="sxs-lookup"><span data-stu-id="bb920-234">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="bb920-235">`[LimitMaxMemoryInMb <Int64?>]`: utilizzo massimo della memoria consentito in MB.</span><span class="sxs-lookup"><span data-stu-id="bb920-235">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="bb920-236">`[LimitMaxPercentageCpu <Double?>]`: percentuale massima di utilizzo della CPU consentita.</span><span class="sxs-lookup"><span data-stu-id="bb920-236">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="bb920-237">`[LinuxFxVersion <String>]`: App Framework e versione Linux</span><span class="sxs-lookup"><span data-stu-id="bb920-237">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="bb920-238">`[LoadBalancing <SiteLoadBalancing?>]`: bilanciamento del carico del sito.</span><span class="sxs-lookup"><span data-stu-id="bb920-238">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="bb920-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> per abilitare MySQL locale; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-240">`[LogsDirectorySizeLimit <Int32?>]`: limite di dimensioni della directory dei log HTTP.</span><span class="sxs-lookup"><span data-stu-id="bb920-240">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="bb920-241">`[MachineKeyDecryption <String>]`: algoritmo usato per la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="bb920-241">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="bb920-242">`[MachineKeyDecryptionKey <String>]`: chiave di decrittografia.</span><span class="sxs-lookup"><span data-stu-id="bb920-242">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="bb920-243">`[MachineKeyValidation <String>]`: convalida MachineKey.</span><span class="sxs-lookup"><span data-stu-id="bb920-243">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="bb920-244">`[MachineKeyValidationKey <String>]`: codice di convalida.</span><span class="sxs-lookup"><span data-stu-id="bb920-244">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="bb920-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: modalità pipeline gestita.</span><span class="sxs-lookup"><span data-stu-id="bb920-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="bb920-246">`[ManagedServiceIdentityId <Int32?>]`: ID identità servizio gestito</span><span class="sxs-lookup"><span data-stu-id="bb920-246">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="bb920-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura la versione minima di TLS necessaria per le richieste SSL</span><span class="sxs-lookup"><span data-stu-id="bb920-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="bb920-248">`[NetFrameworkVersion <String>]`: .NET Framework versione.</span><span class="sxs-lookup"><span data-stu-id="bb920-248">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="bb920-249">`[NodeVersion <String>]`: versione di Node.js.</span><span class="sxs-lookup"><span data-stu-id="bb920-249">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="bb920-250">`[NumberOfWorker <Int32?>]`: numero di dipendenti.</span><span class="sxs-lookup"><span data-stu-id="bb920-250">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="bb920-251">`[PhpVersion <String>]`: versione di PHP.</span><span class="sxs-lookup"><span data-stu-id="bb920-251">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="bb920-252">`[PowerShellVersion <String>]`: versione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bb920-252">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="bb920-253">`[PreWarmedInstanceCount <Int32?>]`: numero di istanze preWarmed.</span><span class="sxs-lookup"><span data-stu-id="bb920-253">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="bb920-254">Questa impostazione si applica solo ai piani di consumo ed elastici</span><span class="sxs-lookup"><span data-stu-id="bb920-254">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="bb920-255">`[PublishingUsername <String>]`: nome utente di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="bb920-255">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="bb920-256">`[PushKind <String>]`: tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="bb920-256">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="bb920-257">`[PythonVersion <String>]`: versione di Python.</span><span class="sxs-lookup"><span data-stu-id="bb920-257">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="bb920-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se è abilitato il debug remoto; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-259">`[RemoteDebuggingVersion <String>]`: versione di debug remoto.</span><span class="sxs-lookup"><span data-stu-id="bb920-259">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="bb920-260">`[RequestCount <Int32?>]`: numero richieste.</span><span class="sxs-lookup"><span data-stu-id="bb920-260">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="bb920-261">`[RequestTimeInterval <String>]`: intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="bb920-261">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="bb920-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> se la traccia della richiesta è abilitata, in caso contrario <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-263">`[RequestTracingExpirationTime <DateTime?>]`: consente di richiedere la scadenza della traccia.</span><span class="sxs-lookup"><span data-stu-id="bb920-263">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="bb920-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: restrizioni di sicurezza IP per scm.</span><span class="sxs-lookup"><span data-stu-id="bb920-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="bb920-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: restrizioni di sicurezza IP per l'uso principale di scm.</span><span class="sxs-lookup"><span data-stu-id="bb920-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="bb920-266">`[ScmType <ScmType?>]`: tipo SCM.</span><span class="sxs-lookup"><span data-stu-id="bb920-266">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="bb920-267">`[SlowRequestCount <Int32?>]`: numero richieste.</span><span class="sxs-lookup"><span data-stu-id="bb920-267">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="bb920-268">`[SlowRequestTimeInterval <String>]`: intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="bb920-268">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="bb920-269">`[SlowRequestTimeTaken <String>]`: tempo impiegato.</span><span class="sxs-lookup"><span data-stu-id="bb920-269">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="bb920-270">`[TagWhitelistJson <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag che sono elencati per l'uso dall'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="bb920-270">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="bb920-271">`[TagsRequiringAuth <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag che richiedono l'autenticazione dell'utente da usare nell'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="bb920-271">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="bb920-272">I tag possono essere costituiti da caratteri alfanumerici e i seguenti: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="bb920-272">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="bb920-273">La convalida deve essere eseguita in PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="bb920-273">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="bb920-274">`[TracingOption <String>]`: per le opzioni di traccia.</span><span class="sxs-lookup"><span data-stu-id="bb920-274">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="bb920-275">`[TriggerPrivateBytesInKb <Int32?>]`: una regola basata su byte privati.</span><span class="sxs-lookup"><span data-stu-id="bb920-275">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="bb920-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: una regola basata sui codici di stato.</span><span class="sxs-lookup"><span data-stu-id="bb920-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="bb920-277">`[Count <Int32?>]`: numero richieste.</span><span class="sxs-lookup"><span data-stu-id="bb920-277">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="bb920-278">`[Status <Int32?>]`: codice di stato HTTP.</span><span class="sxs-lookup"><span data-stu-id="bb920-278">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="bb920-279">`[SubStatus <Int32?>]`: consente di richiedere lo stato secondario.</span><span class="sxs-lookup"><span data-stu-id="bb920-279">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="bb920-280">`[TimeInterval <String>]`: intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="bb920-280">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="bb920-281">`[Win32Status <Int32?>]`: codice di errore Win32.</span><span class="sxs-lookup"><span data-stu-id="bb920-281">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="bb920-282">`[Use32BitWorkerProcess <Boolean?>]`: per usare il processo di lavoro a <code>true</code> 32 bit; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-282">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-283">`[VirtualApplication <IVirtualApplication[]>]`: applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="bb920-283">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="bb920-284">`[PhysicalPath <String>]`: percorso fisico.</span><span class="sxs-lookup"><span data-stu-id="bb920-284">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="bb920-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> se il precaricamento è abilitato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="bb920-286">`[VirtualDirectory <IVirtualDirectory[]>]`: directory virtuali per l'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="bb920-286">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="bb920-287">`[PhysicalPath <String>]`: percorso fisico.</span><span class="sxs-lookup"><span data-stu-id="bb920-287">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="bb920-288">`[VirtualPath <String>]`: percorso dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="bb920-288">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="bb920-289">`[VirtualPath <String>]`: percorso virtuale.</span><span class="sxs-lookup"><span data-stu-id="bb920-289">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="bb920-290">`[VnetName <String>]`: nome rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bb920-290">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="bb920-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket è abilitato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="bb920-292">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span><span class="sxs-lookup"><span data-stu-id="bb920-292">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="bb920-293">`[XManagedServiceIdentityId <Int32?>]`: ID identità del servizio gestito esplicito</span><span class="sxs-lookup"><span data-stu-id="bb920-293">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="bb920-294">`[ContainerSize <Int32?>]`: dimensioni del contenitore di funzioni.</span><span class="sxs-lookup"><span data-stu-id="bb920-294">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="bb920-295">`[DailyMemoryTimeQuota <Int32?>]`: quota massima di tempo di memoria giornaliera consentita (applicabile solo alle app dinamiche).</span><span class="sxs-lookup"><span data-stu-id="bb920-295">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="bb920-296">`[Enabled <Boolean?>]`: <code>true</code> se l'app è abilitata; in caso contrario. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="bb920-296">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="bb920-297">Impostando questo valore su false, l'app viene disabilitata (l'app viene disconnessa).</span><span class="sxs-lookup"><span data-stu-id="bb920-297">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="bb920-298">`[HostNameSslState <IHostNameSslState[]>]`: gli stati SSL del nome host vengono usati per gestire le associazioni SSL per i nomi host dell'app.</span><span class="sxs-lookup"><span data-stu-id="bb920-298">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="bb920-299">`[HostType <HostType?>]`: indica se il nome host è uno standard o un nome host di archivio.</span><span class="sxs-lookup"><span data-stu-id="bb920-299">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="bb920-300">`[Name <String>]`: nome host.</span><span class="sxs-lookup"><span data-stu-id="bb920-300">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="bb920-301">`[SslState <SslState?>]`: tipo SSL.</span><span class="sxs-lookup"><span data-stu-id="bb920-301">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="bb920-302">`[Thumbprint <String>]`: impronta digitale del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="bb920-302">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="bb920-303">`[ToUpdate <Boolean?>]`: impostato su <code>true</code> per aggiornare il nome host esistente.</span><span class="sxs-lookup"><span data-stu-id="bb920-303">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="bb920-304">`[VirtualIP <String>]`: indirizzo IP virtuale assegnato al nome host se è abilitato SSL basato su IP.</span><span class="sxs-lookup"><span data-stu-id="bb920-304">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="bb920-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> per disabilitare i nomi host pubblici dell'app; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="bb920-306">Se <code>true</code> , l'app è accessibile solo tramite il processo di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="bb920-306">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="bb920-307">`[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="bb920-307">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="bb920-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: configura un sito Web in modo da accettare solo le richieste https.</span><span class="sxs-lookup"><span data-stu-id="bb920-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="bb920-309">Reindirizzamento dei problemi per le richieste http</span><span class="sxs-lookup"><span data-stu-id="bb920-309">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="bb920-310">`[HyperV <Boolean?>]`: sandbox Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="bb920-310">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="bb920-311">`[IdentityType <ManagedServiceIdentityType?>]`: tipo di identità del servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="bb920-311">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="bb920-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: elenco delle identità assegnate dall'utente associate alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="bb920-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="bb920-313">I riferimenti alle chiavi del dizionario di identità utente verranno ARM ID risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="bb920-313">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="bb920-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb920-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bb920-315">`[IsXenon <Boolean?>]`: Obsoleta: sandbox Di Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="bb920-315">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="bb920-316">`[RedundancyMode <RedundancyMode?>]`: modalità di ridondanza del sito</span><span class="sxs-lookup"><span data-stu-id="bb920-316">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="bb920-317">`[Reserved <Boolean?>]`: <code>true</code> se riservato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-317">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="bb920-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> per interrompere il sito di SCM (KUDU) quando l'app viene interrotta; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="bb920-319">L'impostazione predefinita è <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="bb920-319">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="bb920-320">`[ServerFarmId <String>]`: ID risorsa del piano di servizio app associato, formattato come: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="bb920-320">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="bb920-321">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb920-321">RELATED LINKS</span></span>

