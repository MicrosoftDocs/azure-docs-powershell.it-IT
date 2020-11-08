---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032558"
---
# <span data-ttu-id="b9732-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="b9732-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="b9732-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9732-102">SYNOPSIS</span></span>
<span data-ttu-id="b9732-103">Operazione per eliminare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="b9732-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="b9732-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9732-104">SYNTAX</span></span>

### <span data-ttu-id="b9732-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9732-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b9732-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9732-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9732-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9732-107">DESCRIPTION</span></span>
<span data-ttu-id="b9732-108">Operazione per eliminare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="b9732-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="b9732-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9732-109">EXAMPLES</span></span>

### <span data-ttu-id="b9732-110">Esempio 1: rimuovere un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="b9732-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="b9732-111">Elimina l'estensione nel computer.</span><span class="sxs-lookup"><span data-stu-id="b9732-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="b9732-112">Esempio 2: rimuovere l'estensione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="b9732-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="b9732-113">Rimuove tutte le estensioni nel computer specificato.</span><span class="sxs-lookup"><span data-stu-id="b9732-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="b9732-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9732-114">PARAMETERS</span></span>

### <span data-ttu-id="b9732-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9732-115">-AsJob</span></span>
<span data-ttu-id="b9732-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b9732-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b9732-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9732-117">-DefaultProfile</span></span>
<span data-ttu-id="b9732-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9732-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9732-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9732-119">-InputObject</span></span>
<span data-ttu-id="b9732-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b9732-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9732-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="b9732-121">-MachineName</span></span>
<span data-ttu-id="b9732-122">Il nome del computer in cui deve essere eliminata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="b9732-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="b9732-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9732-123">-Name</span></span>
<span data-ttu-id="b9732-124">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="b9732-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="b9732-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="b9732-125">-NoWait</span></span>
<span data-ttu-id="b9732-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b9732-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9732-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9732-127">-PassThru</span></span>
<span data-ttu-id="b9732-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="b9732-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b9732-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9732-129">-ResourceGroupName</span></span>
<span data-ttu-id="b9732-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b9732-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9732-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9732-131">-SubscriptionId</span></span>
<span data-ttu-id="b9732-132">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9732-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9732-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b9732-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b9732-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9732-134">-Confirm</span></span>
<span data-ttu-id="b9732-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9732-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9732-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9732-136">-WhatIf</span></span>
<span data-ttu-id="b9732-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9732-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9732-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9732-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9732-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9732-139">CommonParameters</span></span>
<span data-ttu-id="b9732-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9732-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9732-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9732-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9732-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9732-142">INPUTS</span></span>

### <span data-ttu-id="b9732-143">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="b9732-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="b9732-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9732-144">OUTPUTS</span></span>

### <span data-ttu-id="b9732-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9732-145">System.Boolean</span></span>

## <span data-ttu-id="b9732-146">Note</span><span class="sxs-lookup"><span data-stu-id="b9732-146">NOTES</span></span>

<span data-ttu-id="b9732-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b9732-147">ALIASES</span></span>

<span data-ttu-id="b9732-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9732-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9732-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b9732-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9732-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9732-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9732-151">INPUTOBJECT <IConnectedMachineIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b9732-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9732-152">`[ExtensionName <String>]`: Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="b9732-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="b9732-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="b9732-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9732-154">`[Name <String>]`: Nome della macchina ibrida.</span><span class="sxs-lookup"><span data-stu-id="b9732-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="b9732-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b9732-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b9732-156">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9732-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b9732-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b9732-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b9732-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9732-158">RELATED LINKS</span></span>

