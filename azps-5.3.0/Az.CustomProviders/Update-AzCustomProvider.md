---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487755"
---
# <span data-ttu-id="3879a-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="3879a-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="3879a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3879a-102">SYNOPSIS</span></span>
<span data-ttu-id="3879a-103">Aggiorna un provider di risorse personalizzato esistente.</span><span class="sxs-lookup"><span data-stu-id="3879a-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="3879a-104">L'unico valore che può essere aggiornato tramite PATCH è attualmente i tag.</span><span class="sxs-lookup"><span data-stu-id="3879a-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="3879a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3879a-105">SYNTAX</span></span>

### <span data-ttu-id="3879a-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3879a-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3879a-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3879a-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3879a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3879a-108">DESCRIPTION</span></span>
<span data-ttu-id="3879a-109">Aggiorna un provider di risorse personalizzato esistente.</span><span class="sxs-lookup"><span data-stu-id="3879a-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="3879a-110">L'unico valore che può essere aggiornato tramite PATCH è attualmente i tag.</span><span class="sxs-lookup"><span data-stu-id="3879a-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="3879a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3879a-111">EXAMPLES</span></span>

### <span data-ttu-id="3879a-112">Esempio 1: aggiungere tag a un provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="3879a-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="3879a-113">Aggiornare i tag di un provider personalizzato.</span><span class="sxs-lookup"><span data-stu-id="3879a-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="3879a-114">Esempio 2: aggiornare un provider personalizzato con piping</span><span class="sxs-lookup"><span data-stu-id="3879a-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="3879a-115">Aggiornare un provider personalizzato tramite piping.</span><span class="sxs-lookup"><span data-stu-id="3879a-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="3879a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3879a-116">PARAMETERS</span></span>

### <span data-ttu-id="3879a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3879a-117">-DefaultProfile</span></span>
<span data-ttu-id="3879a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3879a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3879a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3879a-119">-InputObject</span></span>
<span data-ttu-id="3879a-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3879a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3879a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3879a-121">-Name</span></span>
<span data-ttu-id="3879a-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="3879a-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="3879a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3879a-123">-ResourceGroupName</span></span>
<span data-ttu-id="3879a-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3879a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="3879a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3879a-125">-SubscriptionId</span></span>
<span data-ttu-id="3879a-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="3879a-126">The Azure subscription ID.</span></span>
<span data-ttu-id="3879a-127">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="3879a-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="3879a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="3879a-128">-Tag</span></span>
<span data-ttu-id="3879a-129">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="3879a-129">Resource tags</span></span>

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

### <span data-ttu-id="3879a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3879a-130">-Confirm</span></span>
<span data-ttu-id="3879a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3879a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3879a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3879a-132">-WhatIf</span></span>
<span data-ttu-id="3879a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3879a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3879a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3879a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3879a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3879a-135">CommonParameters</span></span>
<span data-ttu-id="3879a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3879a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3879a-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3879a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3879a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3879a-138">INPUTS</span></span>

### <span data-ttu-id="3879a-139">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="3879a-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="3879a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3879a-140">OUTPUTS</span></span>

### <span data-ttu-id="3879a-141">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="3879a-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="3879a-142">Note</span><span class="sxs-lookup"><span data-stu-id="3879a-142">NOTES</span></span>

<span data-ttu-id="3879a-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3879a-143">ALIASES</span></span>

<span data-ttu-id="3879a-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3879a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3879a-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3879a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3879a-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3879a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3879a-147">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3879a-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3879a-148">`[AssociationName <String>]`: Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="3879a-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="3879a-149">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="3879a-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3879a-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3879a-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3879a-151">`[ResourceProviderName <String>]`: Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="3879a-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="3879a-152">`[Scope <String>]`: L'ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="3879a-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="3879a-153">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="3879a-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="3879a-154">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="3879a-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="3879a-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3879a-155">RELATED LINKS</span></span>

