---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: b47e87ef781138dabe5b2327227ee17f29e5a494
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328927"
---
# <span data-ttu-id="57028-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="57028-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="57028-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57028-102">SYNOPSIS</span></span>
<span data-ttu-id="57028-103">Aggiornare un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="57028-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="57028-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57028-104">SYNTAX</span></span>

### <span data-ttu-id="57028-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57028-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="57028-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="57028-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57028-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57028-107">DESCRIPTION</span></span>
<span data-ttu-id="57028-108">Aggiornare un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="57028-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="57028-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57028-109">EXAMPLES</span></span>

### <span data-ttu-id="57028-110">Esempio 1: aggiornare un pacchetto MSIX</span><span class="sxs-lookup"><span data-stu-id="57028-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="57028-111">Questo comando aggiorna un pacchetto MSIX in un HostPool.</span><span class="sxs-lookup"><span data-stu-id="57028-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="57028-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57028-112">PARAMETERS</span></span>

### <span data-ttu-id="57028-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57028-113">-DefaultProfile</span></span>
<span data-ttu-id="57028-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57028-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57028-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="57028-115">-DisplayName</span></span>
<span data-ttu-id="57028-116">Nome visualizzato per il pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="57028-116">Display name for MSIX Package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57028-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="57028-117">-FullName</span></span>
<span data-ttu-id="57028-118">Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="57028-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57028-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="57028-119">-HostPoolName</span></span>
<span data-ttu-id="57028-120">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="57028-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57028-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57028-121">-InputObject</span></span>
<span data-ttu-id="57028-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="57028-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57028-123">-Attiva</span><span class="sxs-lookup"><span data-stu-id="57028-123">-IsActive</span></span>
<span data-ttu-id="57028-124">Imposta una versione del pacchetto come attiva in hostpool.</span><span class="sxs-lookup"><span data-stu-id="57028-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="57028-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="57028-125">-IsRegularRegistration</span></span>
<span data-ttu-id="57028-126">Impostare la modalità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="57028-126">Set Registration mode.</span></span>
<span data-ttu-id="57028-127">Normale o in ritardo.</span><span class="sxs-lookup"><span data-stu-id="57028-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="57028-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57028-128">-ResourceGroupName</span></span>
<span data-ttu-id="57028-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57028-129">The name of the resource group.</span></span>
<span data-ttu-id="57028-130">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="57028-130">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57028-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57028-131">-SubscriptionId</span></span>
<span data-ttu-id="57028-132">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="57028-132">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57028-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="57028-133">-Confirm</span></span>
<span data-ttu-id="57028-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57028-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57028-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57028-135">-WhatIf</span></span>
<span data-ttu-id="57028-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57028-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57028-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57028-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57028-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57028-138">CommonParameters</span></span>
<span data-ttu-id="57028-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57028-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57028-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57028-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57028-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57028-141">INPUTS</span></span>

### <span data-ttu-id="57028-142">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="57028-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="57028-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57028-143">OUTPUTS</span></span>

### <span data-ttu-id="57028-144">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201019Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="57028-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="57028-145">Note</span><span class="sxs-lookup"><span data-stu-id="57028-145">NOTES</span></span>

<span data-ttu-id="57028-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="57028-146">ALIASES</span></span>

<span data-ttu-id="57028-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57028-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57028-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="57028-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57028-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57028-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57028-150">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="57028-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57028-151">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="57028-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="57028-152">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="57028-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="57028-153">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="57028-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="57028-154">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="57028-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="57028-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="57028-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57028-156">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="57028-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="57028-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57028-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="57028-158">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="57028-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="57028-159">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="57028-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="57028-160">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="57028-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="57028-161">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="57028-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="57028-162">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="57028-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="57028-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57028-163">RELATED LINKS</span></span>

