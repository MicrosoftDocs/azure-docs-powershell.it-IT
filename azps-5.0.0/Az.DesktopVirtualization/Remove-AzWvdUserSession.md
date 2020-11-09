---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296988"
---
# <span data-ttu-id="e4f1f-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="e4f1f-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="e4f1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f1f-103">Rimuovere un userSession.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-103">Remove a userSession.</span></span>

## <span data-ttu-id="e4f1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4f1f-104">SYNTAX</span></span>

### <span data-ttu-id="e4f1f-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4f1f-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4f1f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4f1f-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4f1f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4f1f-107">DESCRIPTION</span></span>
<span data-ttu-id="e4f1f-108">Rimuovere un userSession.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-108">Remove a userSession.</span></span>

## <span data-ttu-id="e4f1f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4f1f-109">EXAMPLES</span></span>

### <span data-ttu-id="e4f1f-110">Esempio 1: eliminare un desktop di Windows Virtual UserSession per nome</span><span class="sxs-lookup"><span data-stu-id="e4f1f-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="e4f1f-111">Questo comando Elimina un UserSession desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="e4f1f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4f1f-112">PARAMETERS</span></span>

### <span data-ttu-id="e4f1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f1f-113">-DefaultProfile</span></span>
<span data-ttu-id="e4f1f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4f1f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e4f1f-115">-Force</span></span>
<span data-ttu-id="e4f1f-116">Imponi contrassegno per l'accesso disattivato userSession.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="e4f1f-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e4f1f-117">-HostPoolName</span></span>
<span data-ttu-id="e4f1f-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e4f1f-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="e4f1f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e4f1f-119">-Id</span></span>
<span data-ttu-id="e4f1f-120">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="e4f1f-120">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="e4f1f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4f1f-121">-InputObject</span></span>
<span data-ttu-id="e4f1f-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4f1f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4f1f-123">-PassThru</span></span>
<span data-ttu-id="e4f1f-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="e4f1f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e4f1f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f1f-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4f1f-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-126">The name of the resource group.</span></span>
<span data-ttu-id="e4f1f-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e4f1f-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="e4f1f-128">-SessionHostName</span></span>
<span data-ttu-id="e4f1f-129">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="e4f1f-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="e4f1f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4f1f-130">-SubscriptionId</span></span>
<span data-ttu-id="e4f1f-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e4f1f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4f1f-132">-Confirm</span></span>
<span data-ttu-id="e4f1f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f1f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f1f-134">-WhatIf</span></span>
<span data-ttu-id="e4f1f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4f1f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f1f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f1f-137">CommonParameters</span></span>
<span data-ttu-id="e4f1f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f1f-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4f1f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f1f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4f1f-140">INPUTS</span></span>

### <span data-ttu-id="e4f1f-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e4f1f-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e4f1f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4f1f-142">OUTPUTS</span></span>

### <span data-ttu-id="e4f1f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4f1f-143">System.Boolean</span></span>

## <span data-ttu-id="e4f1f-144">Note</span><span class="sxs-lookup"><span data-stu-id="e4f1f-144">NOTES</span></span>

<span data-ttu-id="e4f1f-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e4f1f-145">ALIASES</span></span>

<span data-ttu-id="e4f1f-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4f1f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4f1f-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4f1f-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4f1f-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e4f1f-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4f1f-150">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="e4f1f-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e4f1f-151">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="e4f1f-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e4f1f-152">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="e4f1f-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e4f1f-153">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e4f1f-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e4f1f-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e4f1f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4f1f-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e4f1f-156">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="e4f1f-157">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="e4f1f-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e4f1f-158">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e4f1f-159">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="e4f1f-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e4f1f-160">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e4f1f-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e4f1f-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4f1f-161">RELATED LINKS</span></span>

