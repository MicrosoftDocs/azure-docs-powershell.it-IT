---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193016"
---
# <span data-ttu-id="173cb-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="173cb-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="173cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="173cb-102">SYNOPSIS</span></span>
<span data-ttu-id="173cb-103">Elimina il provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="173cb-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="173cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="173cb-104">SYNTAX</span></span>

### <span data-ttu-id="173cb-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="173cb-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="173cb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="173cb-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="173cb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="173cb-107">DESCRIPTION</span></span>
<span data-ttu-id="173cb-108">Elimina il provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="173cb-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="173cb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="173cb-109">EXAMPLES</span></span>

### <span data-ttu-id="173cb-110">Esempio 1: rimuovere un provider personalizzato.</span><span class="sxs-lookup"><span data-stu-id="173cb-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="173cb-111">Rimuovere un provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="173cb-111">Remove a custom provider</span></span>

### <span data-ttu-id="173cb-112">Esempio 2: rimuovere un provider personalizzato con PassThru</span><span class="sxs-lookup"><span data-stu-id="173cb-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="173cb-113">Rimuovere un provider personalizzato usando la caratteristica PassThru per indicare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="173cb-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="173cb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="173cb-114">PARAMETERS</span></span>

### <span data-ttu-id="173cb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="173cb-115">-AsJob</span></span>
<span data-ttu-id="173cb-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="173cb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="173cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="173cb-117">-DefaultProfile</span></span>
<span data-ttu-id="173cb-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="173cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="173cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="173cb-119">-InputObject</span></span>
<span data-ttu-id="173cb-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="173cb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="173cb-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="173cb-121">-Name</span></span>
<span data-ttu-id="173cb-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="173cb-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="173cb-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="173cb-123">-NoWait</span></span>
<span data-ttu-id="173cb-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="173cb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="173cb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="173cb-125">-PassThru</span></span>
<span data-ttu-id="173cb-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="173cb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="173cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="173cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="173cb-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="173cb-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="173cb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="173cb-129">-SubscriptionId</span></span>
<span data-ttu-id="173cb-130">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="173cb-130">The Azure subscription ID.</span></span>
<span data-ttu-id="173cb-131">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="173cb-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="173cb-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="173cb-132">-Confirm</span></span>
<span data-ttu-id="173cb-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="173cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="173cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="173cb-134">-WhatIf</span></span>
<span data-ttu-id="173cb-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="173cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="173cb-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="173cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="173cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="173cb-137">CommonParameters</span></span>
<span data-ttu-id="173cb-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="173cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="173cb-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="173cb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="173cb-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="173cb-140">INPUTS</span></span>

### <span data-ttu-id="173cb-141">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="173cb-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="173cb-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="173cb-142">OUTPUTS</span></span>

### <span data-ttu-id="173cb-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="173cb-143">System.Boolean</span></span>

## <span data-ttu-id="173cb-144">Note</span><span class="sxs-lookup"><span data-stu-id="173cb-144">NOTES</span></span>

<span data-ttu-id="173cb-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="173cb-145">ALIASES</span></span>

<span data-ttu-id="173cb-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="173cb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="173cb-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="173cb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="173cb-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="173cb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="173cb-149">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="173cb-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="173cb-150">`[AssociationName <String>]`: Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="173cb-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="173cb-151">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="173cb-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="173cb-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="173cb-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="173cb-153">`[ResourceProviderName <String>]`: Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="173cb-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="173cb-154">`[Scope <String>]`: L'ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="173cb-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="173cb-155">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="173cb-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="173cb-156">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="173cb-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="173cb-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="173cb-157">RELATED LINKS</span></span>
