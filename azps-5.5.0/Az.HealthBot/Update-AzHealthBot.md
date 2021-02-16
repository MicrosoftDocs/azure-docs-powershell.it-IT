---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: b14ed0d682a6ba74eb557aae79a4fe151e952a73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200183"
---
# <span data-ttu-id="4752c-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="4752c-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="4752c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4752c-102">SYNOPSIS</span></span>
<span data-ttu-id="4752c-103">Patch a HealthBot.</span><span class="sxs-lookup"><span data-stu-id="4752c-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="4752c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4752c-104">SYNTAX</span></span>

### <span data-ttu-id="4752c-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4752c-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4752c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4752c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4752c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4752c-107">DESCRIPTION</span></span>
<span data-ttu-id="4752c-108">Patch a HealthBot.</span><span class="sxs-lookup"><span data-stu-id="4752c-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="4752c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4752c-109">EXAMPLES</span></span>

### <span data-ttu-id="4752c-110">Esempio 1: aggiornare HealthBot in base al nome e al nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4752c-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="4752c-111">Aggiornare HealthBot in base al nome del gruppo di risorse e al nome</span><span class="sxs-lookup"><span data-stu-id="4752c-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="4752c-112">Esempio 2: aggiornare HealthBot per InputObject</span><span class="sxs-lookup"><span data-stu-id="4752c-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="4752c-113">Aggiornare HealthBot per InputObject</span><span class="sxs-lookup"><span data-stu-id="4752c-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="4752c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4752c-114">PARAMETERS</span></span>

### <span data-ttu-id="4752c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4752c-115">-DefaultProfile</span></span>
<span data-ttu-id="4752c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4752c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4752c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4752c-117">-InputObject</span></span>
<span data-ttu-id="4752c-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4752c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4752c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4752c-119">-Name</span></span>
<span data-ttu-id="4752c-120">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="4752c-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="4752c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4752c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4752c-122">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4752c-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="4752c-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="4752c-123">-Sku</span></span>
<span data-ttu-id="4752c-124">Nome dello SKU HealthBot</span><span class="sxs-lookup"><span data-stu-id="4752c-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4752c-125">-SubscriptionId</span></span>
<span data-ttu-id="4752c-126">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="4752c-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4752c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="4752c-127">-Tag</span></span>
<span data-ttu-id="4752c-128">Tag per un modello HealthBot.</span><span class="sxs-lookup"><span data-stu-id="4752c-128">Tags for a HealthBot.</span></span>

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

### <span data-ttu-id="4752c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4752c-129">-Confirm</span></span>
<span data-ttu-id="4752c-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4752c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4752c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4752c-131">-WhatIf</span></span>
<span data-ttu-id="4752c-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4752c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4752c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4752c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4752c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4752c-134">CommonParameters</span></span>
<span data-ttu-id="4752c-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4752c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4752c-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4752c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4752c-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="4752c-137">INPUTS</span></span>

### <span data-ttu-id="4752c-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="4752c-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="4752c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4752c-139">OUTPUTS</span></span>

### <span data-ttu-id="4752c-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="4752c-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="4752c-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="4752c-141">NOTES</span></span>

<span data-ttu-id="4752c-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4752c-142">ALIASES</span></span>

<span data-ttu-id="4752c-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="4752c-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4752c-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4752c-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4752c-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4752c-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4752c-146">INPUTOBJECT <IHealthBotIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="4752c-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4752c-147">`[BotName <String>]`: nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="4752c-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="4752c-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4752c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4752c-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4752c-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="4752c-150">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4752c-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4752c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4752c-151">RELATED LINKS</span></span>

