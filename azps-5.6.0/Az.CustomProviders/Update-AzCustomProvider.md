---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 0f124d818b95928f12cdc71f60c436f5691f8151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998730"
---
# <span data-ttu-id="40596-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="40596-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="40596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40596-102">SYNOPSIS</span></span>
<span data-ttu-id="40596-103">Aggiorna un provider di risorse personalizzato esistente.</span><span class="sxs-lookup"><span data-stu-id="40596-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="40596-104">L'unico valore che al momento può essere aggiornato con PATCH sono i tag.</span><span class="sxs-lookup"><span data-stu-id="40596-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="40596-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40596-105">SYNTAX</span></span>

### <span data-ttu-id="40596-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40596-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40596-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="40596-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40596-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="40596-108">DESCRIPTION</span></span>
<span data-ttu-id="40596-109">Aggiorna un provider di risorse personalizzato esistente.</span><span class="sxs-lookup"><span data-stu-id="40596-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="40596-110">L'unico valore che al momento può essere aggiornato con PATCH sono i tag.</span><span class="sxs-lookup"><span data-stu-id="40596-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="40596-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40596-111">EXAMPLES</span></span>

### <span data-ttu-id="40596-112">Esempio 1: Aggiungere tag a un provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="40596-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="40596-113">Aggiornare i tag di un provider personalizzato.</span><span class="sxs-lookup"><span data-stu-id="40596-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="40596-114">Esempio 2: Aggiornare il provider personalizzato con piping</span><span class="sxs-lookup"><span data-stu-id="40596-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="40596-115">Aggiornare un provider personalizzato tramite piping.</span><span class="sxs-lookup"><span data-stu-id="40596-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="40596-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40596-116">PARAMETERS</span></span>

### <span data-ttu-id="40596-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40596-117">-DefaultProfile</span></span>
<span data-ttu-id="40596-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40596-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40596-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40596-119">-InputObject</span></span>
<span data-ttu-id="40596-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="40596-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40596-121">-Name</span><span class="sxs-lookup"><span data-stu-id="40596-121">-Name</span></span>
<span data-ttu-id="40596-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="40596-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40596-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40596-123">-ResourceGroupName</span></span>
<span data-ttu-id="40596-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40596-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="40596-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40596-125">-SubscriptionId</span></span>
<span data-ttu-id="40596-126">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="40596-126">The Azure subscription ID.</span></span>
<span data-ttu-id="40596-127">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="40596-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="40596-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="40596-128">-Tag</span></span>
<span data-ttu-id="40596-129">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="40596-129">Resource tags</span></span>

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

### <span data-ttu-id="40596-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40596-130">-Confirm</span></span>
<span data-ttu-id="40596-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40596-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40596-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40596-132">-WhatIf</span></span>
<span data-ttu-id="40596-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40596-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40596-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40596-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40596-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40596-135">CommonParameters</span></span>
<span data-ttu-id="40596-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40596-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40596-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40596-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40596-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="40596-138">INPUTS</span></span>

### <span data-ttu-id="40596-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="40596-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="40596-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40596-140">OUTPUTS</span></span>

### <span data-ttu-id="40596-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="40596-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="40596-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="40596-142">NOTES</span></span>

<span data-ttu-id="40596-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="40596-143">ALIASES</span></span>

<span data-ttu-id="40596-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="40596-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40596-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="40596-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40596-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40596-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40596-147">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="40596-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40596-148">`[AssociationName <String>]`: nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="40596-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="40596-149">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="40596-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40596-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40596-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="40596-151">`[ResourceProviderName <String>]`: nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="40596-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="40596-152">`[Scope <String>]`: ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="40596-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="40596-153">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="40596-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="40596-154">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="40596-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="40596-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40596-155">RELATED LINKS</span></span>

