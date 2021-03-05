---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: 330aca1a9d4cc9438bdf360d5aee4af914df6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007293"
---
# <span data-ttu-id="2f5bf-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="2f5bf-101">Update-AzBotService</span></span>

## <span data-ttu-id="2f5bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5bf-103">Aggiorna un servizio Bot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-103">Updates a Bot Service</span></span>

## <span data-ttu-id="2f5bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f5bf-104">SYNTAX</span></span>

### <span data-ttu-id="2f5bf-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2f5bf-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2f5bf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2f5bf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2f5bf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2f5bf-107">DESCRIPTION</span></span>
<span data-ttu-id="2f5bf-108">Aggiorna un servizio Bot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-108">Updates a Bot Service</span></span>

## <span data-ttu-id="2f5bf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f5bf-109">EXAMPLES</span></span>

### <span data-ttu-id="2f5bf-110">Esempio 1: Aggiornare il bot in base al nome e al nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2f5bf-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="2f5bf-111">Aggiornare il bot in base al nome e al nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2f5bf-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="2f5bf-112">Esempio 2: Aggiornare il bot in base a InputObject</span><span class="sxs-lookup"><span data-stu-id="2f5bf-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="2f5bf-113">Aggiornare il bot in base a InputObject</span><span class="sxs-lookup"><span data-stu-id="2f5bf-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="2f5bf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f5bf-114">PARAMETERS</span></span>

### <span data-ttu-id="2f5bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5bf-115">-DefaultProfile</span></span>
<span data-ttu-id="2f5bf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f5bf-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f5bf-117">-Description</span></span>
<span data-ttu-id="2f5bf-118">La descrizione del bot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-118">The description of the bot</span></span>

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

### <span data-ttu-id="2f5bf-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="2f5bf-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="2f5bf-120">Chiave Application Insights</span><span class="sxs-lookup"><span data-stu-id="2f5bf-120">The Application Insights key</span></span>

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

### <span data-ttu-id="2f5bf-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="2f5bf-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="2f5bf-122">Chiave API Application Insights</span><span class="sxs-lookup"><span data-stu-id="2f5bf-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="2f5bf-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="2f5bf-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="2f5bf-124">The Application Insights App Id</span><span class="sxs-lookup"><span data-stu-id="2f5bf-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="2f5bf-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f5bf-125">-DisplayName</span></span>
<span data-ttu-id="2f5bf-126">Il nome del bot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-126">The Name of the bot</span></span>

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

### <span data-ttu-id="2f5bf-127">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="2f5bf-127">-Endpoint</span></span>
<span data-ttu-id="2f5bf-128">Endpoint del bot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="2f5bf-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="2f5bf-129">-Etag</span></span>
<span data-ttu-id="2f5bf-130">Tag entità</span><span class="sxs-lookup"><span data-stu-id="2f5bf-130">Entity Tag</span></span>

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

### <span data-ttu-id="2f5bf-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="2f5bf-131">-IconUrl</span></span>
<span data-ttu-id="2f5bf-132">L'URL dell'icona del bot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="2f5bf-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f5bf-133">-InputObject</span></span>
<span data-ttu-id="2f5bf-134">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2f5bf-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="2f5bf-135">-Kind</span></span>
<span data-ttu-id="2f5bf-136">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-136">Required.</span></span>
<span data-ttu-id="2f5bf-137">Ottiene o imposta il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-137">Gets or sets the Kind of the resource.</span></span>

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

### <span data-ttu-id="2f5bf-138">-Location</span><span class="sxs-lookup"><span data-stu-id="2f5bf-138">-Location</span></span>
<span data-ttu-id="2f5bf-139">Specifica la posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="2f5bf-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="2f5bf-140">-LuisAppId</span></span>
<span data-ttu-id="2f5bf-141">Raccolta di ID app LUIS</span><span class="sxs-lookup"><span data-stu-id="2f5bf-141">Collection of LUIS App Ids</span></span>

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

### <span data-ttu-id="2f5bf-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="2f5bf-142">-LuisKey</span></span>
<span data-ttu-id="2f5bf-143">Chiave LUIS</span><span class="sxs-lookup"><span data-stu-id="2f5bf-143">The LUIS Key</span></span>

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

### <span data-ttu-id="2f5bf-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="2f5bf-144">-MsaAppId</span></span>
<span data-ttu-id="2f5bf-145">ID app Microsoft per il bot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="2f5bf-146">-Name</span><span class="sxs-lookup"><span data-stu-id="2f5bf-146">-Name</span></span>
<span data-ttu-id="2f5bf-147">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="2f5bf-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f5bf-148">-ResourceGroupName</span></span>
<span data-ttu-id="2f5bf-149">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="2f5bf-150">-SKUName</span><span class="sxs-lookup"><span data-stu-id="2f5bf-150">-SkuName</span></span>
<span data-ttu-id="2f5bf-151">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="2f5bf-151">The sku name</span></span>

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

### <span data-ttu-id="2f5bf-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f5bf-152">-SubscriptionId</span></span>
<span data-ttu-id="2f5bf-153">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="2f5bf-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f5bf-154">-Tag</span></span>
<span data-ttu-id="2f5bf-155">Contiene tag di risorsa definiti come coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="2f5bf-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f5bf-156">-Confirm</span></span>
<span data-ttu-id="2f5bf-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f5bf-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f5bf-158">-WhatIf</span></span>
<span data-ttu-id="2f5bf-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f5bf-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f5bf-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5bf-161">CommonParameters</span></span>
<span data-ttu-id="2f5bf-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5bf-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5bf-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="2f5bf-164">INPUTS</span></span>

### <span data-ttu-id="2f5bf-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="2f5bf-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="2f5bf-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f5bf-166">OUTPUTS</span></span>

### <span data-ttu-id="2f5bf-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="2f5bf-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="2f5bf-168">NOTES</span></span>

<span data-ttu-id="2f5bf-169">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2f5bf-169">ALIASES</span></span>

<span data-ttu-id="2f5bf-170">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2f5bf-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2f5bf-171">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f5bf-172">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2f5bf-173">INPUTOBJECT <IBotServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="2f5bf-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2f5bf-174">`[ChannelName <ChannelName?>]`: nome della risorsa Canale.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="2f5bf-175">`[ConnectionName <String>]`: nome della risorsa Impostazioni di connessione al servizio Bot</span><span class="sxs-lookup"><span data-stu-id="2f5bf-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="2f5bf-176">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="2f5bf-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f5bf-177">`[ResourceGroupName <String>]`: nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="2f5bf-178">`[ResourceName <String>]`: nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="2f5bf-179">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2f5bf-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="2f5bf-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f5bf-180">RELATED LINKS</span></span>

