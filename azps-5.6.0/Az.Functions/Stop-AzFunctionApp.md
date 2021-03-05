---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/stop-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Stop-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Stop-AzFunctionApp.md
ms.openlocfilehash: 2b8717c3387bd8e8ac6cd0fe1cdd37f957c176ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972845"
---
# <span data-ttu-id="e0b76-101">Stop-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="e0b76-101">Stop-AzFunctionApp</span></span>

## <span data-ttu-id="e0b76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0b76-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b76-103">Interrompe un'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="e0b76-103">Stops a function app.</span></span>

## <span data-ttu-id="e0b76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0b76-104">SYNTAX</span></span>

### <span data-ttu-id="e0b76-105">StopByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0b76-105">StopByName (Default)</span></span>
```
Stop-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0b76-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="e0b76-106">ByObjectInput</span></span>
```
Stop-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e0b76-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e0b76-107">DESCRIPTION</span></span>
<span data-ttu-id="e0b76-108">Interrompe un'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="e0b76-108">Stops a function app.</span></span>

## <span data-ttu-id="e0b76-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0b76-109">EXAMPLES</span></span>

### <span data-ttu-id="e0b76-110">Esempio 1: Ottenere un'app per le funzioni in base al nome e arrestarla.</span><span class="sxs-lookup"><span data-stu-id="e0b76-110">Example 1: Get a function app by name and stop it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Stop-AzFunctionApp -Force
```

<span data-ttu-id="e0b76-111">Questo comando recupera un'app per funzione in base al nome e la interrompe.</span><span class="sxs-lookup"><span data-stu-id="e0b76-111">This command gets a function app by name and stops it.</span></span>

### <span data-ttu-id="e0b76-112">Esempio 2: Arrestare un'app per funzioni in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e0b76-112">Example 2: Stop a function app by name.</span></span>
```powershell
PS C:\> Stop-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="e0b76-113">Questo comando interrompe l'esecuzione di un'app per funzione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e0b76-113">This command stops a function app by name.</span></span>

## <span data-ttu-id="e0b76-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0b76-114">PARAMETERS</span></span>

### <span data-ttu-id="e0b76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b76-115">-DefaultProfile</span></span>
<span data-ttu-id="e0b76-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b76-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e0b76-117">-Force</span></span>
<span data-ttu-id="e0b76-118">Forza il cmdlet ad arrestare l'app funzione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e0b76-118">Forces the cmdlet to stop the function app without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b76-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0b76-119">-InputObject</span></span>
<span data-ttu-id="e0b76-120">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e0b76-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0b76-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e0b76-121">-Name</span></span>
<span data-ttu-id="e0b76-122">Nome dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="e0b76-122">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b76-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0b76-123">-PassThru</span></span>
<span data-ttu-id="e0b76-124">Restituisce true quando il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e0b76-124">Returns true when the command succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b76-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b76-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b76-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0b76-126">-SubscriptionId</span></span>
<span data-ttu-id="e0b76-127">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b76-127">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b76-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0b76-128">-Confirm</span></span>
<span data-ttu-id="e0b76-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0b76-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b76-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b76-130">-WhatIf</span></span>
<span data-ttu-id="e0b76-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0b76-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b76-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0b76-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b76-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b76-133">CommonParameters</span></span>
<span data-ttu-id="e0b76-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b76-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b76-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e0b76-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b76-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="e0b76-136">INPUTS</span></span>

### <span data-ttu-id="e0b76-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="e0b76-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="e0b76-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0b76-138">OUTPUTS</span></span>

### <span data-ttu-id="e0b76-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0b76-139">System.Boolean</span></span>

## <span data-ttu-id="e0b76-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="e0b76-140">NOTES</span></span>

<span data-ttu-id="e0b76-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e0b76-141">ALIASES</span></span>

<span data-ttu-id="e0b76-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e0b76-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0b76-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e0b76-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0b76-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0b76-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0b76-145">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="e0b76-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="e0b76-146">`Location <String>`: Posizione risorsa.</span><span class="sxs-lookup"><span data-stu-id="e0b76-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="e0b76-147">`CloningInfoSourceWebAppId <String>`: ARM ID risorsa dell'app di origine.</span><span class="sxs-lookup"><span data-stu-id="e0b76-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="e0b76-148">L'ID risorsa app ha il formato /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} per gli slot di produzione e /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} per altri slot.</span><span class="sxs-lookup"><span data-stu-id="e0b76-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="e0b76-149">`[Kind <String>]`: tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e0b76-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="e0b76-150">`[Tag <IResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e0b76-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="e0b76-151">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0b76-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e0b76-152">`[ClientAffinityEnabled <Boolean?>]`: per abilitare l'affinità client, interrompere l'invio di cookie di affinità di sessione, che instradino le richieste client nella stessa sessione <code>true</code> <code>false</code> alla stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="e0b76-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="e0b76-153">L'impostazione predefinita è <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="e0b76-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> per abilitare l'autenticazione del certificato client (autenticazione a comune TLS); in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="e0b76-155">L'impostazione predefinita è <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="e0b76-156">`[ClientCertExclusionPath <String>]`: percorsi di esclusione separati da virgola per l'autenticazione del certificato client</span><span class="sxs-lookup"><span data-stu-id="e0b76-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="e0b76-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: gli override delle impostazioni dell'applicazione per l'app clonata.</span><span class="sxs-lookup"><span data-stu-id="e0b76-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="e0b76-158">Se specificato, queste impostazioni sostituiscono le impostazioni clonate dall'app di origine.</span><span class="sxs-lookup"><span data-stu-id="e0b76-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="e0b76-159">In caso contrario, le impostazioni dell'app di origine vengono mantenute.</span><span class="sxs-lookup"><span data-stu-id="e0b76-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="e0b76-160">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0b76-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e0b76-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> per clonare nomi host personalizzati dall'app di origine; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e0b76-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> per clonare il controllo del codice sorgente dall'app di origine; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e0b76-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> per configurare il bilanciamento del carico per l'app di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="e0b76-164">`[CloningInfoCorrelationId <String>]`: ID di correlazione dell'operazione di clonazione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="e0b76-165">Questo ID consente di creare più operazioni di clonazione per usare lo stesso snapshot.</span><span class="sxs-lookup"><span data-stu-id="e0b76-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="e0b76-166">`[CloningInfoHostingEnvironment <String>]`: ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="e0b76-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="e0b76-167">`[CloningInfoOverwrite <Boolean?>]`: per <code>true</code> sovrascrivere l'app di destinazione; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e0b76-168">`[CloningInfoSourceWebAppLocation <String>]`: posizione dell'app di origine, ad esempio Stati Uniti occidentali o Europa del Nord</span><span class="sxs-lookup"><span data-stu-id="e0b76-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="e0b76-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ID risorsa del profilo di Gestione traffico da usare, se presente.</span><span class="sxs-lookup"><span data-stu-id="e0b76-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="e0b76-170">L'ID risorsa di Gestione traffico ha il formato /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="e0b76-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="e0b76-171">`[CloningInfoTrafficManagerProfileName <String>]`: nome del profilo di Gestione traffico da creare.</span><span class="sxs-lookup"><span data-stu-id="e0b76-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="e0b76-172">Questa operazione è necessaria solo se il profilo di Gestione traffico non esiste già.</span><span class="sxs-lookup"><span data-stu-id="e0b76-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="e0b76-173">`[Config <ISiteConfig>]`: configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="e0b76-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="e0b76-174">`IsPushEnabled <Boolean>`: ottiene o imposta un flag che indica se l'endpoint Push è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e0b76-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="e0b76-175">`[ActionMinProcessExecutionTime <String>]`: il tempo minimo necessario per l'esecuzione del processo prima di eseguire l'azione</span><span class="sxs-lookup"><span data-stu-id="e0b76-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="e0b76-176">`[ActionType <AutoHealActionType?>]`: azione predefinita da eseguire.</span><span class="sxs-lookup"><span data-stu-id="e0b76-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="e0b76-177">`[AlwaysOn <Boolean?>]`: <code>true</code> se l'opzione Sempre attivato è abilitata; in caso contrario. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e0b76-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-178">`[ApiDefinitionUrl <String>]`: URL della definizione dell'API.</span><span class="sxs-lookup"><span data-stu-id="e0b76-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="e0b76-179">`[ApiManagementConfigId <String>]`: APIM-Api identificatore.</span><span class="sxs-lookup"><span data-stu-id="e0b76-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="e0b76-180">`[AppCommandLine <String>]`: riga di comando dell'app da avviare.</span><span class="sxs-lookup"><span data-stu-id="e0b76-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="e0b76-181">`[AppSetting <INameValuePair[]>]`: impostazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="e0b76-182">`[Name <String>]`: per associare il nome.</span><span class="sxs-lookup"><span data-stu-id="e0b76-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="e0b76-183">`[Value <String>]`: per associare il valore.</span><span class="sxs-lookup"><span data-stu-id="e0b76-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="e0b76-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> se è abilitata l'opzione Correzione automatica; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-185">`[AutoSwapSlotName <String>]`: consente di scambiare automaticamente il nome dello slot.</span><span class="sxs-lookup"><span data-stu-id="e0b76-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="e0b76-186">`[ConnectionString <IConnStringInfo[]>]`: stringhe di connessione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="e0b76-187">`[ConnectionString <String>]`: valore della stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="e0b76-188">`[Name <String>]`: nome della stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="e0b76-189">`[Type <ConnectionStringType?>]`: tipo di database.</span><span class="sxs-lookup"><span data-stu-id="e0b76-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="e0b76-190">`[CorAllowedOrigin <String[]>]`: ottiene o imposta l'elenco di origini che dovrebbe essere consentito per effettuare chiamate tra origini (ad esempio: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="e0b76-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="e0b76-191">Usare "\*" per consentire tutto.</span><span class="sxs-lookup"><span data-stu-id="e0b76-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="e0b76-192">`[CorSupportCredentials <Boolean?>]`: ottiene o imposta se le richieste CORS con credenziali sono consentite.</span><span class="sxs-lookup"><span data-stu-id="e0b76-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="e0b76-193">Per         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="e0b76-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="e0b76-194">`[CustomActionExe <String>]`: eseguibile da eseguire.</span><span class="sxs-lookup"><span data-stu-id="e0b76-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="e0b76-195">`[CustomActionParameter <String>]`: parametri per l'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="e0b76-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="e0b76-196">`[DefaultDocument <String[]>]`: documenti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="e0b76-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="e0b76-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se è abilitata la registrazione degli errori dettagliata; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-198">`[DocumentRoot <String>]`: radice del documento.</span><span class="sxs-lookup"><span data-stu-id="e0b76-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="e0b76-199">`[DynamicTagsJson <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag dinamici che verranno valutati dalle attestazioni degli utenti nell'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="e0b76-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="e0b76-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: elenco di regole di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="e0b76-201">`[ActionHostName <String>]`: nome host di uno slot a cui verrà reindirizzato il traffico, se deciso.</span><span class="sxs-lookup"><span data-stu-id="e0b76-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="e0b76-202">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="e0b76-202">E.g.</span></span> <span data-ttu-id="e0b76-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="e0b76-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="e0b76-204">`[ChangeDecisionCallbackUrl <String>]`: nell'estensione del sito TiPGle è possibile specificare l'URL per l'algoritmo di decisione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e0b76-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="e0b76-205">Vedere l'estensione del sito TiPTip per l'ambito e i contratti.</span><span class="sxs-lookup"><span data-stu-id="e0b76-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="e0b76-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="e0b76-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="e0b76-207">`[ChangeIntervalInMinute <Int32?>]`: specifica l'intervallo in minuti per la valutazione di ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="e0b76-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="e0b76-208">`[ChangeStep <Double?>]`: nello scenario di avvio automatico questo è il passaggio da cui aggiungere/rimuovere fino a <code>ReroutePercentage</code> raggiungere \n <code>MinReroutePercentage</code> o         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="e0b76-209">Le metriche del sito vengono controllate ogni N minuti specificati in .\nCustom decision algorithm può essere fornito nell'estensione del sito TiPTip, in cui è possibile <code>ChangeIntervalInMinutes</code> specificare l'URL. <code>ChangeDecisionCallbackUrl</code></span><span class="sxs-lookup"><span data-stu-id="e0b76-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="e0b76-210">`[MaxReroutePercentage <Double?>]`: specifica il limite superiore sotto il quale reroutePercentage rimarrà.</span><span class="sxs-lookup"><span data-stu-id="e0b76-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="e0b76-211">`[MinReroutePercentage <Double?>]`: specifica il limite inferiore al di sopra del quale resterà ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="e0b76-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="e0b76-212">`[Name <String>]`: nome della regola di routing.</span><span class="sxs-lookup"><span data-stu-id="e0b76-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="e0b76-213">Il nome consigliato deve puntare all'slot che riceverà il traffico nell'esperimento.</span><span class="sxs-lookup"><span data-stu-id="e0b76-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="e0b76-214">`[ReroutePercentage <Double?>]`: percentuale del traffico a cui verrà reindirizzato <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="e0b76-215">`[FtpsState <FtpsState?>]`: stato del servizio FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="e0b76-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="e0b76-216">`[HandlerMapping <IHandlerMapping[]>]`: mapping del gestore.</span><span class="sxs-lookup"><span data-stu-id="e0b76-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="e0b76-217">`[Argument <String>]`: gli argomenti della riga di comando da passare al processore script.</span><span class="sxs-lookup"><span data-stu-id="e0b76-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="e0b76-218">`[Extension <String>]`: le richieste con questa estensione verranno gestite con l'applicazione FastCGI specificata.</span><span class="sxs-lookup"><span data-stu-id="e0b76-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="e0b76-219">`[ScriptProcessor <String>]`: il percorso assoluto dell'applicazione FastCGI.</span><span class="sxs-lookup"><span data-stu-id="e0b76-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="e0b76-220">`[HealthCheckPath <String>]`: percorso per la verifica dell'integrità</span><span class="sxs-lookup"><span data-stu-id="e0b76-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="e0b76-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configura un sito Web per consentire ai client di connettersi tramite http2.0</span><span class="sxs-lookup"><span data-stu-id="e0b76-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="e0b76-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se è abilitata la registrazione HTTP; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: restrizioni di sicurezza IP per principale.</span><span class="sxs-lookup"><span data-stu-id="e0b76-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="e0b76-224">`[Action <String>]`: consente o nega l'accesso per l'intervallo IP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="e0b76-225">`[Description <String>]`: descrizione della regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="e0b76-226">`[IPAddress <String>]`: indirizzo IP per cui la restrizione di sicurezza è valida.</span><span class="sxs-lookup"><span data-stu-id="e0b76-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="e0b76-227">Può essere in forma di indirizzo ipv4 (proprietà SubnetMask obbligatoria) o notazione CIDR, ad esempio ipv4/mask (corrispondenza di bit iniziale).</span><span class="sxs-lookup"><span data-stu-id="e0b76-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="e0b76-228">Per ciDR, non è necessario specificare la proprietà SubnetMask.</span><span class="sxs-lookup"><span data-stu-id="e0b76-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="e0b76-229">`[Name <String>]`: nome della regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="e0b76-230">`[Priority <Int32?>]`: priorità della regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="e0b76-231">`[SubnetMask <String>]`: maschera di subnet per l'intervallo di indirizzi IP per cui la restrizione è valida.</span><span class="sxs-lookup"><span data-stu-id="e0b76-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="e0b76-232">`[SubnetTrafficTag <Int32?>]`: (interno) Tag di traffico subnet</span><span class="sxs-lookup"><span data-stu-id="e0b76-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="e0b76-233">`[Tag <IPFilterTag?>]`: definisce per cosa verrà usato questo filtro IP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="e0b76-234">In questo modo vengono supportati i filtri IP nei proxy.</span><span class="sxs-lookup"><span data-stu-id="e0b76-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="e0b76-235">`[VnetSubnetResourceId <String>]`: ID risorsa di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e0b76-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="e0b76-236">`[VnetTrafficTag <Int32?>]`: tag traffico Vnet (interno)</span><span class="sxs-lookup"><span data-stu-id="e0b76-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="e0b76-237">`[JavaContainer <String>]`: Java contenitore.</span><span class="sxs-lookup"><span data-stu-id="e0b76-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="e0b76-238">`[JavaContainerVersion <String>]`: Java versione del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e0b76-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="e0b76-239">`[JavaVersion <String>]`: Java versione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="e0b76-240">`[LimitMaxDiskSizeInMb <Int64?>]`: utilizzo massimo consentito delle dimensioni del disco in MB.</span><span class="sxs-lookup"><span data-stu-id="e0b76-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="e0b76-241">`[LimitMaxMemoryInMb <Int64?>]`: utilizzo massimo della memoria consentito in MB.</span><span class="sxs-lookup"><span data-stu-id="e0b76-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="e0b76-242">`[LimitMaxPercentageCpu <Double?>]`: percentuale massima di utilizzo della CPU consentita.</span><span class="sxs-lookup"><span data-stu-id="e0b76-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="e0b76-243">`[LinuxFxVersion <String>]`: App Framework Linux e versione</span><span class="sxs-lookup"><span data-stu-id="e0b76-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="e0b76-244">`[LoadBalancing <SiteLoadBalancing?>]`: bilanciamento del carico del sito.</span><span class="sxs-lookup"><span data-stu-id="e0b76-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="e0b76-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> per abilitare MySQL locale; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-246">`[LogsDirectorySizeLimit <Int32?>]`: limite di dimensioni della directory dei log HTTP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="e0b76-247">`[MachineKeyDecryption <String>]`: algoritmo usato per la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="e0b76-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="e0b76-248">`[MachineKeyDecryptionKey <String>]`: chiave di decrittografia.</span><span class="sxs-lookup"><span data-stu-id="e0b76-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="e0b76-249">`[MachineKeyValidation <String>]`: convalida MachineKey.</span><span class="sxs-lookup"><span data-stu-id="e0b76-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="e0b76-250">`[MachineKeyValidationKey <String>]`: codice di convalida.</span><span class="sxs-lookup"><span data-stu-id="e0b76-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="e0b76-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: modalità pipeline gestita.</span><span class="sxs-lookup"><span data-stu-id="e0b76-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="e0b76-252">`[ManagedServiceIdentityId <Int32?>]`: ID identità servizio gestito</span><span class="sxs-lookup"><span data-stu-id="e0b76-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="e0b76-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura la versione minima di TLS necessaria per le richieste SSL</span><span class="sxs-lookup"><span data-stu-id="e0b76-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="e0b76-254">`[NetFrameworkVersion <String>]`: .NET Framework versione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="e0b76-255">`[NodeVersion <String>]`: versione di Node.js.</span><span class="sxs-lookup"><span data-stu-id="e0b76-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="e0b76-256">`[NumberOfWorker <Int32?>]`: numero di dipendenti.</span><span class="sxs-lookup"><span data-stu-id="e0b76-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="e0b76-257">`[PhpVersion <String>]`: versione di PHP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="e0b76-258">`[PowerShellVersion <String>]`: versione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0b76-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="e0b76-259">`[PreWarmedInstanceCount <Int32?>]`: numero di istanze preWarmed.</span><span class="sxs-lookup"><span data-stu-id="e0b76-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="e0b76-260">Questa impostazione si applica solo ai piani di consumo ed elastici</span><span class="sxs-lookup"><span data-stu-id="e0b76-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="e0b76-261">`[PublishingUsername <String>]`: nome utente di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e0b76-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="e0b76-262">`[PushKind <String>]`: tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e0b76-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="e0b76-263">`[PythonVersion <String>]`: versione di Python.</span><span class="sxs-lookup"><span data-stu-id="e0b76-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="e0b76-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se è abilitato il debug remoto; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-265">`[RemoteDebuggingVersion <String>]`: versione di debug remoto.</span><span class="sxs-lookup"><span data-stu-id="e0b76-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="e0b76-266">`[RequestCount <Int32?>]`: numero richieste.</span><span class="sxs-lookup"><span data-stu-id="e0b76-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="e0b76-267">`[RequestTimeInterval <String>]`: intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="e0b76-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="e0b76-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> se la traccia della richiesta è abilitata, in caso contrario <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-269">`[RequestTracingExpirationTime <DateTime?>]`: consente di richiedere la scadenza della traccia.</span><span class="sxs-lookup"><span data-stu-id="e0b76-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="e0b76-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: restrizioni di sicurezza IP per scm.</span><span class="sxs-lookup"><span data-stu-id="e0b76-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="e0b76-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: restrizioni di sicurezza IP per l'uso principale di scm.</span><span class="sxs-lookup"><span data-stu-id="e0b76-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="e0b76-272">`[ScmType <ScmType?>]`: tipo SCM.</span><span class="sxs-lookup"><span data-stu-id="e0b76-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="e0b76-273">`[SlowRequestCount <Int32?>]`: numero richieste.</span><span class="sxs-lookup"><span data-stu-id="e0b76-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="e0b76-274">`[SlowRequestTimeInterval <String>]`: intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="e0b76-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="e0b76-275">`[SlowRequestTimeTaken <String>]`: tempo impiegato.</span><span class="sxs-lookup"><span data-stu-id="e0b76-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="e0b76-276">`[TagWhitelistJson <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag che sono elencati per l'uso dall'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="e0b76-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="e0b76-277">`[TagsRequiringAuth <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag che richiedono l'autenticazione dell'utente da usare nell'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="e0b76-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="e0b76-278">I tag possono essere costituiti da caratteri alfanumerici e i seguenti: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="e0b76-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="e0b76-279">La convalida deve essere eseguita in PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="e0b76-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="e0b76-280">`[TracingOption <String>]`: per le opzioni di traccia.</span><span class="sxs-lookup"><span data-stu-id="e0b76-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="e0b76-281">`[TriggerPrivateBytesInKb <Int32?>]`: una regola basata su byte privati.</span><span class="sxs-lookup"><span data-stu-id="e0b76-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="e0b76-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: una regola basata sui codici di stato.</span><span class="sxs-lookup"><span data-stu-id="e0b76-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="e0b76-283">`[Count <Int32?>]`: numero richieste.</span><span class="sxs-lookup"><span data-stu-id="e0b76-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="e0b76-284">`[Status <Int32?>]`: codice di stato HTTP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="e0b76-285">`[SubStatus <Int32?>]`: consente di richiedere lo stato secondario.</span><span class="sxs-lookup"><span data-stu-id="e0b76-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="e0b76-286">`[TimeInterval <String>]`: intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="e0b76-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="e0b76-287">`[Win32Status <Int32?>]`: codice di errore Win32.</span><span class="sxs-lookup"><span data-stu-id="e0b76-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="e0b76-288">`[Use32BitWorkerProcess <Boolean?>]`: per usare il processo di lavoro a <code>true</code> 32 bit; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-289">`[VirtualApplication <IVirtualApplication[]>]`: applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="e0b76-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="e0b76-290">`[PhysicalPath <String>]`: percorso fisico.</span><span class="sxs-lookup"><span data-stu-id="e0b76-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="e0b76-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> se il precaricamento è abilitato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="e0b76-292">`[VirtualDirectory <IVirtualDirectory[]>]`: directory virtuali per l'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0b76-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="e0b76-293">`[PhysicalPath <String>]`: percorso fisico.</span><span class="sxs-lookup"><span data-stu-id="e0b76-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="e0b76-294">`[VirtualPath <String>]`: percorso dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0b76-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="e0b76-295">`[VirtualPath <String>]`: percorso virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0b76-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="e0b76-296">`[VnetName <String>]`: nome rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0b76-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="e0b76-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket è abilitato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e0b76-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span><span class="sxs-lookup"><span data-stu-id="e0b76-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="e0b76-299">`[XManagedServiceIdentityId <Int32?>]`: ID identità del servizio gestito esplicito</span><span class="sxs-lookup"><span data-stu-id="e0b76-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="e0b76-300">`[ContainerSize <Int32?>]`: dimensioni del contenitore di funzioni.</span><span class="sxs-lookup"><span data-stu-id="e0b76-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="e0b76-301">`[DailyMemoryTimeQuota <Int32?>]`: quota massima di tempo di memoria giornaliera consentita (applicabile solo alle app dinamiche).</span><span class="sxs-lookup"><span data-stu-id="e0b76-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="e0b76-302">`[Enabled <Boolean?>]`: <code>true</code> se l'app è abilitata; in caso contrario. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e0b76-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="e0b76-303">Impostando questo valore su false, l'app viene disabilitata (l'app viene disconnessa).</span><span class="sxs-lookup"><span data-stu-id="e0b76-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="e0b76-304">`[HostNameSslState <IHostNameSslState[]>]`: gli stati SSL del nome host vengono usati per gestire le associazioni SSL per i nomi host dell'app.</span><span class="sxs-lookup"><span data-stu-id="e0b76-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="e0b76-305">`[HostType <HostType?>]`: indica se il nome host è uno standard o un nome host di archivio.</span><span class="sxs-lookup"><span data-stu-id="e0b76-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="e0b76-306">`[Name <String>]`: nome host.</span><span class="sxs-lookup"><span data-stu-id="e0b76-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="e0b76-307">`[SslState <SslState?>]`: tipo SSL.</span><span class="sxs-lookup"><span data-stu-id="e0b76-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="e0b76-308">`[Thumbprint <String>]`: impronta digitale del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="e0b76-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="e0b76-309">`[ToUpdate <Boolean?>]`: impostato su <code>true</code> per aggiornare il nome host esistente.</span><span class="sxs-lookup"><span data-stu-id="e0b76-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="e0b76-310">`[VirtualIP <String>]`: indirizzo IP virtuale assegnato al nome host se è abilitato SSL basato su IP.</span><span class="sxs-lookup"><span data-stu-id="e0b76-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="e0b76-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> per disabilitare i nomi host pubblici dell'app; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="e0b76-312">Se <code>true</code> , l'app è accessibile solo tramite il processo di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="e0b76-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="e0b76-313">`[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="e0b76-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="e0b76-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configura un sito Web in modo da accettare solo le richieste https.</span><span class="sxs-lookup"><span data-stu-id="e0b76-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="e0b76-315">Reindirizzamento dei problemi per le richieste http</span><span class="sxs-lookup"><span data-stu-id="e0b76-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="e0b76-316">`[HyperV <Boolean?>]`: sandbox Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e0b76-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="e0b76-317">`[IdentityType <ManagedServiceIdentityType?>]`: tipo di identità del servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="e0b76-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="e0b76-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: elenco delle identità assegnate dall'utente associate alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="e0b76-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="e0b76-319">I riferimenti alle chiavi del dizionario di identità utente verranno ARM ID risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="e0b76-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="e0b76-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0b76-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e0b76-321">`[IsXenon <Boolean?>]`: Obsoleta: sandbox Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e0b76-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="e0b76-322">`[RedundancyMode <RedundancyMode?>]`: modalità di ridondanza del sito</span><span class="sxs-lookup"><span data-stu-id="e0b76-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="e0b76-323">`[Reserved <Boolean?>]`: <code>true</code> se riservato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e0b76-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> per interrompere il sito di SCM (KUDU) quando l'app viene interrotta; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="e0b76-325">L'impostazione predefinita è <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e0b76-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="e0b76-326">`[ServerFarmId <String>]`: ID risorsa del piano di servizio app associato, formattato come: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="e0b76-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="e0b76-327">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0b76-327">RELATED LINKS</span></span>

