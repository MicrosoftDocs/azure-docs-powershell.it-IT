---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202200"
---
# <span data-ttu-id="43ad3-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="43ad3-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="43ad3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="43ad3-103">Operazione per rimuovere un'identità di computer ibrida in Azure.</span><span class="sxs-lookup"><span data-stu-id="43ad3-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="43ad3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43ad3-104">SYNTAX</span></span>

### <span data-ttu-id="43ad3-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43ad3-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43ad3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43ad3-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43ad3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43ad3-107">DESCRIPTION</span></span>
<span data-ttu-id="43ad3-108">Operazione per rimuovere un'identità di computer ibrida in Azure.</span><span class="sxs-lookup"><span data-stu-id="43ad3-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="43ad3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43ad3-109">EXAMPLES</span></span>

### <span data-ttu-id="43ad3-110">Esempio 1: rimuovere un computer connesso</span><span class="sxs-lookup"><span data-stu-id="43ad3-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="43ad3-111">Elimina il computer connesso.</span><span class="sxs-lookup"><span data-stu-id="43ad3-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="43ad3-112">Esempio 2: rimuovere i computer connessi tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="43ad3-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="43ad3-113">Rimuove tutti i computer nel `contoso-connected-machines` gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="43ad3-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="43ad3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43ad3-114">PARAMETERS</span></span>

### <span data-ttu-id="43ad3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ad3-115">-DefaultProfile</span></span>
<span data-ttu-id="43ad3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43ad3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ad3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43ad3-117">-InputObject</span></span>
<span data-ttu-id="43ad3-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="43ad3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43ad3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="43ad3-119">-Name</span></span>
<span data-ttu-id="43ad3-120">Nome della macchina ibrida.</span><span class="sxs-lookup"><span data-stu-id="43ad3-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="43ad3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43ad3-121">-PassThru</span></span>
<span data-ttu-id="43ad3-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="43ad3-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="43ad3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ad3-123">-ResourceGroupName</span></span>
<span data-ttu-id="43ad3-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43ad3-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="43ad3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43ad3-125">-SubscriptionId</span></span>
<span data-ttu-id="43ad3-126">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="43ad3-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="43ad3-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="43ad3-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="43ad3-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43ad3-128">-Confirm</span></span>
<span data-ttu-id="43ad3-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ad3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ad3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ad3-130">-WhatIf</span></span>
<span data-ttu-id="43ad3-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43ad3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ad3-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43ad3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ad3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ad3-133">CommonParameters</span></span>
<span data-ttu-id="43ad3-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ad3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ad3-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43ad3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ad3-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43ad3-136">INPUTS</span></span>

### <span data-ttu-id="43ad3-137">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="43ad3-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="43ad3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43ad3-138">OUTPUTS</span></span>

### <span data-ttu-id="43ad3-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43ad3-139">System.Boolean</span></span>

## <span data-ttu-id="43ad3-140">Note</span><span class="sxs-lookup"><span data-stu-id="43ad3-140">NOTES</span></span>

<span data-ttu-id="43ad3-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="43ad3-141">ALIASES</span></span>

<span data-ttu-id="43ad3-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43ad3-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43ad3-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="43ad3-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43ad3-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43ad3-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43ad3-145">INPUTOBJECT <IConnectedMachineIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="43ad3-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43ad3-146">`[ExtensionName <String>]`: Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="43ad3-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="43ad3-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="43ad3-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43ad3-148">`[Name <String>]`: Nome della macchina ibrida.</span><span class="sxs-lookup"><span data-stu-id="43ad3-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="43ad3-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43ad3-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="43ad3-150">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="43ad3-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="43ad3-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="43ad3-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="43ad3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43ad3-152">RELATED LINKS</span></span>

