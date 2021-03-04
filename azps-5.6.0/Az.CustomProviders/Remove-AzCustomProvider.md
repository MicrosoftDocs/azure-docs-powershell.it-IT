---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: 87d04a30b5e04132f937d21b3585557efe71f4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998771"
---
# <span data-ttu-id="0a7c9-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="0a7c9-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="0a7c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7c9-103">Elimina il provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="0a7c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a7c9-104">SYNTAX</span></span>

### <span data-ttu-id="0a7c9-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a7c9-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0a7c9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a7c9-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a7c9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a7c9-107">DESCRIPTION</span></span>
<span data-ttu-id="0a7c9-108">Elimina il provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="0a7c9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a7c9-109">EXAMPLES</span></span>

### <span data-ttu-id="0a7c9-110">Esempio 1: Rimuovere un provider personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="0a7c9-111">Rimuovere un provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="0a7c9-111">Remove a custom provider</span></span>

### <span data-ttu-id="0a7c9-112">Esempio 2: Rimuovere un provider personalizzato con PassThru</span><span class="sxs-lookup"><span data-stu-id="0a7c9-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="0a7c9-113">Rimuovere un provider personalizzato usando la caratteristica PassThru per indicare un'operazione riuscita o non riuscita.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="0a7c9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a7c9-114">PARAMETERS</span></span>

### <span data-ttu-id="0a7c9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a7c9-115">-AsJob</span></span>
<span data-ttu-id="0a7c9-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="0a7c9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0a7c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7c9-117">-DefaultProfile</span></span>
<span data-ttu-id="0a7c9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a7c9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a7c9-119">-InputObject</span></span>
<span data-ttu-id="0a7c9-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7c9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0a7c9-121">-Name</span></span>
<span data-ttu-id="0a7c9-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7c9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0a7c9-123">-NoWait</span></span>
<span data-ttu-id="0a7c9-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="0a7c9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a7c9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a7c9-125">-PassThru</span></span>
<span data-ttu-id="0a7c9-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="0a7c9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0a7c9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a7c9-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a7c9-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7c9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a7c9-129">-SubscriptionId</span></span>
<span data-ttu-id="0a7c9-130">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-130">The Azure subscription ID.</span></span>
<span data-ttu-id="0a7c9-131">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-000000000000000.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7c9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a7c9-132">-Confirm</span></span>
<span data-ttu-id="0a7c9-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a7c9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a7c9-134">-WhatIf</span></span>
<span data-ttu-id="0a7c9-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a7c9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a7c9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7c9-137">CommonParameters</span></span>
<span data-ttu-id="0a7c9-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7c9-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7c9-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a7c9-140">INPUTS</span></span>

### <span data-ttu-id="0a7c9-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="0a7c9-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="0a7c9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a7c9-142">OUTPUTS</span></span>

### <span data-ttu-id="0a7c9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a7c9-143">System.Boolean</span></span>

## <span data-ttu-id="0a7c9-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a7c9-144">NOTES</span></span>

<span data-ttu-id="0a7c9-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0a7c9-145">ALIASES</span></span>

<span data-ttu-id="0a7c9-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0a7c9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a7c9-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a7c9-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a7c9-149">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0a7c9-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a7c9-150">`[AssociationName <String>]`: nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="0a7c9-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0a7c9-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a7c9-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0a7c9-153">`[ResourceProviderName <String>]`: nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="0a7c9-154">`[Scope <String>]`: ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="0a7c9-155">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="0a7c9-156">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-000000000000000.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="0a7c9-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a7c9-157">RELATED LINKS</span></span>

