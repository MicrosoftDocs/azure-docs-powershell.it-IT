---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: f7dd02a214fa32223e052c1999329699f1c653e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488695"
---
# <span data-ttu-id="d8091-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="d8091-101">Update-AzBotService</span></span>

## <span data-ttu-id="d8091-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8091-102">SYNOPSIS</span></span>
<span data-ttu-id="d8091-103">Aggiorna un servizio bot</span><span class="sxs-lookup"><span data-stu-id="d8091-103">Updates a Bot Service</span></span>

## <span data-ttu-id="d8091-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8091-104">SYNTAX</span></span>

### <span data-ttu-id="d8091-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8091-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8091-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d8091-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8091-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8091-107">DESCRIPTION</span></span>
<span data-ttu-id="d8091-108">Aggiorna un servizio bot</span><span class="sxs-lookup"><span data-stu-id="d8091-108">Updates a Bot Service</span></span>

## <span data-ttu-id="d8091-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8091-109">EXAMPLES</span></span>

### <span data-ttu-id="d8091-110">Esempio 1: aggiornare il bot per nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8091-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="d8091-111">Aggiornare il bot per nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8091-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="d8091-112">Esempio 2: aggiornare il bot tramite InputObject</span><span class="sxs-lookup"><span data-stu-id="d8091-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="d8091-113">Aggiornare il bot da InputObject</span><span class="sxs-lookup"><span data-stu-id="d8091-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="d8091-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8091-114">PARAMETERS</span></span>

### <span data-ttu-id="d8091-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8091-115">-DefaultProfile</span></span>
<span data-ttu-id="d8091-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8091-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8091-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8091-117">-Description</span></span>
<span data-ttu-id="d8091-118">Descrizione del bot</span><span class="sxs-lookup"><span data-stu-id="d8091-118">The description of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="d8091-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="d8091-120">Chiave di Insight per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="d8091-120">The Application Insights key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="d8091-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="d8091-122">Chiave dell'API Insights dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d8091-122">The Application Insights Api Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="d8091-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="d8091-124">ID app Insights dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d8091-124">The Application Insights App Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d8091-125">-DisplayName</span></span>
<span data-ttu-id="d8091-126">Nome del bot</span><span class="sxs-lookup"><span data-stu-id="d8091-126">The Name of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-127">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d8091-127">-Endpoint</span></span>
<span data-ttu-id="d8091-128">Endpoint del bot</span><span class="sxs-lookup"><span data-stu-id="d8091-128">The bot's endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-129">-ETag</span><span class="sxs-lookup"><span data-stu-id="d8091-129">-Etag</span></span>
<span data-ttu-id="d8091-130">Tag di entità</span><span class="sxs-lookup"><span data-stu-id="d8091-130">Entity Tag</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="d8091-131">-IconUrl</span></span>
<span data-ttu-id="d8091-132">URL dell'icona del bot</span><span class="sxs-lookup"><span data-stu-id="d8091-132">The Icon Url of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8091-133">-InputObject</span></span>
<span data-ttu-id="d8091-134">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d8091-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-135">-Tipo</span><span class="sxs-lookup"><span data-stu-id="d8091-135">-Kind</span></span>
<span data-ttu-id="d8091-136">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d8091-136">Required.</span></span>
<span data-ttu-id="d8091-137">Ottiene o imposta il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d8091-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-138">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d8091-138">-Location</span></span>
<span data-ttu-id="d8091-139">Specifica la posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d8091-139">Specifies the location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="d8091-140">-LuisAppId</span></span>
<span data-ttu-id="d8091-141">Raccolta di ID app LUIS</span><span class="sxs-lookup"><span data-stu-id="d8091-141">Collection of LUIS App Ids</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="d8091-142">-LuisKey</span></span>
<span data-ttu-id="d8091-143">Il tasto LUIS</span><span class="sxs-lookup"><span data-stu-id="d8091-143">The LUIS Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="d8091-144">-MsaAppId</span></span>
<span data-ttu-id="d8091-145">ID app Microsoft per il bot</span><span class="sxs-lookup"><span data-stu-id="d8091-145">Microsoft App Id for the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8091-146">-Name</span></span>
<span data-ttu-id="d8091-147">Il nome della risorsa bot.</span><span class="sxs-lookup"><span data-stu-id="d8091-147">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8091-148">-ResourceGroupName</span></span>
<span data-ttu-id="d8091-149">Nome del gruppo di risorse bot nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="d8091-149">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d8091-150">-SkuName</span></span>
<span data-ttu-id="d8091-151">Nome Usk</span><span class="sxs-lookup"><span data-stu-id="d8091-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8091-152">-SubscriptionId</span></span>
<span data-ttu-id="d8091-153">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8091-153">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8091-154">-Tag</span></span>
<span data-ttu-id="d8091-155">Contiene i tag delle risorse definiti come coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="d8091-155">Contains resource tags defined as key/value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8091-156">-Confirm</span></span>
<span data-ttu-id="d8091-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8091-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8091-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8091-158">-WhatIf</span></span>
<span data-ttu-id="d8091-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8091-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8091-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8091-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8091-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8091-161">CommonParameters</span></span>
<span data-ttu-id="d8091-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8091-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8091-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8091-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8091-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8091-164">INPUTS</span></span>

### <span data-ttu-id="d8091-165">Microsoft. Azure. PowerShell. Cmdlets. BotService. Models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="d8091-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="d8091-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8091-166">OUTPUTS</span></span>

### <span data-ttu-id="d8091-167">Microsoft. Azure. PowerShell. Cmdlets. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="d8091-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="d8091-168">Note</span><span class="sxs-lookup"><span data-stu-id="d8091-168">NOTES</span></span>

<span data-ttu-id="d8091-169">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d8091-169">ALIASES</span></span>

<span data-ttu-id="d8091-170">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8091-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8091-171">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d8091-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8091-172">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8091-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8091-173">INPUTOBJECT <IBotServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d8091-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8091-174">`[ChannelName <ChannelName?>]`: Il nome della risorsa canale.</span><span class="sxs-lookup"><span data-stu-id="d8091-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="d8091-175">`[ConnectionName <String>]`: Il nome della risorsa di impostazione della connessione al servizio bot</span><span class="sxs-lookup"><span data-stu-id="d8091-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="d8091-176">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d8091-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8091-177">`[ResourceGroupName <String>]`: Nome del gruppo di risorse bot nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="d8091-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="d8091-178">`[ResourceName <String>]`: Il nome della risorsa bot.</span><span class="sxs-lookup"><span data-stu-id="d8091-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="d8091-179">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="d8091-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d8091-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8091-180">RELATED LINKS</span></span>

