---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 682f59c5c07643ecd93fd1ae051abc8e74c4e185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980478"
---
# <span data-ttu-id="6d093-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="6d093-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="6d093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d093-102">SYNOPSIS</span></span>
<span data-ttu-id="6d093-103">Rimuovere un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6d093-103">Remove a workspace.</span></span>

## <span data-ttu-id="6d093-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d093-104">SYNTAX</span></span>

### <span data-ttu-id="6d093-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d093-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d093-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d093-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d093-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d093-107">DESCRIPTION</span></span>
<span data-ttu-id="6d093-108">Rimuovere un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6d093-108">Remove a workspace.</span></span>

## <span data-ttu-id="6d093-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d093-109">EXAMPLES</span></span>

### <span data-ttu-id="6d093-110">Esempio 1: Eliminare un'area di lavoro desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="6d093-110">Example 1: Delete a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="6d093-111">Questo comando elimina un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d093-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="6d093-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d093-112">PARAMETERS</span></span>

### <span data-ttu-id="6d093-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d093-113">-DefaultProfile</span></span>
<span data-ttu-id="6d093-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d093-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d093-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d093-115">-InputObject</span></span>
<span data-ttu-id="6d093-116">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6d093-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d093-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6d093-117">-Name</span></span>
<span data-ttu-id="6d093-118">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="6d093-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d093-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d093-119">-PassThru</span></span>
<span data-ttu-id="6d093-120">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="6d093-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6d093-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d093-121">-ResourceGroupName</span></span>
<span data-ttu-id="6d093-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d093-122">The name of the resource group.</span></span>
<span data-ttu-id="6d093-123">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6d093-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6d093-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d093-124">-SubscriptionId</span></span>
<span data-ttu-id="6d093-125">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6d093-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6d093-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d093-126">-Confirm</span></span>
<span data-ttu-id="6d093-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d093-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d093-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d093-128">-WhatIf</span></span>
<span data-ttu-id="6d093-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d093-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d093-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d093-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d093-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d093-131">CommonParameters</span></span>
<span data-ttu-id="6d093-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d093-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d093-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d093-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d093-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d093-134">INPUTS</span></span>

### <span data-ttu-id="6d093-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6d093-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6d093-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d093-136">OUTPUTS</span></span>

### <span data-ttu-id="6d093-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d093-137">System.Boolean</span></span>

## <span data-ttu-id="6d093-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d093-138">NOTES</span></span>

<span data-ttu-id="6d093-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6d093-139">ALIASES</span></span>

<span data-ttu-id="6d093-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="6d093-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d093-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6d093-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d093-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d093-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d093-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6d093-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d093-144">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="6d093-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6d093-145">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="6d093-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6d093-146">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="6d093-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6d093-147">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="6d093-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6d093-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6d093-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d093-149">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="6d093-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="6d093-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d093-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6d093-151">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6d093-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="6d093-152">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="6d093-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6d093-153">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6d093-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6d093-154">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="6d093-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6d093-155">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="6d093-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6d093-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d093-156">RELATED LINKS</span></span>

