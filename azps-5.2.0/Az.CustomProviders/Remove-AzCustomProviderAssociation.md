---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330748"
---
# <span data-ttu-id="ca563-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="ca563-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="ca563-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca563-102">SYNOPSIS</span></span>
<span data-ttu-id="ca563-103">Eliminare un'associazione.</span><span class="sxs-lookup"><span data-stu-id="ca563-103">Delete an association.</span></span>

## <span data-ttu-id="ca563-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca563-104">SYNTAX</span></span>

### <span data-ttu-id="ca563-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca563-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca563-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca563-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca563-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca563-107">DESCRIPTION</span></span>
<span data-ttu-id="ca563-108">Eliminare un'associazione.</span><span class="sxs-lookup"><span data-stu-id="ca563-108">Delete an association.</span></span>

## <span data-ttu-id="ca563-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca563-109">EXAMPLES</span></span>

### <span data-ttu-id="ca563-110">Esempio 1: rimuovere un'associazione di provider personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ca563-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="ca563-111">Rimuovere un'associazione di provider personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ca563-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="ca563-112">Esempio 2: rimuovere un'associazione di provider personalizzata con piping</span><span class="sxs-lookup"><span data-stu-id="ca563-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="ca563-113">Rimuovere un'associazione di provider personalizzata utilizzando piping e la caratteristica PassThru per indicare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ca563-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="ca563-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca563-114">PARAMETERS</span></span>

### <span data-ttu-id="ca563-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca563-115">-AsJob</span></span>
<span data-ttu-id="ca563-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ca563-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ca563-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca563-117">-DefaultProfile</span></span>
<span data-ttu-id="ca563-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca563-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca563-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca563-119">-InputObject</span></span>
<span data-ttu-id="ca563-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ca563-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca563-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca563-121">-Name</span></span>
<span data-ttu-id="ca563-122">Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="ca563-122">The name of the association.</span></span>

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

### <span data-ttu-id="ca563-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ca563-123">-NoWait</span></span>
<span data-ttu-id="ca563-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ca563-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ca563-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca563-125">-PassThru</span></span>
<span data-ttu-id="ca563-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="ca563-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ca563-127">-Ambito</span><span class="sxs-lookup"><span data-stu-id="ca563-127">-Scope</span></span>
<span data-ttu-id="ca563-128">Ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="ca563-128">The scope of the association.</span></span>

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

### <span data-ttu-id="ca563-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca563-129">-Confirm</span></span>
<span data-ttu-id="ca563-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca563-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca563-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca563-131">-WhatIf</span></span>
<span data-ttu-id="ca563-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca563-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca563-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca563-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca563-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca563-134">CommonParameters</span></span>
<span data-ttu-id="ca563-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca563-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca563-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca563-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca563-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca563-137">INPUTS</span></span>

### <span data-ttu-id="ca563-138">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="ca563-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="ca563-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca563-139">OUTPUTS</span></span>

### <span data-ttu-id="ca563-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca563-140">System.Boolean</span></span>

## <span data-ttu-id="ca563-141">Note</span><span class="sxs-lookup"><span data-stu-id="ca563-141">NOTES</span></span>

<span data-ttu-id="ca563-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ca563-142">ALIASES</span></span>

<span data-ttu-id="ca563-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca563-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca563-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ca563-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca563-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca563-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca563-146">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ca563-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca563-147">`[AssociationName <String>]`: Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="ca563-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="ca563-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ca563-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca563-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca563-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ca563-150">`[ResourceProviderName <String>]`: Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca563-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="ca563-151">`[Scope <String>]`: L'ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="ca563-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="ca563-152">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="ca563-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="ca563-153">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="ca563-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="ca563-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca563-154">RELATED LINKS</span></span>

