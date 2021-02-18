---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181142"
---
# <span data-ttu-id="d4d9d-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="d4d9d-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="d4d9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d9d-103">Aggiorna un provider di risorse personalizzato esistente.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="d4d9d-104">L'unico valore che al momento può essere aggiornato con PATCH sono i tag.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="d4d9d-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4d9d-105">SYNTAX</span></span>

### <span data-ttu-id="d4d9d-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4d9d-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4d9d-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d4d9d-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4d9d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4d9d-108">DESCRIPTION</span></span>
<span data-ttu-id="d4d9d-109">Aggiorna un provider di risorse personalizzato esistente.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="d4d9d-110">L'unico valore che al momento può essere aggiornato con PATCH sono i tag.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="d4d9d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4d9d-111">EXAMPLES</span></span>

### <span data-ttu-id="d4d9d-112">Esempio 1: Aggiungere tag a un provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="d4d9d-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="d4d9d-113">Aggiornare i tag di un provider personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="d4d9d-114">Esempio 2: Aggiornare il provider personalizzato con piping</span><span class="sxs-lookup"><span data-stu-id="d4d9d-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="d4d9d-115">Aggiornare un provider personalizzato tramite piping.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="d4d9d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4d9d-116">PARAMETERS</span></span>

### <span data-ttu-id="d4d9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d9d-117">-DefaultProfile</span></span>
<span data-ttu-id="d4d9d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d9d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4d9d-119">-InputObject</span></span>
<span data-ttu-id="d4d9d-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4d9d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d4d9d-121">-Name</span></span>
<span data-ttu-id="d4d9d-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="d4d9d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d9d-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4d9d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4d9d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4d9d-125">-SubscriptionId</span></span>
<span data-ttu-id="d4d9d-126">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-126">The Azure subscription ID.</span></span>
<span data-ttu-id="d4d9d-127">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="d4d9d-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="d4d9d-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4d9d-128">-Tag</span></span>
<span data-ttu-id="d4d9d-129">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="d4d9d-129">Resource tags</span></span>

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

### <span data-ttu-id="d4d9d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4d9d-130">-Confirm</span></span>
<span data-ttu-id="d4d9d-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4d9d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d9d-132">-WhatIf</span></span>
<span data-ttu-id="d4d9d-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d9d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4d9d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d9d-135">CommonParameters</span></span>
<span data-ttu-id="d4d9d-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d9d-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d9d-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4d9d-138">INPUTS</span></span>

### <span data-ttu-id="d4d9d-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="d4d9d-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="d4d9d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4d9d-140">OUTPUTS</span></span>

### <span data-ttu-id="d4d9d-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="d4d9d-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="d4d9d-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4d9d-142">NOTES</span></span>

<span data-ttu-id="d4d9d-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d4d9d-143">ALIASES</span></span>

<span data-ttu-id="d4d9d-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d4d9d-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4d9d-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4d9d-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4d9d-147">INPUTOBJECT <ICustomProvidersIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="d4d9d-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4d9d-148">`[AssociationName <String>]`: nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="d4d9d-149">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d4d9d-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4d9d-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d4d9d-151">`[ResourceProviderName <String>]`: nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="d4d9d-152">`[Scope <String>]`: ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="d4d9d-153">`[SubscriptionId <String>]`: l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="d4d9d-154">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="d4d9d-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="d4d9d-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4d9d-155">RELATED LINKS</span></span>

