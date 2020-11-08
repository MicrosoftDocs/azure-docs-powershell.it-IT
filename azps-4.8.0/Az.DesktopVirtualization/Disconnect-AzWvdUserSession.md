---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: f4156fdc52ffaf01caad49517229ebf63d960fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190755"
---
# <span data-ttu-id="e46e2-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="e46e2-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="e46e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e46e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e46e2-103">Scollegare un userSession.</span><span class="sxs-lookup"><span data-stu-id="e46e2-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="e46e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e46e2-104">SYNTAX</span></span>

### <span data-ttu-id="e46e2-105">Disconnetti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e46e2-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e46e2-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e46e2-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e46e2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e46e2-107">DESCRIPTION</span></span>
<span data-ttu-id="e46e2-108">Scollegare un userSession.</span><span class="sxs-lookup"><span data-stu-id="e46e2-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="e46e2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e46e2-109">EXAMPLES</span></span>

### <span data-ttu-id="e46e2-110">Esempio 1: disconnettere un desktop virtuale di Windows UserSession per nome</span><span class="sxs-lookup"><span data-stu-id="e46e2-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="e46e2-111">Questo comando disconnette un UserSession desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="e46e2-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="e46e2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e46e2-112">PARAMETERS</span></span>

### <span data-ttu-id="e46e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46e2-113">-DefaultProfile</span></span>
<span data-ttu-id="e46e2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e46e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e46e2-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e46e2-115">-HostPoolName</span></span>
<span data-ttu-id="e46e2-116">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e46e2-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46e2-117">-ID</span><span class="sxs-lookup"><span data-stu-id="e46e2-117">-Id</span></span>
<span data-ttu-id="e46e2-118">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="e46e2-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46e2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e46e2-119">-InputObject</span></span>
<span data-ttu-id="e46e2-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e46e2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e46e2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e46e2-121">-PassThru</span></span>
<span data-ttu-id="e46e2-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="e46e2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e46e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="e46e2-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e46e2-124">The name of the resource group.</span></span>
<span data-ttu-id="e46e2-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e46e2-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46e2-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="e46e2-126">-SessionHostName</span></span>
<span data-ttu-id="e46e2-127">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="e46e2-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46e2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e46e2-128">-SubscriptionId</span></span>
<span data-ttu-id="e46e2-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e46e2-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46e2-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e46e2-130">-Confirm</span></span>
<span data-ttu-id="e46e2-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e46e2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e46e2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e46e2-132">-WhatIf</span></span>
<span data-ttu-id="e46e2-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e46e2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e46e2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e46e2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e46e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46e2-135">CommonParameters</span></span>
<span data-ttu-id="e46e2-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e46e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46e2-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e46e2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46e2-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e46e2-138">INPUTS</span></span>

### <span data-ttu-id="e46e2-139">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e46e2-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e46e2-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e46e2-140">OUTPUTS</span></span>

### <span data-ttu-id="e46e2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e46e2-141">System.Boolean</span></span>

## <span data-ttu-id="e46e2-142">Note</span><span class="sxs-lookup"><span data-stu-id="e46e2-142">NOTES</span></span>

<span data-ttu-id="e46e2-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e46e2-143">ALIASES</span></span>

<span data-ttu-id="e46e2-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e46e2-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e46e2-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e46e2-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e46e2-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e46e2-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e46e2-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e46e2-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e46e2-148">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="e46e2-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e46e2-149">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="e46e2-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e46e2-150">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="e46e2-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e46e2-151">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e46e2-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e46e2-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e46e2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e46e2-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e46e2-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e46e2-154">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e46e2-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="e46e2-155">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="e46e2-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e46e2-156">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e46e2-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e46e2-157">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="e46e2-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e46e2-158">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e46e2-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e46e2-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e46e2-159">RELATED LINKS</span></span>

