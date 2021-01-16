---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338419"
---
# <span data-ttu-id="ac7a5-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="ac7a5-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="ac7a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ac7a5-103">Rimuovere un userSession.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-103">Remove a userSession.</span></span>

## <span data-ttu-id="ac7a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac7a5-104">SYNTAX</span></span>

### <span data-ttu-id="ac7a5-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac7a5-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac7a5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ac7a5-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac7a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac7a5-107">DESCRIPTION</span></span>
<span data-ttu-id="ac7a5-108">Rimuovere un userSession.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-108">Remove a userSession.</span></span>

## <span data-ttu-id="ac7a5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac7a5-109">EXAMPLES</span></span>

### <span data-ttu-id="ac7a5-110">Esempio 1: eliminare un desktop di Windows Virtual UserSession per nome</span><span class="sxs-lookup"><span data-stu-id="ac7a5-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="ac7a5-111">Questo comando Elimina un UserSession desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="ac7a5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac7a5-112">PARAMETERS</span></span>

### <span data-ttu-id="ac7a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac7a5-113">-DefaultProfile</span></span>
<span data-ttu-id="ac7a5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac7a5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ac7a5-115">-Force</span></span>
<span data-ttu-id="ac7a5-116">Imponi contrassegno per l'accesso disattivato userSession.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="ac7a5-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ac7a5-117">-HostPoolName</span></span>
<span data-ttu-id="ac7a5-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ac7a5-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ac7a5-119">-Id</span></span>
<span data-ttu-id="ac7a5-120">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-120">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="ac7a5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac7a5-121">-InputObject</span></span>
<span data-ttu-id="ac7a5-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac7a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac7a5-123">-PassThru</span></span>
<span data-ttu-id="ac7a5-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="ac7a5-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ac7a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac7a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac7a5-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-126">The name of the resource group.</span></span>
<span data-ttu-id="ac7a5-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ac7a5-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="ac7a5-128">-SessionHostName</span></span>
<span data-ttu-id="ac7a5-129">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="ac7a5-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac7a5-130">-SubscriptionId</span></span>
<span data-ttu-id="ac7a5-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ac7a5-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac7a5-132">-Confirm</span></span>
<span data-ttu-id="ac7a5-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac7a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac7a5-134">-WhatIf</span></span>
<span data-ttu-id="ac7a5-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac7a5-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac7a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac7a5-137">CommonParameters</span></span>
<span data-ttu-id="ac7a5-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac7a5-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac7a5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac7a5-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac7a5-140">INPUTS</span></span>

### <span data-ttu-id="ac7a5-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ac7a5-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ac7a5-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac7a5-142">OUTPUTS</span></span>

### <span data-ttu-id="ac7a5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac7a5-143">System.Boolean</span></span>

## <span data-ttu-id="ac7a5-144">Note</span><span class="sxs-lookup"><span data-stu-id="ac7a5-144">NOTES</span></span>

<span data-ttu-id="ac7a5-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ac7a5-145">ALIASES</span></span>

<span data-ttu-id="ac7a5-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac7a5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac7a5-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac7a5-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac7a5-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ac7a5-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac7a5-150">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="ac7a5-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ac7a5-151">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ac7a5-152">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ac7a5-153">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ac7a5-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ac7a5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac7a5-155">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ac7a5-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ac7a5-157">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="ac7a5-158">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ac7a5-159">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ac7a5-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ac7a5-160">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="ac7a5-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ac7a5-161">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ac7a5-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ac7a5-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac7a5-162">RELATED LINKS</span></span>

