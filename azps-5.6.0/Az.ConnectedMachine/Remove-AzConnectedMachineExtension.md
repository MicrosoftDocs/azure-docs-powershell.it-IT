---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: 777c02f6588d7c1fdb1a1d6e9e9c004f51694293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012366"
---
# <span data-ttu-id="be17e-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="be17e-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="be17e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be17e-102">SYNOPSIS</span></span>
<span data-ttu-id="be17e-103">Operazione per eliminare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="be17e-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="be17e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be17e-104">SYNTAX</span></span>

### <span data-ttu-id="be17e-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be17e-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="be17e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="be17e-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be17e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be17e-107">DESCRIPTION</span></span>
<span data-ttu-id="be17e-108">Operazione per eliminare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="be17e-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="be17e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be17e-109">EXAMPLES</span></span>

### <span data-ttu-id="be17e-110">Esempio 1: Rimuovere un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="be17e-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="be17e-111">Elimina l'estensione nel computer.</span><span class="sxs-lookup"><span data-stu-id="be17e-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="be17e-112">Esempio 2: Rimuovere l'estensione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="be17e-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="be17e-113">Rimuove tutte le estensioni nel computer specificato.</span><span class="sxs-lookup"><span data-stu-id="be17e-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="be17e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be17e-114">PARAMETERS</span></span>

### <span data-ttu-id="be17e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be17e-115">-AsJob</span></span>
<span data-ttu-id="be17e-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="be17e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="be17e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be17e-117">-DefaultProfile</span></span>
<span data-ttu-id="be17e-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be17e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be17e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be17e-119">-InputObject</span></span>
<span data-ttu-id="be17e-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="be17e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be17e-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="be17e-121">-MachineName</span></span>
<span data-ttu-id="be17e-122">Nome del computer in cui deve essere eliminata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="be17e-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="be17e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="be17e-123">-Name</span></span>
<span data-ttu-id="be17e-124">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="be17e-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="be17e-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be17e-125">-NoWait</span></span>
<span data-ttu-id="be17e-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="be17e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="be17e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be17e-127">-PassThru</span></span>
<span data-ttu-id="be17e-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="be17e-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="be17e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be17e-129">-ResourceGroupName</span></span>
<span data-ttu-id="be17e-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="be17e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="be17e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be17e-131">-SubscriptionId</span></span>
<span data-ttu-id="be17e-132">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be17e-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="be17e-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="be17e-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="be17e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be17e-134">-Confirm</span></span>
<span data-ttu-id="be17e-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be17e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be17e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be17e-136">-WhatIf</span></span>
<span data-ttu-id="be17e-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be17e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be17e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be17e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be17e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be17e-139">CommonParameters</span></span>
<span data-ttu-id="be17e-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be17e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be17e-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be17e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be17e-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="be17e-142">INPUTS</span></span>

### <span data-ttu-id="be17e-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="be17e-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="be17e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be17e-144">OUTPUTS</span></span>

### <span data-ttu-id="be17e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be17e-145">System.Boolean</span></span>

## <span data-ttu-id="be17e-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="be17e-146">NOTES</span></span>

<span data-ttu-id="be17e-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="be17e-147">ALIASES</span></span>

<span data-ttu-id="be17e-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="be17e-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be17e-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="be17e-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be17e-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be17e-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be17e-151">INPUTOBJECT <IConnectedMachineIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="be17e-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be17e-152">`[ExtensionName <String>]`: nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="be17e-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="be17e-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="be17e-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be17e-154">`[Name <String>]`: nome del computer ibrido.</span><span class="sxs-lookup"><span data-stu-id="be17e-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="be17e-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="be17e-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="be17e-156">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be17e-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="be17e-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="be17e-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="be17e-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be17e-158">RELATED LINKS</span></span>

