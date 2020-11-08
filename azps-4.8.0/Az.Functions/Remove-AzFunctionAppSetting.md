---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: abfa704b042b0a8cd25b8682e3b93306b5ca6277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192476"
---
# <span data-ttu-id="35dfb-101">Remove-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="35dfb-101">Remove-AzFunctionAppSetting</span></span>

## <span data-ttu-id="35dfb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="35dfb-103">Rimuove le impostazioni dell'app da un'app di funzione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-103">Removes app settings from a function app.</span></span>

## <span data-ttu-id="35dfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35dfb-104">SYNTAX</span></span>

### <span data-ttu-id="35dfb-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35dfb-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35dfb-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="35dfb-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35dfb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35dfb-107">DESCRIPTION</span></span>
<span data-ttu-id="35dfb-108">Rimuove le impostazioni dell'app da un'app di funzione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-108">Removes app settings from a function app.</span></span>

## <span data-ttu-id="35dfb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35dfb-109">EXAMPLES</span></span>

### <span data-ttu-id="35dfb-110">Esempio 1: rimuovere le impostazioni dell'app in un'app di funzione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-110">Example 1: Remove app settings in a function app.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

<span data-ttu-id="35dfb-111">Questo comando rimuove le impostazioni dell'app in un'app di funzione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-111">This command removes app settings in a function app.</span></span>

## <span data-ttu-id="35dfb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35dfb-112">PARAMETERS</span></span>

### <span data-ttu-id="35dfb-113">-AppSettingName</span><span class="sxs-lookup"><span data-stu-id="35dfb-113">-AppSettingName</span></span>
<span data-ttu-id="35dfb-114">Elenco delle impostazioni dell'app funzione da rimuovere dall'App funzione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-114">List of function app settings to be removed from the function app.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35dfb-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="35dfb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="35dfb-116">-Force</span></span>
<span data-ttu-id="35dfb-117">Impone al cmdlet di rimuovere l'impostazione dell'app funzione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="35dfb-117">Forces the cmdlet to remove function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="35dfb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35dfb-118">-InputObject</span></span>
<span data-ttu-id="35dfb-119">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="35dfb-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35dfb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="35dfb-120">-Name</span></span>
<span data-ttu-id="35dfb-121">Nome dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-121">Name of the function app.</span></span>

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

### <span data-ttu-id="35dfb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35dfb-122">-ResourceGroupName</span></span>
<span data-ttu-id="35dfb-123">Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="35dfb-123">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="35dfb-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35dfb-124">-SubscriptionId</span></span>
<span data-ttu-id="35dfb-125">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="35dfb-125">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dfb-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35dfb-126">-Confirm</span></span>
<span data-ttu-id="35dfb-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35dfb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35dfb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35dfb-128">-WhatIf</span></span>
<span data-ttu-id="35dfb-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35dfb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35dfb-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35dfb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35dfb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dfb-131">CommonParameters</span></span>
<span data-ttu-id="35dfb-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dfb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dfb-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35dfb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dfb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35dfb-134">INPUTS</span></span>

### <span data-ttu-id="35dfb-135">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="35dfb-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="35dfb-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35dfb-136">OUTPUTS</span></span>

### <span data-ttu-id="35dfb-137">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="35dfb-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="35dfb-138">Note</span><span class="sxs-lookup"><span data-stu-id="35dfb-138">NOTES</span></span>

<span data-ttu-id="35dfb-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="35dfb-139">ALIASES</span></span>

<span data-ttu-id="35dfb-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35dfb-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35dfb-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="35dfb-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35dfb-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35dfb-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35dfb-143">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="35dfb-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="35dfb-144">`Location <String>`: Percorso delle risorse.</span><span class="sxs-lookup"><span data-stu-id="35dfb-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="35dfb-145">`CloningInfoSourceWebAppId <String>`: ID risorsa ARM dell'app di origine.</span><span class="sxs-lookup"><span data-stu-id="35dfb-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="35dfb-146">ID risorsa dell'app è il formato/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} per gli slot di produzione e/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} per altri slot.</span><span class="sxs-lookup"><span data-stu-id="35dfb-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="35dfb-147">`[Kind <String>]`: Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="35dfb-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="35dfb-148">`[Tag <IResourceTags>]`: Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="35dfb-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="35dfb-149">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="35dfb-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="35dfb-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> per abilitare l'affinità del client <code>false</code> , per interrompere l'invio di cookie di affinità della sessione, che instradano le richieste client nella stessa sessione alla stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="35dfb-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="35dfb-151">Il valore predefinito è <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="35dfb-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> per abilitare l'autenticazione del certificato client (TLS Mutual Authentication); in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="35dfb-153">Il valore predefinito è <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="35dfb-154">`[ClientCertExclusionPath <String>]`: percorsi di esclusione separati da virgola con autenticazione del certificato client</span><span class="sxs-lookup"><span data-stu-id="35dfb-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="35dfb-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: L'impostazione dell'applicazione sostituisce l'app clonata.</span><span class="sxs-lookup"><span data-stu-id="35dfb-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="35dfb-156">Se specificato, queste impostazioni sostituiscono le impostazioni clonate dall'app di origine.</span><span class="sxs-lookup"><span data-stu-id="35dfb-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="35dfb-157">In caso contrario, vengono mantenute le impostazioni delle applicazioni dall'app di origine.</span><span class="sxs-lookup"><span data-stu-id="35dfb-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="35dfb-158">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="35dfb-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="35dfb-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> per clonare hostname personalizzati dall'app di origine; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="35dfb-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> per clonare il controllo del codice sorgente dall'app di origine; in caso contrario <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="35dfb-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> per configurare il bilanciamento del carico per l'app di origine e destinazione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="35dfb-162">`[CloningInfoCorrelationId <String>]`: ID correlazione dell'operazione di clonazione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="35dfb-163">Questo ID unisce più operazioni di clonazione insieme per usare lo stesso snapshot.</span><span class="sxs-lookup"><span data-stu-id="35dfb-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="35dfb-164">`[CloningInfoHostingEnvironment <String>]`: Ambiente di servizio app.</span><span class="sxs-lookup"><span data-stu-id="35dfb-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="35dfb-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> per sovrascrivere l'app di destinazione; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="35dfb-166">`[CloningInfoSourceWebAppLocation <String>]`: Posizione di origine app ex: ovest degli Stati Uniti o Nord Europa</span><span class="sxs-lookup"><span data-stu-id="35dfb-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="35dfb-167">`[CloningInfoTrafficManagerProfileId <String>]`: ID risorsa ARM del profilo di gestione traffico da usare, se esistente.</span><span class="sxs-lookup"><span data-stu-id="35dfb-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="35dfb-168">ID risorsa del gestore del traffico con il formato/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="35dfb-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="35dfb-169">`[CloningInfoTrafficManagerProfileName <String>]`: Nome del profilo di Traffic Manager da creare.</span><span class="sxs-lookup"><span data-stu-id="35dfb-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="35dfb-170">Questa operazione è necessaria solo se il profilo di Traffic Manager non esiste già.</span><span class="sxs-lookup"><span data-stu-id="35dfb-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="35dfb-171">`[Config <ISiteConfig>]`: Configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="35dfb-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="35dfb-172">`IsPushEnabled <Boolean>`: Ottiene o imposta un contrassegno che indica se l'endpoint push è abilitato.</span><span class="sxs-lookup"><span data-stu-id="35dfb-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="35dfb-173">`[ActionMinProcessExecutionTime <String>]`: Tempo minimo necessario per l'esecuzione del processo prima di eseguire l'azione</span><span class="sxs-lookup"><span data-stu-id="35dfb-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="35dfb-174">`[ActionType <AutoHealActionType?>]`: Azione predefinita da intraprendere.</span><span class="sxs-lookup"><span data-stu-id="35dfb-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="35dfb-175">`[AlwaysOn <Boolean?>]`: <code>true</code> se è sempre attivato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-176">`[ApiDefinitionUrl <String>]`: URL della definizione dell'API.</span><span class="sxs-lookup"><span data-stu-id="35dfb-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="35dfb-177">`[ApiManagementConfigId <String>]`: APIM-Api identificatore.</span><span class="sxs-lookup"><span data-stu-id="35dfb-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="35dfb-178">`[AppCommandLine <String>]`: Riga di comando dell'app da avviare.</span><span class="sxs-lookup"><span data-stu-id="35dfb-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="35dfb-179">`[AppSetting <INameValuePair[]>]`: Impostazioni applicazione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="35dfb-180">`[Name <String>]`: Nome coppia.</span><span class="sxs-lookup"><span data-stu-id="35dfb-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="35dfb-181">`[Value <String>]`: Valore pair.</span><span class="sxs-lookup"><span data-stu-id="35dfb-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="35dfb-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> se l'opzione Correzione automatica è abilitata; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-183">`[AutoSwapSlotName <String>]`: Nome dello slot di scambio automatico.</span><span class="sxs-lookup"><span data-stu-id="35dfb-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="35dfb-184">`[ConnectionString <IConnStringInfo[]>]`: Stringhe di connessione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="35dfb-185">`[ConnectionString <String>]`: Valore stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="35dfb-186">`[Name <String>]`: Nome della stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="35dfb-187">`[Type <ConnectionStringType?>]`: Tipo di database.</span><span class="sxs-lookup"><span data-stu-id="35dfb-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="35dfb-188">`[CorAllowedOrigin <String[]>]`: Ottiene o imposta l'elenco di origini che devono essere consentite per effettuare chiamate tra origini, ad esempio: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="35dfb-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="35dfb-189">Usare "\*" per consentire tutti.</span><span class="sxs-lookup"><span data-stu-id="35dfb-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="35dfb-190">`[CorSupportCredentials <Boolean?>]`: Ottiene o imposta se sono consentite le richieste di CORS con le credenziali.</span><span class="sxs-lookup"><span data-stu-id="35dfb-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="35dfb-191"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="35dfb-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="35dfb-192">`[CustomActionExe <String>]`: Eseguibile da eseguire.</span><span class="sxs-lookup"><span data-stu-id="35dfb-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="35dfb-193">`[CustomActionParameter <String>]`: Parametri per l'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="35dfb-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="35dfb-194">`[DefaultDocument <String[]>]`: Documenti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="35dfb-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="35dfb-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se è abilitata la registrazione dettagliata degli errori; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-196">`[DocumentRoot <String>]`: Radice del documento.</span><span class="sxs-lookup"><span data-stu-id="35dfb-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="35dfb-197">`[DynamicTagsJson <String>]`: Ottiene o imposta una stringa JSON contenente un elenco di tag dinamici che verranno valutati dalle attestazioni degli utenti nell'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="35dfb-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="35dfb-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: Elenco delle regole di rampa.</span><span class="sxs-lookup"><span data-stu-id="35dfb-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="35dfb-199">`[ActionHostName <String>]`: Hostname di uno slot a cui verrà reindirizzato il traffico, se deciso.</span><span class="sxs-lookup"><span data-stu-id="35dfb-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="35dfb-200">Ad esempio.</span><span class="sxs-lookup"><span data-stu-id="35dfb-200">E.g.</span></span> <span data-ttu-id="35dfb-201">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="35dfb-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="35dfb-202">`[ChangeDecisionCallbackUrl <String>]`: L'algoritmo decisionale personalizzato può essere fornito nell'estensione del sito di TiPCallback, quale URL può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="35dfb-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="35dfb-203">Vedere estensione del sito TiPCallback per il patibolo e i contratti.</span><span class="sxs-lookup"><span data-stu-id="35dfb-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="35dfb-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="35dfb-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="35dfb-205">`[ChangeIntervalInMinute <Int32?>]`: Specifica l'intervallo in minuti per rivalutare ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="35dfb-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="35dfb-206">`[ChangeStep <Double?>]`: Nello scenario rampa automatica questo è il passaggio da cui aggiungere/rimuovere <code>ReroutePercentage</code> fino a quando non raggiunge \n <code>MinReroutePercentage</code> o         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="35dfb-207">Le metriche del sito vengono controllate ogni N minuti specificato nell' <code>ChangeIntervalInMinutes</code> algoritmo di decisione .\nCustom può essere fornito nell'estensione del sito TiPCallback in cui è possibile specificare l'URL <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="35dfb-208">`[MaxReroutePercentage <Double?>]`: Specifica il limite superiore al di sotto del quale ReroutePercentage rimarrà.</span><span class="sxs-lookup"><span data-stu-id="35dfb-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="35dfb-209">`[MinReroutePercentage <Double?>]`: Specifica il contorno inferiore sopra il quale ReroutePercentage rimarrà.</span><span class="sxs-lookup"><span data-stu-id="35dfb-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="35dfb-210">`[Name <String>]`: Nome della regola di routing.</span><span class="sxs-lookup"><span data-stu-id="35dfb-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="35dfb-211">Il nome consigliato consiste nel puntare allo slot che riceverà il traffico nell'esperimento.</span><span class="sxs-lookup"><span data-stu-id="35dfb-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="35dfb-212">`[ReroutePercentage <Double?>]`: Percentuale del traffico a cui verrà reindirizzato <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="35dfb-213">`[FtpsState <FtpsState?>]`: Stato del servizio FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="35dfb-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="35dfb-214">`[HandlerMapping <IHandlerMapping[]>]`: Mapping dei gestori.</span><span class="sxs-lookup"><span data-stu-id="35dfb-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="35dfb-215">`[Argument <String>]`: Argomenti della riga di comando da passare al processore di script.</span><span class="sxs-lookup"><span data-stu-id="35dfb-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="35dfb-216">`[Extension <String>]`: Le richieste con questa estensione verranno gestite con l'applicazione specificata FastCGI.</span><span class="sxs-lookup"><span data-stu-id="35dfb-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="35dfb-217">`[ScriptProcessor <String>]`: Il percorso assoluto dell'applicazione FastCGI.</span><span class="sxs-lookup"><span data-stu-id="35dfb-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="35dfb-218">`[HealthCheckPath <String>]`: Percorso di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="35dfb-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="35dfb-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configura un sito Web per consentire ai client di connettersi tramite http 2.0</span><span class="sxs-lookup"><span data-stu-id="35dfb-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="35dfb-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se la registrazione http è abilitata; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrizioni di sicurezza IP per Main.</span><span class="sxs-lookup"><span data-stu-id="35dfb-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="35dfb-222">`[Action <String>]`: Consenti o negare l'accesso per questo intervallo IP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="35dfb-223">`[Description <String>]`: Descrizione della regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="35dfb-224">`[IPAddress <String>]`: Indirizzo IP per cui è valida la restrizione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="35dfb-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="35dfb-225">Può essere in forma di indirizzo IPv4 puro (proprietà submask necessaria) o notazione CIDR, ad esempio IPv4/Mask (corrispondenza di bit iniziale).</span><span class="sxs-lookup"><span data-stu-id="35dfb-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="35dfb-226">Per la notazione CIDR, la proprietà submask non deve essere specificata.</span><span class="sxs-lookup"><span data-stu-id="35dfb-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="35dfb-227">`[Name <String>]`: Nome regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="35dfb-228">`[Priority <Int32?>]`: Priorità della regola di restrizione IP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="35dfb-229">`[SubnetMask <String>]`: Subnet mask per l'intervallo di indirizzi IP per cui è valida la restrizione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="35dfb-230">`[SubnetTrafficTag <Int32?>]`: tag di traffico subnet (interno)</span><span class="sxs-lookup"><span data-stu-id="35dfb-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="35dfb-231">`[Tag <IPFilterTag?>]`: Definisce l'uso di questo filtro IP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="35dfb-232">Questo per supportare il filtro IP sui proxy.</span><span class="sxs-lookup"><span data-stu-id="35dfb-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="35dfb-233">`[VnetSubnetResourceId <String>]`: ID risorsa di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="35dfb-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="35dfb-234">`[VnetTrafficTag <Int32?>]`: (interno) VNET traffico</span><span class="sxs-lookup"><span data-stu-id="35dfb-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="35dfb-235">`[JavaContainer <String>]`: Contenitore Java.</span><span class="sxs-lookup"><span data-stu-id="35dfb-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="35dfb-236">`[JavaContainerVersion <String>]`: Versione contenitore Java.</span><span class="sxs-lookup"><span data-stu-id="35dfb-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="35dfb-237">`[JavaVersion <String>]`: Versione Java.</span><span class="sxs-lookup"><span data-stu-id="35dfb-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="35dfb-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Utilizzo massimo consentito per le dimensioni del disco in MB.</span><span class="sxs-lookup"><span data-stu-id="35dfb-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="35dfb-239">`[LimitMaxMemoryInMb <Int64?>]`: Utilizzo massimo consentito della memoria in MB.</span><span class="sxs-lookup"><span data-stu-id="35dfb-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="35dfb-240">`[LimitMaxPercentageCpu <Double?>]`: Percentuale massima di utilizzo della CPU consentita.</span><span class="sxs-lookup"><span data-stu-id="35dfb-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="35dfb-241">`[LinuxFxVersion <String>]`: Framework e versione dell'app Linux</span><span class="sxs-lookup"><span data-stu-id="35dfb-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="35dfb-242">`[LoadBalancing <SiteLoadBalancing?>]`: Bilanciamento del carico del sito.</span><span class="sxs-lookup"><span data-stu-id="35dfb-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="35dfb-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> per abilitare MySQL locale; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-244">`[LogsDirectorySizeLimit <Int32?>]`: Limite di dimensione della directory registri HTTP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="35dfb-245">`[MachineKeyDecryption <String>]`: Algoritmo usato per la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="35dfb-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="35dfb-246">`[MachineKeyDecryptionKey <String>]`: Chiave di decrittografia.</span><span class="sxs-lookup"><span data-stu-id="35dfb-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="35dfb-247">`[MachineKeyValidation <String>]`: Convalida MachineKey.</span><span class="sxs-lookup"><span data-stu-id="35dfb-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="35dfb-248">`[MachineKeyValidationKey <String>]`: Chiave di convalida.</span><span class="sxs-lookup"><span data-stu-id="35dfb-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="35dfb-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Modalità pipeline gestita.</span><span class="sxs-lookup"><span data-stu-id="35dfb-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="35dfb-250">`[ManagedServiceIdentityId <Int32?>]`: ID identità servizio gestito</span><span class="sxs-lookup"><span data-stu-id="35dfb-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="35dfb-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura la versione minima di TLS necessaria per le richieste SSL</span><span class="sxs-lookup"><span data-stu-id="35dfb-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="35dfb-252">`[NetFrameworkVersion <String>]`: Versione di .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="35dfb-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="35dfb-253">`[NodeVersion <String>]`: Versione di Node.js.</span><span class="sxs-lookup"><span data-stu-id="35dfb-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="35dfb-254">`[NumberOfWorker <Int32?>]`: Numero di lavoratori.</span><span class="sxs-lookup"><span data-stu-id="35dfb-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="35dfb-255">`[PhpVersion <String>]`: Versione di PHP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="35dfb-256">`[PowerShellVersion <String>]`: Versione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35dfb-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="35dfb-257">`[PreWarmedInstanceCount <Int32?>]`: Numero di istanze preriscaldate.</span><span class="sxs-lookup"><span data-stu-id="35dfb-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="35dfb-258">Questa impostazione si applica solo ai piani consumi e elastici</span><span class="sxs-lookup"><span data-stu-id="35dfb-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="35dfb-259">`[PublishingUsername <String>]`: Nome utente di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="35dfb-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="35dfb-260">`[PushKind <String>]`: Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="35dfb-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="35dfb-261">`[PythonVersion <String>]`: Versione di Python.</span><span class="sxs-lookup"><span data-stu-id="35dfb-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="35dfb-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se il debug remoto è abilitato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-263">`[RemoteDebuggingVersion <String>]`: Versione di debug remoto.</span><span class="sxs-lookup"><span data-stu-id="35dfb-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="35dfb-264">`[RequestCount <Int32?>]`: Richiedi conteggio.</span><span class="sxs-lookup"><span data-stu-id="35dfb-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="35dfb-265">`[RequestTimeInterval <String>]`: Intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="35dfb-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="35dfb-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> se l'analisi delle richieste è abilitata; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-267">`[RequestTracingExpirationTime <DateTime?>]`: Richiedi ora di scadenza dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="35dfb-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="35dfb-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrizioni di sicurezza IP per SCM.</span><span class="sxs-lookup"><span data-stu-id="35dfb-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="35dfb-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Restrizioni di sicurezza IP per SCM per l'uso di Main.</span><span class="sxs-lookup"><span data-stu-id="35dfb-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="35dfb-270">`[ScmType <ScmType?>]`: Tipo SCM.</span><span class="sxs-lookup"><span data-stu-id="35dfb-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="35dfb-271">`[SlowRequestCount <Int32?>]`: Richiedi conteggio.</span><span class="sxs-lookup"><span data-stu-id="35dfb-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="35dfb-272">`[SlowRequestTimeInterval <String>]`: Intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="35dfb-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="35dfb-273">`[SlowRequestTimeTaken <String>]`: Tempo impiegato.</span><span class="sxs-lookup"><span data-stu-id="35dfb-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="35dfb-274">`[TagWhitelistJson <String>]`: Ottiene o imposta una stringa JSON contenente un elenco di tag whitelist per l'uso da parte dell'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="35dfb-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="35dfb-275">`[TagsRequiringAuth <String>]`: Ottiene o imposta una stringa JSON contenente un elenco di tag che richiedono l'utilizzo dell'autenticazione utente nell'endpoint di registrazione push.</span><span class="sxs-lookup"><span data-stu-id="35dfb-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="35dfb-276">I tag possono essere costituiti da caratteri alfanumerici e i seguenti:' _',' @',' #',' .',':','-'.</span><span class="sxs-lookup"><span data-stu-id="35dfb-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="35dfb-277">La convalida deve essere eseguita in PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="35dfb-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="35dfb-278">`[TracingOption <String>]`: Opzioni di traccia.</span><span class="sxs-lookup"><span data-stu-id="35dfb-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="35dfb-279">`[TriggerPrivateBytesInKb <Int32?>]`: Regola basata sui byte privati.</span><span class="sxs-lookup"><span data-stu-id="35dfb-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="35dfb-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Regola basata sui codici di stato.</span><span class="sxs-lookup"><span data-stu-id="35dfb-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="35dfb-281">`[Count <Int32?>]`: Richiedi conteggio.</span><span class="sxs-lookup"><span data-stu-id="35dfb-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="35dfb-282">`[Status <Int32?>]`: Codice di stato HTTP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="35dfb-283">`[SubStatus <Int32?>]`: Richiedi stato secondario.</span><span class="sxs-lookup"><span data-stu-id="35dfb-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="35dfb-284">`[TimeInterval <String>]`: Intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="35dfb-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="35dfb-285">`[Win32Status <Int32?>]`: Codice di errore Win32.</span><span class="sxs-lookup"><span data-stu-id="35dfb-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="35dfb-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> per usare il processo di lavoro a 32 bit; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-287">`[VirtualApplication <IVirtualApplication[]>]`: Applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="35dfb-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="35dfb-288">`[PhysicalPath <String>]`: Percorso fisico.</span><span class="sxs-lookup"><span data-stu-id="35dfb-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="35dfb-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> se il precaricamento è abilitato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="35dfb-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Directory virtuali per l'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="35dfb-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="35dfb-291">`[PhysicalPath <String>]`: Percorso fisico.</span><span class="sxs-lookup"><span data-stu-id="35dfb-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="35dfb-292">`[VirtualPath <String>]`: Percorso dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="35dfb-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="35dfb-293">`[VirtualPath <String>]`: Percorso virtuale.</span><span class="sxs-lookup"><span data-stu-id="35dfb-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="35dfb-294">`[VnetName <String>]`: Nome rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="35dfb-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="35dfb-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket è abilitato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="35dfb-296">`[WindowsFxVersion <String>]`: Framework e versione per le app Xenon</span><span class="sxs-lookup"><span data-stu-id="35dfb-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="35dfb-297">`[XManagedServiceIdentityId <Int32?>]`: ID identità servizio gestito esplicito</span><span class="sxs-lookup"><span data-stu-id="35dfb-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="35dfb-298">`[ContainerSize <Int32?>]`: Dimensioni del contenitore di funzioni.</span><span class="sxs-lookup"><span data-stu-id="35dfb-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="35dfb-299">`[DailyMemoryTimeQuota <Int32?>]`: Quota massima di memoria giornaliera consentita (applicabile solo per le app dinamiche).</span><span class="sxs-lookup"><span data-stu-id="35dfb-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="35dfb-300">`[Enabled <Boolean?>]`: <code>true</code> se l'app è abilitata; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="35dfb-301">L'impostazione di questo valore su false disabilita l'app (l'app non è in linea).</span><span class="sxs-lookup"><span data-stu-id="35dfb-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="35dfb-302">`[HostNameSslState <IHostNameSslState[]>]`: Gli Stati SSL del nome host vengono usati per gestire i binding SSL per i nomi host dell'app.</span><span class="sxs-lookup"><span data-stu-id="35dfb-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="35dfb-303">`[HostType <HostType?>]`: Indica se il nome host è un nome host standard o repository.</span><span class="sxs-lookup"><span data-stu-id="35dfb-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="35dfb-304">`[Name <String>]`Hostname.</span><span class="sxs-lookup"><span data-stu-id="35dfb-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="35dfb-305">`[SslState <SslState?>]`: Tipo SSL.</span><span class="sxs-lookup"><span data-stu-id="35dfb-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="35dfb-306">`[Thumbprint <String>]`: Identificazione personale del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="35dfb-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="35dfb-307">`[ToUpdate <Boolean?>]`: Impostato su <code>true</code> per aggiornare il nome host esistente.</span><span class="sxs-lookup"><span data-stu-id="35dfb-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="35dfb-308">`[VirtualIP <String>]`: Indirizzo IP virtuale assegnato al nome host se è abilitato il protocollo SSL basato su IP.</span><span class="sxs-lookup"><span data-stu-id="35dfb-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="35dfb-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> per disabilitare i nomi host pubblici dell'app; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="35dfb-310">Se <code>true</code> l'app è accessibile solo tramite il processo di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="35dfb-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="35dfb-311">`[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente di servizio app.</span><span class="sxs-lookup"><span data-stu-id="35dfb-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="35dfb-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configura un sito Web in cui accettare solo le richieste HTTPS.</span><span class="sxs-lookup"><span data-stu-id="35dfb-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="35dfb-313">Problemi di reindirizzamento per le richieste http</span><span class="sxs-lookup"><span data-stu-id="35dfb-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="35dfb-314">`[HyperV <Boolean?>]`: Sandbox Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="35dfb-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="35dfb-315">`[IdentityType <ManagedServiceIdentityType?>]`: Tipo di identità del servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="35dfb-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="35dfb-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: L'elenco delle identità assegnate dall'utente associato alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="35dfb-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="35dfb-317">I riferimenti chiave del dizionario delle identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="35dfb-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="35dfb-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="35dfb-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="35dfb-319">`[IsXenon <Boolean?>]`: Obsolete: sandbox Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="35dfb-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="35dfb-320">`[RedundancyMode <RedundancyMode?>]`: Modalità di ridondanza del sito</span><span class="sxs-lookup"><span data-stu-id="35dfb-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="35dfb-321">`[Reserved <Boolean?>]`: <code>true</code> se riservato; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="35dfb-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> per arrestare il sito SCM (kudu) quando l'app viene arrestata; in caso contrario, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="35dfb-323">Il valore predefinito è <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="35dfb-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="35dfb-324">`[ServerFarmId <String>]`: ID risorsa del piano di servizio app associato, formattato come: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="35dfb-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="35dfb-325">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35dfb-325">RELATED LINKS</span></span>
