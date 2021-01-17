---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479259"
---
# <span data-ttu-id="e5e5a-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e5e5a-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="e5e5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e5a-103">Elimina l'HSM dedicato di Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="e5e5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5e5a-104">SYNTAX</span></span>

### <span data-ttu-id="e5e5a-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5e5a-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e5e5a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e5e5a-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5e5a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5e5a-107">DESCRIPTION</span></span>
<span data-ttu-id="e5e5a-108">Elimina l'HSM dedicato di Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="e5e5a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5e5a-109">EXAMPLES</span></span>

### <span data-ttu-id="e5e5a-110">Esempio 1: rimuovere un HSM dedicato per nome</span><span class="sxs-lookup"><span data-stu-id="e5e5a-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="e5e5a-111">Questo commnad rimuove un modulo HSM (hardware Security Module) per nome.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="e5e5a-112">Esempio 2: rimuovere un HSM dedicato per oggetto</span><span class="sxs-lookup"><span data-stu-id="e5e5a-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="e5e5a-113">Questo commnad rimuove un HSM dedicato per oggetto.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="e5e5a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5e5a-114">PARAMETERS</span></span>

### <span data-ttu-id="e5e5a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5e5a-115">-AsJob</span></span>
<span data-ttu-id="e5e5a-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e5e5a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e5e5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e5a-117">-DefaultProfile</span></span>
<span data-ttu-id="e5e5a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5e5a-119">-InputObject</span></span>
<span data-ttu-id="e5e5a-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5e5a-121">-Name</span></span>
<span data-ttu-id="e5e5a-122">Nome dell'HSM dedicato da eliminare</span><span class="sxs-lookup"><span data-stu-id="e5e5a-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="e5e5a-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="e5e5a-123">-NoWait</span></span>
<span data-ttu-id="e5e5a-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e5e5a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e5e5a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5e5a-125">-PassThru</span></span>
<span data-ttu-id="e5e5a-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="e5e5a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e5e5a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e5a-127">-ResourceGroupName</span></span>
<span data-ttu-id="e5e5a-128">Il nome del gruppo di risorse a cui appartiene l'HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="e5e5a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5e5a-129">-SubscriptionId</span></span>
<span data-ttu-id="e5e5a-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5e5a-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5e5a-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5e5a-132">-Confirm</span></span>
<span data-ttu-id="e5e5a-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5e5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e5a-134">-WhatIf</span></span>
<span data-ttu-id="e5e5a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5e5a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5e5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e5a-137">CommonParameters</span></span>
<span data-ttu-id="e5e5a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e5a-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5e5a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e5a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5e5a-140">INPUTS</span></span>

### <span data-ttu-id="e5e5a-141">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="e5e5a-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="e5e5a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5e5a-142">OUTPUTS</span></span>

### <span data-ttu-id="e5e5a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5e5a-143">System.Boolean</span></span>

## <span data-ttu-id="e5e5a-144">Note</span><span class="sxs-lookup"><span data-stu-id="e5e5a-144">NOTES</span></span>

<span data-ttu-id="e5e5a-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e5e5a-145">ALIASES</span></span>

<span data-ttu-id="e5e5a-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5e5a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5e5a-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5e5a-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5e5a-149">INPUTOBJECT <IDedicatedHsmIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e5e5a-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5e5a-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e5e5a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5e5a-151">`[Name <String>]`: Nome dell'HSM dedicato</span><span class="sxs-lookup"><span data-stu-id="e5e5a-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="e5e5a-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="e5e5a-153">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e5e5a-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e5e5a-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5e5a-155">RELATED LINKS</span></span>

