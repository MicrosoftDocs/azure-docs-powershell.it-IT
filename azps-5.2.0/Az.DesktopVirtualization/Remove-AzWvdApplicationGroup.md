---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338476"
---
# <span data-ttu-id="ce986-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="ce986-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="ce986-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce986-102">SYNOPSIS</span></span>
<span data-ttu-id="ce986-103">Rimuovere un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="ce986-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="ce986-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce986-104">SYNTAX</span></span>

### <span data-ttu-id="ce986-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce986-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce986-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ce986-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce986-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce986-107">DESCRIPTION</span></span>
<span data-ttu-id="ce986-108">Rimuovere un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="ce986-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="ce986-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce986-109">EXAMPLES</span></span>

### <span data-ttu-id="ce986-110">Esempio 1: eliminare un desktop di Windows Virtual ApplicationGroup per nome</span><span class="sxs-lookup"><span data-stu-id="ce986-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="ce986-111">Questo comando Elimina un ApplicationGroup desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ce986-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="ce986-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce986-112">PARAMETERS</span></span>

### <span data-ttu-id="ce986-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce986-113">-DefaultProfile</span></span>
<span data-ttu-id="ce986-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce986-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce986-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce986-115">-InputObject</span></span>
<span data-ttu-id="ce986-116">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ce986-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ce986-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce986-117">-Name</span></span>
<span data-ttu-id="ce986-118">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="ce986-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce986-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce986-119">-PassThru</span></span>
<span data-ttu-id="ce986-120">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="ce986-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ce986-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce986-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce986-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ce986-122">The name of the resource group.</span></span>
<span data-ttu-id="ce986-123">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ce986-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ce986-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce986-124">-SubscriptionId</span></span>
<span data-ttu-id="ce986-125">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ce986-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ce986-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce986-126">-Confirm</span></span>
<span data-ttu-id="ce986-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce986-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce986-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce986-128">-WhatIf</span></span>
<span data-ttu-id="ce986-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce986-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce986-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce986-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce986-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce986-131">CommonParameters</span></span>
<span data-ttu-id="ce986-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce986-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce986-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce986-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce986-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce986-134">INPUTS</span></span>

### <span data-ttu-id="ce986-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ce986-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ce986-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce986-136">OUTPUTS</span></span>

### <span data-ttu-id="ce986-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce986-137">System.Boolean</span></span>

## <span data-ttu-id="ce986-138">Note</span><span class="sxs-lookup"><span data-stu-id="ce986-138">NOTES</span></span>

<span data-ttu-id="ce986-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ce986-139">ALIASES</span></span>

<span data-ttu-id="ce986-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce986-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce986-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ce986-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce986-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce986-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce986-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ce986-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce986-144">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="ce986-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ce986-145">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="ce986-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ce986-146">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="ce986-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ce986-147">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="ce986-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ce986-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ce986-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce986-149">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="ce986-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ce986-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ce986-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ce986-151">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ce986-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="ce986-152">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="ce986-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ce986-153">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ce986-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ce986-154">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="ce986-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ce986-155">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ce986-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ce986-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce986-156">RELATED LINKS</span></span>

