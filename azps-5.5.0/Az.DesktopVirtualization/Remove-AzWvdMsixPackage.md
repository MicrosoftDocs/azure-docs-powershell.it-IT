---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180766"
---
# <span data-ttu-id="f6f4f-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="f6f4f-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="f6f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f4f-103">Rimuovere un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="f6f4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6f4f-104">SYNTAX</span></span>

### <span data-ttu-id="f6f4f-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6f4f-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6f4f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6f4f-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6f4f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f6f4f-107">DESCRIPTION</span></span>
<span data-ttu-id="f6f4f-108">Rimuovere un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="f6f4f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6f4f-109">EXAMPLES</span></span>

### <span data-ttu-id="f6f4f-110">Esempio 1: Eliminare il pacchetto MSIX in base al nome completo del pacchetto</span><span class="sxs-lookup"><span data-stu-id="f6f4f-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="f6f4f-111">Questo comando elimina un pacchetto MSIX in un hostPool</span><span class="sxs-lookup"><span data-stu-id="f6f4f-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="f6f4f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6f4f-112">PARAMETERS</span></span>

### <span data-ttu-id="f6f4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f4f-113">-DefaultProfile</span></span>
<span data-ttu-id="f6f4f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f4f-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="f6f4f-115">-FullName</span></span>
<span data-ttu-id="f6f4f-116">Nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="f6f4f-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="f6f4f-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f6f4f-117">-HostPoolName</span></span>
<span data-ttu-id="f6f4f-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="f6f4f-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="f6f4f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6f4f-119">-InputObject</span></span>
<span data-ttu-id="f6f4f-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6f4f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6f4f-121">-PassThru</span></span>
<span data-ttu-id="f6f4f-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="f6f4f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f6f4f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6f4f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6f4f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-124">The name of the resource group.</span></span>
<span data-ttu-id="f6f4f-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f6f4f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6f4f-126">-SubscriptionId</span></span>
<span data-ttu-id="f6f4f-127">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f6f4f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6f4f-128">-Confirm</span></span>
<span data-ttu-id="f6f4f-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6f4f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f4f-130">-WhatIf</span></span>
<span data-ttu-id="f6f4f-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6f4f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6f4f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f4f-133">CommonParameters</span></span>
<span data-ttu-id="f6f4f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f4f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f4f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="f6f4f-136">INPUTS</span></span>

### <span data-ttu-id="f6f4f-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f6f4f-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f6f4f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6f4f-138">OUTPUTS</span></span>

### <span data-ttu-id="f6f4f-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6f4f-139">System.Boolean</span></span>

## <span data-ttu-id="f6f4f-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="f6f4f-140">NOTES</span></span>

<span data-ttu-id="f6f4f-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f6f4f-141">ALIASES</span></span>

<span data-ttu-id="f6f4f-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f6f4f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6f4f-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6f4f-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6f4f-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="f6f4f-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6f4f-146">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="f6f4f-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f6f4f-147">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="f6f4f-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f6f4f-148">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="f6f4f-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f6f4f-149">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="f6f4f-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f6f4f-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f6f4f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6f4f-151">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="f6f4f-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f6f4f-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f6f4f-153">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="f6f4f-154">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="f6f4f-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f6f4f-155">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f6f4f-156">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="f6f4f-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f6f4f-157">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="f6f4f-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f6f4f-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6f4f-158">RELATED LINKS</span></span>

