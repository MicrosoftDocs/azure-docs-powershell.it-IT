---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 1976c5750b5372cedce8ccf237fe8a444fa1feee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966013"
---
# <span data-ttu-id="c78ae-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="c78ae-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="c78ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c78ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c78ae-103">Inviare un messaggio a un utente.</span><span class="sxs-lookup"><span data-stu-id="c78ae-103">Send a message to a user.</span></span>

## <span data-ttu-id="c78ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c78ae-104">SYNTAX</span></span>

### <span data-ttu-id="c78ae-105">SendExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c78ae-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c78ae-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c78ae-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c78ae-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c78ae-107">DESCRIPTION</span></span>
<span data-ttu-id="c78ae-108">Inviare un messaggio a un utente.</span><span class="sxs-lookup"><span data-stu-id="c78ae-108">Send a message to a user.</span></span>

## <span data-ttu-id="c78ae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c78ae-109">EXAMPLES</span></span>

### <span data-ttu-id="c78ae-110">Esempio 1: Inviare un messaggio a UserSession</span><span class="sxs-lookup"><span data-stu-id="c78ae-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="c78ae-111">Questo comando invia un messaggio a UserSession.</span><span class="sxs-lookup"><span data-stu-id="c78ae-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="c78ae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c78ae-112">PARAMETERS</span></span>

### <span data-ttu-id="c78ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c78ae-113">-DefaultProfile</span></span>
<span data-ttu-id="c78ae-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c78ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c78ae-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c78ae-115">-HostPoolName</span></span>
<span data-ttu-id="c78ae-116">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="c78ae-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c78ae-117">-InputObject</span></span>
<span data-ttu-id="c78ae-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c78ae-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c78ae-119">-Message Sistema</span><span class="sxs-lookup"><span data-stu-id="c78ae-119">-MessageBody</span></span>
<span data-ttu-id="c78ae-120">Corpo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="c78ae-120">Body of message.</span></span>

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

### <span data-ttu-id="c78ae-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="c78ae-121">-MessageTitle</span></span>
<span data-ttu-id="c78ae-122">Titolo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="c78ae-122">Title of message.</span></span>

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

### <span data-ttu-id="c78ae-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c78ae-123">-PassThru</span></span>
<span data-ttu-id="c78ae-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="c78ae-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c78ae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c78ae-125">-ResourceGroupName</span></span>
<span data-ttu-id="c78ae-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c78ae-126">The name of the resource group.</span></span>
<span data-ttu-id="c78ae-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c78ae-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c78ae-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="c78ae-128">-SessionHostName</span></span>
<span data-ttu-id="c78ae-129">Nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="c78ae-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c78ae-130">-SubscriptionId</span></span>
<span data-ttu-id="c78ae-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c78ae-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c78ae-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="c78ae-132">-UserSessionId</span></span>
<span data-ttu-id="c78ae-133">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-133">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="c78ae-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c78ae-134">-Confirm</span></span>
<span data-ttu-id="c78ae-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c78ae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c78ae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c78ae-136">-WhatIf</span></span>
<span data-ttu-id="c78ae-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c78ae-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c78ae-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c78ae-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c78ae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c78ae-139">CommonParameters</span></span>
<span data-ttu-id="c78ae-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c78ae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c78ae-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c78ae-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c78ae-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="c78ae-142">INPUTS</span></span>

### <span data-ttu-id="c78ae-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c78ae-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c78ae-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c78ae-144">OUTPUTS</span></span>

### <span data-ttu-id="c78ae-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c78ae-145">System.Boolean</span></span>

## <span data-ttu-id="c78ae-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="c78ae-146">NOTES</span></span>

<span data-ttu-id="c78ae-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c78ae-147">ALIASES</span></span>

<span data-ttu-id="c78ae-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="c78ae-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c78ae-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c78ae-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c78ae-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c78ae-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c78ae-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c78ae-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c78ae-152">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="c78ae-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c78ae-153">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c78ae-154">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c78ae-155">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c78ae-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="c78ae-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c78ae-157">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c78ae-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c78ae-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c78ae-159">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c78ae-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="c78ae-160">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c78ae-161">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c78ae-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c78ae-162">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="c78ae-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c78ae-163">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c78ae-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c78ae-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c78ae-164">RELATED LINKS</span></span>

