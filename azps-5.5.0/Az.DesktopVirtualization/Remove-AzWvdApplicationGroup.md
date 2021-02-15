---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204235"
---
# <span data-ttu-id="2341e-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="2341e-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="2341e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2341e-102">SYNOPSIS</span></span>
<span data-ttu-id="2341e-103">Rimuovere un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="2341e-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="2341e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2341e-104">SYNTAX</span></span>

### <span data-ttu-id="2341e-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2341e-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2341e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2341e-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2341e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2341e-107">DESCRIPTION</span></span>
<span data-ttu-id="2341e-108">Rimuovere un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="2341e-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="2341e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2341e-109">EXAMPLES</span></span>

### <span data-ttu-id="2341e-110">Esempio 1: Eliminare un gruppo applicazioni desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="2341e-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="2341e-111">Questo comando elimina un gruppo di applicazioni desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2341e-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="2341e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2341e-112">PARAMETERS</span></span>

### <span data-ttu-id="2341e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2341e-113">-DefaultProfile</span></span>
<span data-ttu-id="2341e-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2341e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2341e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2341e-115">-InputObject</span></span>
<span data-ttu-id="2341e-116">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2341e-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2341e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2341e-117">-Name</span></span>
<span data-ttu-id="2341e-118">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="2341e-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2341e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2341e-119">-PassThru</span></span>
<span data-ttu-id="2341e-120">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="2341e-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2341e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2341e-121">-ResourceGroupName</span></span>
<span data-ttu-id="2341e-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2341e-122">The name of the resource group.</span></span>
<span data-ttu-id="2341e-123">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2341e-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2341e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2341e-124">-SubscriptionId</span></span>
<span data-ttu-id="2341e-125">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2341e-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2341e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2341e-126">-Confirm</span></span>
<span data-ttu-id="2341e-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2341e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2341e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2341e-128">-WhatIf</span></span>
<span data-ttu-id="2341e-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2341e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2341e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2341e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2341e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2341e-131">CommonParameters</span></span>
<span data-ttu-id="2341e-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2341e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2341e-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2341e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2341e-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2341e-134">INPUTS</span></span>

### <span data-ttu-id="2341e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2341e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2341e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2341e-136">OUTPUTS</span></span>

### <span data-ttu-id="2341e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2341e-137">System.Boolean</span></span>

## <span data-ttu-id="2341e-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="2341e-138">NOTES</span></span>

<span data-ttu-id="2341e-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2341e-139">ALIASES</span></span>

<span data-ttu-id="2341e-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2341e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2341e-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2341e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2341e-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2341e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2341e-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="2341e-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2341e-144">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="2341e-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2341e-145">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="2341e-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2341e-146">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="2341e-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2341e-147">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="2341e-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2341e-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="2341e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2341e-149">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="2341e-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="2341e-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2341e-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2341e-151">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2341e-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="2341e-152">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="2341e-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2341e-153">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2341e-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2341e-154">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="2341e-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2341e-155">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="2341e-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2341e-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2341e-156">RELATED LINKS</span></span>

