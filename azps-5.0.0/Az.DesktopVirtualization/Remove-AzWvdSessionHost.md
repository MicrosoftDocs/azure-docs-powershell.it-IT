---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: f7bad3a88f4d182407a90a2484daed3d538e3a69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296989"
---
# <span data-ttu-id="af559-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="af559-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="af559-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af559-102">SYNOPSIS</span></span>
<span data-ttu-id="af559-103">Rimuovere un SessionHost.</span><span class="sxs-lookup"><span data-stu-id="af559-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="af559-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af559-104">SYNTAX</span></span>

### <span data-ttu-id="af559-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af559-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="af559-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="af559-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af559-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af559-107">DESCRIPTION</span></span>
<span data-ttu-id="af559-108">Rimuovere un SessionHost.</span><span class="sxs-lookup"><span data-stu-id="af559-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="af559-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af559-109">EXAMPLES</span></span>

### <span data-ttu-id="af559-110">Esempio 1: eliminare un desktop di Windows Virtual SessionHost per nome</span><span class="sxs-lookup"><span data-stu-id="af559-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="af559-111">Questo comando Elimina un SessionHost desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="af559-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="af559-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af559-112">PARAMETERS</span></span>

### <span data-ttu-id="af559-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af559-113">-DefaultProfile</span></span>
<span data-ttu-id="af559-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af559-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af559-115">-Force</span><span class="sxs-lookup"><span data-stu-id="af559-115">-Force</span></span>
<span data-ttu-id="af559-116">Imponi flag per forzare l'eliminazione di sessionHost anche quando userSession esiste.</span><span class="sxs-lookup"><span data-stu-id="af559-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="af559-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="af559-117">-HostPoolName</span></span>
<span data-ttu-id="af559-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="af559-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="af559-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af559-119">-InputObject</span></span>
<span data-ttu-id="af559-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="af559-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="af559-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="af559-121">-Name</span></span>
<span data-ttu-id="af559-122">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="af559-122">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="af559-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af559-123">-PassThru</span></span>
<span data-ttu-id="af559-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="af559-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="af559-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af559-125">-ResourceGroupName</span></span>
<span data-ttu-id="af559-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af559-126">The name of the resource group.</span></span>
<span data-ttu-id="af559-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="af559-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="af559-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af559-128">-SubscriptionId</span></span>
<span data-ttu-id="af559-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af559-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="af559-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af559-130">-Confirm</span></span>
<span data-ttu-id="af559-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af559-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af559-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af559-132">-WhatIf</span></span>
<span data-ttu-id="af559-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af559-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af559-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af559-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af559-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af559-135">CommonParameters</span></span>
<span data-ttu-id="af559-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af559-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af559-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af559-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af559-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af559-138">INPUTS</span></span>

### <span data-ttu-id="af559-139">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="af559-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="af559-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af559-140">OUTPUTS</span></span>

### <span data-ttu-id="af559-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af559-141">System.Boolean</span></span>

## <span data-ttu-id="af559-142">Note</span><span class="sxs-lookup"><span data-stu-id="af559-142">NOTES</span></span>

<span data-ttu-id="af559-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="af559-143">ALIASES</span></span>

<span data-ttu-id="af559-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af559-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af559-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="af559-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af559-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="af559-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af559-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="af559-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af559-148">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="af559-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="af559-149">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="af559-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="af559-150">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="af559-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="af559-151">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="af559-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="af559-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="af559-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af559-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af559-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="af559-154">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="af559-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="af559-155">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="af559-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="af559-156">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af559-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="af559-157">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="af559-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="af559-158">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="af559-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="af559-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af559-159">RELATED LINKS</span></span>

