---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 61e1eb1f5ae3846ce2f0cf7ad82d17d613d27e0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966205"
---
# <span data-ttu-id="b6186-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="b6186-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="b6186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6186-102">SYNOPSIS</span></span>
<span data-ttu-id="b6186-103">Disconnettere una userSession.</span><span class="sxs-lookup"><span data-stu-id="b6186-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="b6186-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6186-104">SYNTAX</span></span>

### <span data-ttu-id="b6186-105">Disconnetti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6186-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6186-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6186-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6186-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6186-107">DESCRIPTION</span></span>
<span data-ttu-id="b6186-108">Disconnettere una userSession.</span><span class="sxs-lookup"><span data-stu-id="b6186-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="b6186-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6186-109">EXAMPLES</span></span>

### <span data-ttu-id="b6186-110">Esempio 1: Disconnettere un userSession di Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="b6186-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="b6186-111">Questo comando disconnette una UserSession di Desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="b6186-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="b6186-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6186-112">PARAMETERS</span></span>

### <span data-ttu-id="b6186-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6186-113">-DefaultProfile</span></span>
<span data-ttu-id="b6186-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6186-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6186-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b6186-115">-HostPoolName</span></span>
<span data-ttu-id="b6186-116">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b6186-117">-Id</span><span class="sxs-lookup"><span data-stu-id="b6186-117">-Id</span></span>
<span data-ttu-id="b6186-118">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-118">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="b6186-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6186-119">-InputObject</span></span>
<span data-ttu-id="b6186-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b6186-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6186-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6186-121">-PassThru</span></span>
<span data-ttu-id="b6186-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b6186-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b6186-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6186-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6186-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6186-124">The name of the resource group.</span></span>
<span data-ttu-id="b6186-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6186-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b6186-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="b6186-126">-SessionHostName</span></span>
<span data-ttu-id="b6186-127">Nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-127">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="b6186-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6186-128">-SubscriptionId</span></span>
<span data-ttu-id="b6186-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b6186-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b6186-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6186-130">-Confirm</span></span>
<span data-ttu-id="b6186-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6186-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6186-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6186-132">-WhatIf</span></span>
<span data-ttu-id="b6186-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6186-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6186-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6186-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6186-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6186-135">CommonParameters</span></span>
<span data-ttu-id="b6186-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6186-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6186-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6186-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6186-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6186-138">INPUTS</span></span>

### <span data-ttu-id="b6186-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b6186-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b6186-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6186-140">OUTPUTS</span></span>

### <span data-ttu-id="b6186-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6186-141">System.Boolean</span></span>

## <span data-ttu-id="b6186-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6186-142">NOTES</span></span>

<span data-ttu-id="b6186-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b6186-143">ALIASES</span></span>

<span data-ttu-id="b6186-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b6186-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6186-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b6186-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6186-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6186-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6186-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b6186-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6186-148">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="b6186-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b6186-149">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b6186-150">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b6186-151">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b6186-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b6186-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6186-153">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b6186-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6186-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b6186-155">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6186-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="b6186-156">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b6186-157">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b6186-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b6186-158">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="b6186-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b6186-159">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b6186-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b6186-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6186-160">RELATED LINKS</span></span>

