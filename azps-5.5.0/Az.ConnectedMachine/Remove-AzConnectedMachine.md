---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209914"
---
# <span data-ttu-id="94b37-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="94b37-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="94b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94b37-102">SYNOPSIS</span></span>
<span data-ttu-id="94b37-103">Operazione per rimuovere un'identità di computer ibrida in Azure.</span><span class="sxs-lookup"><span data-stu-id="94b37-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="94b37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94b37-104">SYNTAX</span></span>

### <span data-ttu-id="94b37-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94b37-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94b37-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94b37-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94b37-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94b37-107">DESCRIPTION</span></span>
<span data-ttu-id="94b37-108">Operazione per rimuovere un'identità di computer ibrida in Azure.</span><span class="sxs-lookup"><span data-stu-id="94b37-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="94b37-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94b37-109">EXAMPLES</span></span>

### <span data-ttu-id="94b37-110">Esempio 1: Rimuovere un computer connesso</span><span class="sxs-lookup"><span data-stu-id="94b37-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="94b37-111">Elimina il computer connesso.</span><span class="sxs-lookup"><span data-stu-id="94b37-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="94b37-112">Esempio 2: Rimuovere i computer connessi tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="94b37-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="94b37-113">Rimuove tutti i computer nel `contoso-connected-machines` gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94b37-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="94b37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94b37-114">PARAMETERS</span></span>

### <span data-ttu-id="94b37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b37-115">-DefaultProfile</span></span>
<span data-ttu-id="94b37-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94b37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94b37-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94b37-117">-InputObject</span></span>
<span data-ttu-id="94b37-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="94b37-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94b37-119">-Name</span><span class="sxs-lookup"><span data-stu-id="94b37-119">-Name</span></span>
<span data-ttu-id="94b37-120">Nome del computer ibrido.</span><span class="sxs-lookup"><span data-stu-id="94b37-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="94b37-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94b37-121">-PassThru</span></span>
<span data-ttu-id="94b37-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="94b37-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="94b37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b37-123">-ResourceGroupName</span></span>
<span data-ttu-id="94b37-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94b37-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="94b37-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94b37-125">-SubscriptionId</span></span>
<span data-ttu-id="94b37-126">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94b37-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94b37-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="94b37-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94b37-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94b37-128">-Confirm</span></span>
<span data-ttu-id="94b37-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94b37-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b37-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b37-130">-WhatIf</span></span>
<span data-ttu-id="94b37-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94b37-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94b37-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94b37-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b37-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b37-133">CommonParameters</span></span>
<span data-ttu-id="94b37-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b37-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b37-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94b37-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b37-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="94b37-136">INPUTS</span></span>

### <span data-ttu-id="94b37-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="94b37-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="94b37-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94b37-138">OUTPUTS</span></span>

### <span data-ttu-id="94b37-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94b37-139">System.Boolean</span></span>

## <span data-ttu-id="94b37-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="94b37-140">NOTES</span></span>

<span data-ttu-id="94b37-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="94b37-141">ALIASES</span></span>

<span data-ttu-id="94b37-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="94b37-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94b37-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="94b37-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94b37-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94b37-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94b37-145">INPUTOBJECT <IConnectedMachineIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="94b37-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94b37-146">`[ExtensionName <String>]`: nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="94b37-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="94b37-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="94b37-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94b37-148">`[Name <String>]`: nome del computer ibrido.</span><span class="sxs-lookup"><span data-stu-id="94b37-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="94b37-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94b37-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="94b37-150">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94b37-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="94b37-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="94b37-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94b37-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94b37-152">RELATED LINKS</span></span>

