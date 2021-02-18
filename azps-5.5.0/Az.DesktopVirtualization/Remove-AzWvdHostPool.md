---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 65e7d5870e03d4e2d103254aec7a44835286d5df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200495"
---
# <span data-ttu-id="8f7df-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="8f7df-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="8f7df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f7df-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7df-103">Rimuovere un pool host.</span><span class="sxs-lookup"><span data-stu-id="8f7df-103">Remove a host pool.</span></span>

## <span data-ttu-id="8f7df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f7df-104">SYNTAX</span></span>

### <span data-ttu-id="8f7df-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8f7df-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f7df-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f7df-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f7df-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8f7df-107">DESCRIPTION</span></span>
<span data-ttu-id="8f7df-108">Rimuovere un pool host.</span><span class="sxs-lookup"><span data-stu-id="8f7df-108">Remove a host pool.</span></span>

## <span data-ttu-id="8f7df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f7df-109">EXAMPLES</span></span>

### <span data-ttu-id="8f7df-110">Esempio 1: Eliminare un pool di desktop virtuali Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="8f7df-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="8f7df-111">Questo comando elimina un pool di desktop virtuali Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f7df-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="8f7df-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f7df-112">PARAMETERS</span></span>

### <span data-ttu-id="8f7df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7df-113">-DefaultProfile</span></span>
<span data-ttu-id="8f7df-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7df-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8f7df-115">-Force</span></span>
<span data-ttu-id="8f7df-116">Forzare il contrassegno a eliminare sessionHost.</span><span class="sxs-lookup"><span data-stu-id="8f7df-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="8f7df-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f7df-117">-InputObject</span></span>
<span data-ttu-id="8f7df-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8f7df-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8f7df-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8f7df-119">-Name</span></span>
<span data-ttu-id="8f7df-120">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="8f7df-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7df-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f7df-121">-PassThru</span></span>
<span data-ttu-id="8f7df-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="8f7df-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8f7df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7df-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f7df-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f7df-124">The name of the resource group.</span></span>
<span data-ttu-id="8f7df-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8f7df-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8f7df-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f7df-126">-SubscriptionId</span></span>
<span data-ttu-id="8f7df-127">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8f7df-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8f7df-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f7df-128">-Confirm</span></span>
<span data-ttu-id="8f7df-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7df-130">-WhatIf</span></span>
<span data-ttu-id="8f7df-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f7df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7df-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f7df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7df-133">CommonParameters</span></span>
<span data-ttu-id="8f7df-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7df-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8f7df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7df-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="8f7df-136">INPUTS</span></span>

### <span data-ttu-id="8f7df-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8f7df-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8f7df-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f7df-138">OUTPUTS</span></span>

### <span data-ttu-id="8f7df-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f7df-139">System.Boolean</span></span>

## <span data-ttu-id="8f7df-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="8f7df-140">NOTES</span></span>

<span data-ttu-id="8f7df-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8f7df-141">ALIASES</span></span>

<span data-ttu-id="8f7df-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="8f7df-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f7df-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8f7df-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f7df-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f7df-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f7df-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="8f7df-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f7df-146">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="8f7df-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8f7df-147">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="8f7df-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8f7df-148">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="8f7df-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8f7df-149">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="8f7df-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8f7df-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="8f7df-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f7df-151">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="8f7df-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8f7df-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f7df-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8f7df-153">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8f7df-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="8f7df-154">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="8f7df-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8f7df-155">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8f7df-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8f7df-156">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="8f7df-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8f7df-157">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="8f7df-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8f7df-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f7df-158">RELATED LINKS</span></span>

