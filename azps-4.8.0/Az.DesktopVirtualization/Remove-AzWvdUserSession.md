---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190215"
---
# <span data-ttu-id="8a565-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="8a565-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="8a565-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a565-102">SYNOPSIS</span></span>
<span data-ttu-id="8a565-103">Rimuovere un userSession.</span><span class="sxs-lookup"><span data-stu-id="8a565-103">Remove a userSession.</span></span>

## <span data-ttu-id="8a565-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a565-104">SYNTAX</span></span>

### <span data-ttu-id="8a565-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a565-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a565-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a565-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a565-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a565-107">DESCRIPTION</span></span>
<span data-ttu-id="8a565-108">Rimuovere un userSession.</span><span class="sxs-lookup"><span data-stu-id="8a565-108">Remove a userSession.</span></span>

## <span data-ttu-id="8a565-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a565-109">EXAMPLES</span></span>

### <span data-ttu-id="8a565-110">Esempio 1: eliminare un desktop di Windows Virtual UserSession per nome</span><span class="sxs-lookup"><span data-stu-id="8a565-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="8a565-111">Questo comando Elimina un UserSession desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="8a565-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="8a565-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a565-112">PARAMETERS</span></span>

### <span data-ttu-id="8a565-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a565-113">-DefaultProfile</span></span>
<span data-ttu-id="8a565-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a565-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a565-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a565-115">-Force</span></span>
<span data-ttu-id="8a565-116">Imponi contrassegno per l'accesso disattivato userSession.</span><span class="sxs-lookup"><span data-stu-id="8a565-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="8a565-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8a565-117">-HostPoolName</span></span>
<span data-ttu-id="8a565-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="8a565-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="8a565-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8a565-119">-Id</span></span>
<span data-ttu-id="8a565-120">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="8a565-120">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="8a565-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a565-121">-InputObject</span></span>
<span data-ttu-id="8a565-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8a565-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a565-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a565-123">-PassThru</span></span>
<span data-ttu-id="8a565-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="8a565-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8a565-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a565-125">-ResourceGroupName</span></span>
<span data-ttu-id="8a565-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8a565-126">The name of the resource group.</span></span>
<span data-ttu-id="8a565-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8a565-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8a565-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="8a565-128">-SessionHostName</span></span>
<span data-ttu-id="8a565-129">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="8a565-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="8a565-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a565-130">-SubscriptionId</span></span>
<span data-ttu-id="8a565-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8a565-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8a565-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a565-132">-Confirm</span></span>
<span data-ttu-id="8a565-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a565-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a565-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a565-134">-WhatIf</span></span>
<span data-ttu-id="8a565-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a565-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a565-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a565-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a565-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a565-137">CommonParameters</span></span>
<span data-ttu-id="8a565-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a565-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a565-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a565-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a565-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a565-140">INPUTS</span></span>

### <span data-ttu-id="8a565-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8a565-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8a565-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a565-142">OUTPUTS</span></span>

### <span data-ttu-id="8a565-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a565-143">System.Boolean</span></span>

## <span data-ttu-id="8a565-144">Note</span><span class="sxs-lookup"><span data-stu-id="8a565-144">NOTES</span></span>

<span data-ttu-id="8a565-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8a565-145">ALIASES</span></span>

<span data-ttu-id="8a565-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a565-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a565-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8a565-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a565-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a565-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a565-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="8a565-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a565-150">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="8a565-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8a565-151">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="8a565-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8a565-152">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="8a565-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8a565-153">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="8a565-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8a565-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="8a565-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a565-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8a565-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8a565-156">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8a565-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="8a565-157">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="8a565-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8a565-158">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8a565-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8a565-159">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="8a565-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8a565-160">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="8a565-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8a565-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a565-161">RELATED LINKS</span></span>

