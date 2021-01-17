---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476373"
---
# <span data-ttu-id="56bac-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="56bac-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="56bac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56bac-102">SYNOPSIS</span></span>
<span data-ttu-id="56bac-103">Rimuovere un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="56bac-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="56bac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56bac-104">SYNTAX</span></span>

### <span data-ttu-id="56bac-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56bac-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56bac-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56bac-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56bac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56bac-107">DESCRIPTION</span></span>
<span data-ttu-id="56bac-108">Rimuovere un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="56bac-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="56bac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56bac-109">EXAMPLES</span></span>

### <span data-ttu-id="56bac-110">Esempio 1: eliminare il pacchetto MSIX per nome completo del pacchetto</span><span class="sxs-lookup"><span data-stu-id="56bac-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="56bac-111">Questo comando Elimina un pacchetto MSIX in un HostPool</span><span class="sxs-lookup"><span data-stu-id="56bac-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="56bac-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56bac-112">PARAMETERS</span></span>

### <span data-ttu-id="56bac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bac-113">-DefaultProfile</span></span>
<span data-ttu-id="56bac-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56bac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56bac-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="56bac-115">-FullName</span></span>
<span data-ttu-id="56bac-116">Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="56bac-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56bac-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="56bac-117">-HostPoolName</span></span>
<span data-ttu-id="56bac-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="56bac-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="56bac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56bac-119">-InputObject</span></span>
<span data-ttu-id="56bac-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="56bac-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56bac-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56bac-121">-PassThru</span></span>
<span data-ttu-id="56bac-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="56bac-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="56bac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56bac-123">-ResourceGroupName</span></span>
<span data-ttu-id="56bac-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56bac-124">The name of the resource group.</span></span>
<span data-ttu-id="56bac-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="56bac-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="56bac-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56bac-126">-SubscriptionId</span></span>
<span data-ttu-id="56bac-127">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56bac-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="56bac-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56bac-128">-Confirm</span></span>
<span data-ttu-id="56bac-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56bac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56bac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56bac-130">-WhatIf</span></span>
<span data-ttu-id="56bac-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56bac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56bac-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56bac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56bac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bac-133">CommonParameters</span></span>
<span data-ttu-id="56bac-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bac-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56bac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bac-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56bac-136">INPUTS</span></span>

### <span data-ttu-id="56bac-137">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="56bac-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="56bac-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56bac-138">OUTPUTS</span></span>

### <span data-ttu-id="56bac-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56bac-139">System.Boolean</span></span>

## <span data-ttu-id="56bac-140">Note</span><span class="sxs-lookup"><span data-stu-id="56bac-140">NOTES</span></span>

<span data-ttu-id="56bac-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="56bac-141">ALIASES</span></span>

<span data-ttu-id="56bac-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56bac-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56bac-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="56bac-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56bac-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56bac-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56bac-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="56bac-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56bac-146">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="56bac-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="56bac-147">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="56bac-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="56bac-148">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="56bac-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="56bac-149">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="56bac-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="56bac-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="56bac-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56bac-151">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="56bac-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="56bac-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56bac-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="56bac-153">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="56bac-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="56bac-154">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="56bac-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="56bac-155">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56bac-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="56bac-156">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="56bac-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="56bac-157">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="56bac-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="56bac-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56bac-158">RELATED LINKS</span></span>

