---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c2604531014283b3599adb94c4a12d70761e1533
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297006"
---
# <span data-ttu-id="80fd2-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="80fd2-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="80fd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="80fd2-103">Rimuovere un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80fd2-103">Remove an application.</span></span>

## <span data-ttu-id="80fd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80fd2-104">SYNTAX</span></span>

### <span data-ttu-id="80fd2-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80fd2-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80fd2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80fd2-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80fd2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80fd2-107">DESCRIPTION</span></span>
<span data-ttu-id="80fd2-108">Rimuovere un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80fd2-108">Remove an application.</span></span>

## <span data-ttu-id="80fd2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80fd2-109">EXAMPLES</span></span>

### <span data-ttu-id="80fd2-110">Esempio 1: eliminare un'applicazione desktop virtuale di Windows per nome</span><span class="sxs-lookup"><span data-stu-id="80fd2-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="80fd2-111">Questo comando Elimina un'applicazione desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="80fd2-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="80fd2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80fd2-112">PARAMETERS</span></span>

### <span data-ttu-id="80fd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fd2-113">-DefaultProfile</span></span>
<span data-ttu-id="80fd2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80fd2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80fd2-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="80fd2-115">-GroupName</span></span>
<span data-ttu-id="80fd2-116">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="80fd2-116">The name of the application group</span></span>

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

### <span data-ttu-id="80fd2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80fd2-117">-InputObject</span></span>
<span data-ttu-id="80fd2-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="80fd2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80fd2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="80fd2-119">-Name</span></span>
<span data-ttu-id="80fd2-120">Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="80fd2-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80fd2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80fd2-121">-PassThru</span></span>
<span data-ttu-id="80fd2-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="80fd2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80fd2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80fd2-123">-ResourceGroupName</span></span>
<span data-ttu-id="80fd2-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80fd2-124">The name of the resource group.</span></span>
<span data-ttu-id="80fd2-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="80fd2-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="80fd2-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80fd2-126">-SubscriptionId</span></span>
<span data-ttu-id="80fd2-127">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80fd2-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="80fd2-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80fd2-128">-Confirm</span></span>
<span data-ttu-id="80fd2-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80fd2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80fd2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80fd2-130">-WhatIf</span></span>
<span data-ttu-id="80fd2-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80fd2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80fd2-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80fd2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80fd2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fd2-133">CommonParameters</span></span>
<span data-ttu-id="80fd2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80fd2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fd2-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80fd2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fd2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80fd2-136">INPUTS</span></span>

### <span data-ttu-id="80fd2-137">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="80fd2-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="80fd2-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80fd2-138">OUTPUTS</span></span>

### <span data-ttu-id="80fd2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80fd2-139">System.Boolean</span></span>

## <span data-ttu-id="80fd2-140">Note</span><span class="sxs-lookup"><span data-stu-id="80fd2-140">NOTES</span></span>

<span data-ttu-id="80fd2-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="80fd2-141">ALIASES</span></span>

<span data-ttu-id="80fd2-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80fd2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80fd2-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="80fd2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80fd2-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80fd2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80fd2-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="80fd2-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80fd2-146">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="80fd2-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="80fd2-147">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="80fd2-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="80fd2-148">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="80fd2-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="80fd2-149">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="80fd2-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="80fd2-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="80fd2-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80fd2-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80fd2-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="80fd2-152">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="80fd2-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="80fd2-153">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="80fd2-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="80fd2-154">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80fd2-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="80fd2-155">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="80fd2-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="80fd2-156">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="80fd2-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="80fd2-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80fd2-157">RELATED LINKS</span></span>

