---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: fa480a867cbbe93a756ea38b4534818ca119c098
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180759"
---
# <span data-ttu-id="7578c-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="7578c-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="7578c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7578c-102">SYNOPSIS</span></span>
<span data-ttu-id="7578c-103">Rimuovere un sessionHost.</span><span class="sxs-lookup"><span data-stu-id="7578c-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="7578c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7578c-104">SYNTAX</span></span>

### <span data-ttu-id="7578c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7578c-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7578c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7578c-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7578c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7578c-107">DESCRIPTION</span></span>
<span data-ttu-id="7578c-108">Rimuovere un sessionHost.</span><span class="sxs-lookup"><span data-stu-id="7578c-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="7578c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7578c-109">EXAMPLES</span></span>

### <span data-ttu-id="7578c-110">Esempio 1: Eliminare un sessionHost di Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="7578c-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="7578c-111">Questo comando elimina un sessionhost di Desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="7578c-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="7578c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7578c-112">PARAMETERS</span></span>

### <span data-ttu-id="7578c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7578c-113">-DefaultProfile</span></span>
<span data-ttu-id="7578c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7578c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7578c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7578c-115">-Force</span></span>
<span data-ttu-id="7578c-116">Forzare il flag a forzare l'eliminazione di sessionHost anche quando è presente userSession.</span><span class="sxs-lookup"><span data-stu-id="7578c-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="7578c-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="7578c-117">-HostPoolName</span></span>
<span data-ttu-id="7578c-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="7578c-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="7578c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7578c-119">-InputObject</span></span>
<span data-ttu-id="7578c-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7578c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7578c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7578c-121">-Name</span></span>
<span data-ttu-id="7578c-122">Nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="7578c-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7578c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7578c-123">-PassThru</span></span>
<span data-ttu-id="7578c-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="7578c-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7578c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7578c-125">-ResourceGroupName</span></span>
<span data-ttu-id="7578c-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7578c-126">The name of the resource group.</span></span>
<span data-ttu-id="7578c-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7578c-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7578c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7578c-128">-SubscriptionId</span></span>
<span data-ttu-id="7578c-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7578c-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7578c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7578c-130">-Confirm</span></span>
<span data-ttu-id="7578c-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7578c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7578c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7578c-132">-WhatIf</span></span>
<span data-ttu-id="7578c-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7578c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7578c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7578c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7578c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7578c-135">CommonParameters</span></span>
<span data-ttu-id="7578c-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7578c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7578c-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7578c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7578c-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="7578c-138">INPUTS</span></span>

### <span data-ttu-id="7578c-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="7578c-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="7578c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7578c-140">OUTPUTS</span></span>

### <span data-ttu-id="7578c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7578c-141">System.Boolean</span></span>

## <span data-ttu-id="7578c-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="7578c-142">NOTES</span></span>

<span data-ttu-id="7578c-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7578c-143">ALIASES</span></span>

<span data-ttu-id="7578c-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="7578c-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7578c-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7578c-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7578c-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7578c-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7578c-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="7578c-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7578c-148">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="7578c-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="7578c-149">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="7578c-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="7578c-150">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="7578c-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="7578c-151">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="7578c-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="7578c-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="7578c-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7578c-153">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="7578c-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="7578c-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7578c-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7578c-155">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7578c-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="7578c-156">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="7578c-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="7578c-157">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7578c-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7578c-158">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="7578c-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="7578c-159">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="7578c-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="7578c-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7578c-160">RELATED LINKS</span></span>

