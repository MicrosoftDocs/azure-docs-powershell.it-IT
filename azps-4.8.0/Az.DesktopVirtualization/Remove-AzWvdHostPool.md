---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 7b0cdf0cbe0aecdb2e1b6829ed1ec22b1e485e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192514"
---
# <span data-ttu-id="86d2d-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="86d2d-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="86d2d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="86d2d-103">Rimuovere un pool host.</span><span class="sxs-lookup"><span data-stu-id="86d2d-103">Remove a host pool.</span></span>

## <span data-ttu-id="86d2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86d2d-104">SYNTAX</span></span>

### <span data-ttu-id="86d2d-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86d2d-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="86d2d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="86d2d-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="86d2d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86d2d-107">DESCRIPTION</span></span>
<span data-ttu-id="86d2d-108">Rimuovere un pool host.</span><span class="sxs-lookup"><span data-stu-id="86d2d-108">Remove a host pool.</span></span>

## <span data-ttu-id="86d2d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86d2d-109">EXAMPLES</span></span>

### <span data-ttu-id="86d2d-110">Esempio 1: eliminare un desktop di Windows Virtual HostPool per nome</span><span class="sxs-lookup"><span data-stu-id="86d2d-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="86d2d-111">Questo comando Elimina un HostPool desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86d2d-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="86d2d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86d2d-112">PARAMETERS</span></span>

### <span data-ttu-id="86d2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d2d-113">-DefaultProfile</span></span>
<span data-ttu-id="86d2d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86d2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d2d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="86d2d-115">-Force</span></span>
<span data-ttu-id="86d2d-116">Imponi contrassegno per eliminare sessionHost.</span><span class="sxs-lookup"><span data-stu-id="86d2d-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="86d2d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86d2d-117">-InputObject</span></span>
<span data-ttu-id="86d2d-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="86d2d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="86d2d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="86d2d-119">-Name</span></span>
<span data-ttu-id="86d2d-120">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="86d2d-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="86d2d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86d2d-121">-PassThru</span></span>
<span data-ttu-id="86d2d-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="86d2d-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="86d2d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d2d-123">-ResourceGroupName</span></span>
<span data-ttu-id="86d2d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86d2d-124">The name of the resource group.</span></span>
<span data-ttu-id="86d2d-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="86d2d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="86d2d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86d2d-126">-SubscriptionId</span></span>
<span data-ttu-id="86d2d-127">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="86d2d-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="86d2d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86d2d-128">-Confirm</span></span>
<span data-ttu-id="86d2d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d2d-130">-WhatIf</span></span>
<span data-ttu-id="86d2d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86d2d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d2d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86d2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d2d-133">CommonParameters</span></span>
<span data-ttu-id="86d2d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d2d-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86d2d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d2d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86d2d-136">INPUTS</span></span>

### <span data-ttu-id="86d2d-137">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="86d2d-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="86d2d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86d2d-138">OUTPUTS</span></span>

### <span data-ttu-id="86d2d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86d2d-139">System.Boolean</span></span>

## <span data-ttu-id="86d2d-140">Note</span><span class="sxs-lookup"><span data-stu-id="86d2d-140">NOTES</span></span>

<span data-ttu-id="86d2d-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="86d2d-141">ALIASES</span></span>

<span data-ttu-id="86d2d-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86d2d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86d2d-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="86d2d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86d2d-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86d2d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86d2d-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="86d2d-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="86d2d-146">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="86d2d-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="86d2d-147">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="86d2d-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="86d2d-148">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="86d2d-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="86d2d-149">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="86d2d-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="86d2d-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="86d2d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86d2d-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86d2d-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="86d2d-152">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="86d2d-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="86d2d-153">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="86d2d-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="86d2d-154">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="86d2d-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="86d2d-155">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="86d2d-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="86d2d-156">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="86d2d-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="86d2d-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86d2d-157">RELATED LINKS</span></span>

