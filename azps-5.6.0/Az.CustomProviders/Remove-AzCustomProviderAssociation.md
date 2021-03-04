---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 6d3a6863044722be49efb78a71e3e0fbe82db5e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998757"
---
# <span data-ttu-id="c0b5d-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="c0b5d-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="c0b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b5d-103">Eliminare un'associazione.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-103">Delete an association.</span></span>

## <span data-ttu-id="c0b5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0b5d-104">SYNTAX</span></span>

### <span data-ttu-id="c0b5d-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0b5d-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0b5d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c0b5d-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0b5d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c0b5d-107">DESCRIPTION</span></span>
<span data-ttu-id="c0b5d-108">Eliminare un'associazione.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-108">Delete an association.</span></span>

## <span data-ttu-id="c0b5d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0b5d-109">EXAMPLES</span></span>

### <span data-ttu-id="c0b5d-110">Esempio 1: Rimuovere un'associazione di provider personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="c0b5d-111">Rimuovere un'associazione di provider personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="c0b5d-112">Esempio 2: Rimuovere un'associazione di provider personalizzata con Piping</span><span class="sxs-lookup"><span data-stu-id="c0b5d-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="c0b5d-113">Rimuovere un'associazione di provider personalizzata, usando i piping e la caratteristica PassThru per indicare un'operazione riuscita o non riuscita.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="c0b5d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0b5d-114">PARAMETERS</span></span>

### <span data-ttu-id="c0b5d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0b5d-115">-AsJob</span></span>
<span data-ttu-id="c0b5d-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c0b5d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c0b5d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b5d-117">-DefaultProfile</span></span>
<span data-ttu-id="c0b5d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0b5d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0b5d-119">-InputObject</span></span>
<span data-ttu-id="c0b5d-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c0b5d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c0b5d-121">-Name</span></span>
<span data-ttu-id="c0b5d-122">Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b5d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0b5d-123">-NoWait</span></span>
<span data-ttu-id="c0b5d-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c0b5d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c0b5d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0b5d-125">-PassThru</span></span>
<span data-ttu-id="c0b5d-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="c0b5d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c0b5d-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="c0b5d-127">-Scope</span></span>
<span data-ttu-id="c0b5d-128">Ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-128">The scope of the association.</span></span>

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

### <span data-ttu-id="c0b5d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0b5d-129">-Confirm</span></span>
<span data-ttu-id="c0b5d-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0b5d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b5d-131">-WhatIf</span></span>
<span data-ttu-id="c0b5d-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0b5d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0b5d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b5d-134">CommonParameters</span></span>
<span data-ttu-id="c0b5d-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b5d-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b5d-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="c0b5d-137">INPUTS</span></span>

### <span data-ttu-id="c0b5d-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="c0b5d-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="c0b5d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0b5d-139">OUTPUTS</span></span>

### <span data-ttu-id="c0b5d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0b5d-140">System.Boolean</span></span>

## <span data-ttu-id="c0b5d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="c0b5d-141">NOTES</span></span>

<span data-ttu-id="c0b5d-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c0b5d-142">ALIASES</span></span>

<span data-ttu-id="c0b5d-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="c0b5d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0b5d-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0b5d-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0b5d-146">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c0b5d-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c0b5d-147">`[AssociationName <String>]`: nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="c0b5d-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="c0b5d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0b5d-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c0b5d-150">`[ResourceProviderName <String>]`: nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="c0b5d-151">`[Scope <String>]`: ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="c0b5d-152">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="c0b5d-153">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-000000000000000.</span><span class="sxs-lookup"><span data-stu-id="c0b5d-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="c0b5d-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0b5d-154">RELATED LINKS</span></span>

