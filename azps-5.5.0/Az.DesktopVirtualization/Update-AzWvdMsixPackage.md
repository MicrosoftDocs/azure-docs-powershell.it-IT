---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186023"
---
# <span data-ttu-id="0b0b5-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="0b0b5-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="0b0b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0b5-103">Aggiornare un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="0b0b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b0b5-104">SYNTAX</span></span>

### <span data-ttu-id="0b0b5-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b0b5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0b0b5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b0b5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b0b5-107">DESCRIPTION</span></span>
<span data-ttu-id="0b0b5-108">Aggiornare un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="0b0b5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b0b5-109">EXAMPLES</span></span>

### <span data-ttu-id="0b0b5-110">Esempio 1: Aggiornare un pacchetto MSIX</span><span class="sxs-lookup"><span data-stu-id="0b0b5-110">Example 1: Update a MSIX Package</span></span> 
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

<span data-ttu-id="0b0b5-111">Questo comando aggiorna un pacchetto MSIX in un hostPool.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="0b0b5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b0b5-112">PARAMETERS</span></span>

### <span data-ttu-id="0b0b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0b5-113">-DefaultProfile</span></span>
<span data-ttu-id="0b0b5-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b0b5-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0b0b5-115">-DisplayName</span></span>
<span data-ttu-id="0b0b5-116">Nome visualizzato per il pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="0b0b5-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="0b0b5-117">-FullName</span></span>
<span data-ttu-id="0b0b5-118">Nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="0b0b5-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="0b0b5-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="0b0b5-119">-HostPoolName</span></span>
<span data-ttu-id="0b0b5-120">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="0b0b5-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="0b0b5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b0b5-121">-InputObject</span></span>
<span data-ttu-id="0b0b5-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b0b5-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="0b0b5-123">-IsActive</span></span>
<span data-ttu-id="0b0b5-124">Impostare una versione del pacchetto in modo che sia attiva nell'altro pool host.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="0b0b5-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="0b0b5-125">-IsRegularRegistration</span></span>
<span data-ttu-id="0b0b5-126">Impostare la modalità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-126">Set Registration mode.</span></span>
<span data-ttu-id="0b0b5-127">Normale o ritardato.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="0b0b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b0b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="0b0b5-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-129">The name of the resource group.</span></span>
<span data-ttu-id="0b0b5-130">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0b0b5-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b0b5-131">-SubscriptionId</span></span>
<span data-ttu-id="0b0b5-132">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0b0b5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b0b5-133">-Confirm</span></span>
<span data-ttu-id="0b0b5-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b0b5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b0b5-135">-WhatIf</span></span>
<span data-ttu-id="0b0b5-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b0b5-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b0b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0b5-138">CommonParameters</span></span>
<span data-ttu-id="0b0b5-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0b5-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0b5-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b0b5-141">INPUTS</span></span>

### <span data-ttu-id="0b0b5-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0b0b5-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0b0b5-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b0b5-143">OUTPUTS</span></span>

### <span data-ttu-id="0b0b5-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="0b0b5-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="0b0b5-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b0b5-145">NOTES</span></span>

<span data-ttu-id="0b0b5-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0b0b5-146">ALIASES</span></span>

<span data-ttu-id="0b0b5-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0b0b5-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b0b5-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b0b5-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b0b5-150">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="0b0b5-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b0b5-151">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="0b0b5-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0b0b5-152">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="0b0b5-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0b0b5-153">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="0b0b5-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0b0b5-154">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="0b0b5-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0b0b5-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0b0b5-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b0b5-156">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="0b0b5-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="0b0b5-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0b0b5-158">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="0b0b5-159">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="0b0b5-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0b0b5-160">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0b0b5-161">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="0b0b5-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0b0b5-162">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="0b0b5-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0b0b5-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b0b5-163">RELATED LINKS</span></span>

