---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 5b5e5ba314bee8d6260985c65f46d372cce94258
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475355"
---
# <span data-ttu-id="bfa18-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="bfa18-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="bfa18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfa18-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa18-103">Inviare un messaggio a un utente.</span><span class="sxs-lookup"><span data-stu-id="bfa18-103">Send a message to a user.</span></span>

## <span data-ttu-id="bfa18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfa18-104">SYNTAX</span></span>

### <span data-ttu-id="bfa18-105">SendExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfa18-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bfa18-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bfa18-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bfa18-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfa18-107">DESCRIPTION</span></span>
<span data-ttu-id="bfa18-108">Inviare un messaggio a un utente.</span><span class="sxs-lookup"><span data-stu-id="bfa18-108">Send a message to a user.</span></span>

## <span data-ttu-id="bfa18-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfa18-109">EXAMPLES</span></span>

### <span data-ttu-id="bfa18-110">Esempio 1: inviare un messaggio a UserSession</span><span class="sxs-lookup"><span data-stu-id="bfa18-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="bfa18-111">Questo comando Invia un messaggio a un UserSession.</span><span class="sxs-lookup"><span data-stu-id="bfa18-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="bfa18-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfa18-112">PARAMETERS</span></span>

### <span data-ttu-id="bfa18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa18-113">-DefaultProfile</span></span>
<span data-ttu-id="bfa18-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfa18-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="bfa18-115">-HostPoolName</span></span>
<span data-ttu-id="bfa18-116">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa18-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfa18-117">-InputObject</span></span>
<span data-ttu-id="bfa18-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bfa18-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa18-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="bfa18-119">-MessageBody</span></span>
<span data-ttu-id="bfa18-120">Corpo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bfa18-120">Body of message.</span></span>

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

### <span data-ttu-id="bfa18-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="bfa18-121">-MessageTitle</span></span>
<span data-ttu-id="bfa18-122">Titolo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bfa18-122">Title of message.</span></span>

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

### <span data-ttu-id="bfa18-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfa18-123">-PassThru</span></span>
<span data-ttu-id="bfa18-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="bfa18-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bfa18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa18-125">-ResourceGroupName</span></span>
<span data-ttu-id="bfa18-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfa18-126">The name of the resource group.</span></span>
<span data-ttu-id="bfa18-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bfa18-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa18-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="bfa18-128">-SessionHostName</span></span>
<span data-ttu-id="bfa18-129">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa18-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfa18-130">-SubscriptionId</span></span>
<span data-ttu-id="bfa18-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bfa18-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa18-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="bfa18-132">-UserSessionId</span></span>
<span data-ttu-id="bfa18-133">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa18-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bfa18-134">-Confirm</span></span>
<span data-ttu-id="bfa18-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa18-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa18-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa18-136">-WhatIf</span></span>
<span data-ttu-id="bfa18-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfa18-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa18-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfa18-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa18-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa18-139">CommonParameters</span></span>
<span data-ttu-id="bfa18-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa18-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa18-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfa18-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa18-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfa18-142">INPUTS</span></span>

### <span data-ttu-id="bfa18-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="bfa18-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="bfa18-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfa18-144">OUTPUTS</span></span>

### <span data-ttu-id="bfa18-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfa18-145">System.Boolean</span></span>

## <span data-ttu-id="bfa18-146">Note</span><span class="sxs-lookup"><span data-stu-id="bfa18-146">NOTES</span></span>

<span data-ttu-id="bfa18-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bfa18-147">ALIASES</span></span>

<span data-ttu-id="bfa18-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfa18-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bfa18-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bfa18-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bfa18-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bfa18-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bfa18-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="bfa18-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bfa18-152">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="bfa18-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="bfa18-153">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="bfa18-154">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="bfa18-155">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="bfa18-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="bfa18-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bfa18-157">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="bfa18-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfa18-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bfa18-159">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bfa18-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="bfa18-160">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="bfa18-161">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bfa18-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bfa18-162">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="bfa18-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="bfa18-163">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="bfa18-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="bfa18-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfa18-164">RELATED LINKS</span></span>

