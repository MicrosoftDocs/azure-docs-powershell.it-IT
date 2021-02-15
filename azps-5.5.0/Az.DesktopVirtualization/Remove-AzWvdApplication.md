---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c65fd55599a78bbaa558ba7ec8efa94fdc3b40e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204242"
---
# <span data-ttu-id="4a474-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="4a474-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="4a474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a474-102">SYNOPSIS</span></span>
<span data-ttu-id="4a474-103">Rimuovere un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a474-103">Remove an application.</span></span>

## <span data-ttu-id="4a474-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a474-104">SYNTAX</span></span>

### <span data-ttu-id="4a474-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a474-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a474-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a474-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a474-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4a474-107">DESCRIPTION</span></span>
<span data-ttu-id="4a474-108">Rimuovere un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a474-108">Remove an application.</span></span>

## <span data-ttu-id="4a474-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a474-109">EXAMPLES</span></span>

### <span data-ttu-id="4a474-110">Esempio 1: Eliminare un'applicazione Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="4a474-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="4a474-111">Questo comando elimina un'applicazione Desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="4a474-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="4a474-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a474-112">PARAMETERS</span></span>

### <span data-ttu-id="4a474-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a474-113">-DefaultProfile</span></span>
<span data-ttu-id="4a474-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a474-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a474-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="4a474-115">-GroupName</span></span>
<span data-ttu-id="4a474-116">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="4a474-116">The name of the application group</span></span>

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

### <span data-ttu-id="4a474-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a474-117">-InputObject</span></span>
<span data-ttu-id="4a474-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4a474-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a474-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4a474-119">-Name</span></span>
<span data-ttu-id="4a474-120">Nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="4a474-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a474-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a474-121">-PassThru</span></span>
<span data-ttu-id="4a474-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="4a474-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a474-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a474-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a474-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a474-124">The name of the resource group.</span></span>
<span data-ttu-id="4a474-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a474-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4a474-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a474-126">-SubscriptionId</span></span>
<span data-ttu-id="4a474-127">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a474-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4a474-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a474-128">-Confirm</span></span>
<span data-ttu-id="4a474-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a474-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a474-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a474-130">-WhatIf</span></span>
<span data-ttu-id="4a474-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a474-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a474-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a474-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a474-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a474-133">CommonParameters</span></span>
<span data-ttu-id="4a474-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a474-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a474-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a474-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a474-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="4a474-136">INPUTS</span></span>

### <span data-ttu-id="4a474-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4a474-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4a474-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a474-138">OUTPUTS</span></span>

### <span data-ttu-id="4a474-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a474-139">System.Boolean</span></span>

## <span data-ttu-id="4a474-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="4a474-140">NOTES</span></span>

<span data-ttu-id="4a474-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4a474-141">ALIASES</span></span>

<span data-ttu-id="4a474-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="4a474-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a474-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4a474-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a474-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a474-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a474-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="4a474-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a474-146">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="4a474-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4a474-147">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="4a474-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4a474-148">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="4a474-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4a474-149">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="4a474-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4a474-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4a474-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a474-151">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="4a474-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4a474-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a474-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4a474-153">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a474-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="4a474-154">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="4a474-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4a474-155">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a474-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4a474-156">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="4a474-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4a474-157">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="4a474-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4a474-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a474-158">RELATED LINKS</span></span>

