---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186039"
---
# <span data-ttu-id="da502-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="da502-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="da502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da502-102">SYNOPSIS</span></span>
<span data-ttu-id="da502-103">Rimuovere una userSession.</span><span class="sxs-lookup"><span data-stu-id="da502-103">Remove a userSession.</span></span>

## <span data-ttu-id="da502-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da502-104">SYNTAX</span></span>

### <span data-ttu-id="da502-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da502-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da502-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da502-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da502-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da502-107">DESCRIPTION</span></span>
<span data-ttu-id="da502-108">Rimuovere una userSession.</span><span class="sxs-lookup"><span data-stu-id="da502-108">Remove a userSession.</span></span>

## <span data-ttu-id="da502-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da502-109">EXAMPLES</span></span>

### <span data-ttu-id="da502-110">Esempio 1: Eliminare una UserSession di Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="da502-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="da502-111">Questo comando elimina una UserSession di Desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="da502-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="da502-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da502-112">PARAMETERS</span></span>

### <span data-ttu-id="da502-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da502-113">-DefaultProfile</span></span>
<span data-ttu-id="da502-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da502-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da502-115">-Force</span><span class="sxs-lookup"><span data-stu-id="da502-115">-Force</span></span>
<span data-ttu-id="da502-116">Forzare il contrassegno a disconnettersi da userSession.</span><span class="sxs-lookup"><span data-stu-id="da502-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="da502-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="da502-117">-HostPoolName</span></span>
<span data-ttu-id="da502-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="da502-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="da502-119">-Id</span><span class="sxs-lookup"><span data-stu-id="da502-119">-Id</span></span>
<span data-ttu-id="da502-120">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="da502-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da502-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da502-121">-InputObject</span></span>
<span data-ttu-id="da502-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="da502-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="da502-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da502-123">-PassThru</span></span>
<span data-ttu-id="da502-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="da502-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="da502-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da502-125">-ResourceGroupName</span></span>
<span data-ttu-id="da502-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da502-126">The name of the resource group.</span></span>
<span data-ttu-id="da502-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="da502-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="da502-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="da502-128">-SessionHostName</span></span>
<span data-ttu-id="da502-129">Nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="da502-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="da502-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da502-130">-SubscriptionId</span></span>
<span data-ttu-id="da502-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="da502-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="da502-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da502-132">-Confirm</span></span>
<span data-ttu-id="da502-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da502-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da502-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da502-134">-WhatIf</span></span>
<span data-ttu-id="da502-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da502-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da502-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da502-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da502-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da502-137">CommonParameters</span></span>
<span data-ttu-id="da502-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da502-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da502-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da502-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da502-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="da502-140">INPUTS</span></span>

### <span data-ttu-id="da502-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="da502-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="da502-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da502-142">OUTPUTS</span></span>

### <span data-ttu-id="da502-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da502-143">System.Boolean</span></span>

## <span data-ttu-id="da502-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="da502-144">NOTES</span></span>

<span data-ttu-id="da502-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da502-145">ALIASES</span></span>

<span data-ttu-id="da502-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="da502-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da502-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="da502-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da502-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da502-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da502-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="da502-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da502-150">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="da502-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="da502-151">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="da502-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="da502-152">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="da502-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="da502-153">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="da502-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="da502-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="da502-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da502-155">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="da502-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="da502-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da502-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="da502-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="da502-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="da502-158">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="da502-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="da502-159">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="da502-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="da502-160">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="da502-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="da502-161">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="da502-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="da502-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da502-162">RELATED LINKS</span></span>

