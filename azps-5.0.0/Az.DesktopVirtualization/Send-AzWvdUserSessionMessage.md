---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 047ede26246c31b17fbeb49fca4353b2cb17594c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296965"
---
# <span data-ttu-id="e2a70-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="e2a70-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="e2a70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2a70-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a70-103">Inviare un messaggio a un utente.</span><span class="sxs-lookup"><span data-stu-id="e2a70-103">Send a message to a user.</span></span>

## <span data-ttu-id="e2a70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2a70-104">SYNTAX</span></span>

### <span data-ttu-id="e2a70-105">SendExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2a70-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2a70-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e2a70-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2a70-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2a70-107">DESCRIPTION</span></span>
<span data-ttu-id="e2a70-108">Inviare un messaggio a un utente.</span><span class="sxs-lookup"><span data-stu-id="e2a70-108">Send a message to a user.</span></span>

## <span data-ttu-id="e2a70-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2a70-109">EXAMPLES</span></span>

### <span data-ttu-id="e2a70-110">Esempio 1: inviare un messaggio a UserSession</span><span class="sxs-lookup"><span data-stu-id="e2a70-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="e2a70-111">Questo comando Invia un messaggio a un UserSession.</span><span class="sxs-lookup"><span data-stu-id="e2a70-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="e2a70-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2a70-112">PARAMETERS</span></span>

### <span data-ttu-id="e2a70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a70-113">-DefaultProfile</span></span>
<span data-ttu-id="e2a70-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a70-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2a70-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e2a70-115">-HostPoolName</span></span>
<span data-ttu-id="e2a70-116">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e2a70-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="e2a70-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2a70-117">-InputObject</span></span>
<span data-ttu-id="e2a70-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e2a70-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e2a70-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="e2a70-119">-MessageBody</span></span>
<span data-ttu-id="e2a70-120">Corpo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e2a70-120">Body of message.</span></span>

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

### <span data-ttu-id="e2a70-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="e2a70-121">-MessageTitle</span></span>
<span data-ttu-id="e2a70-122">Titolo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e2a70-122">Title of message.</span></span>

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

### <span data-ttu-id="e2a70-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2a70-123">-PassThru</span></span>
<span data-ttu-id="e2a70-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="e2a70-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e2a70-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a70-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2a70-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2a70-126">The name of the resource group.</span></span>
<span data-ttu-id="e2a70-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e2a70-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e2a70-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="e2a70-128">-SessionHostName</span></span>
<span data-ttu-id="e2a70-129">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="e2a70-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="e2a70-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2a70-130">-SubscriptionId</span></span>
<span data-ttu-id="e2a70-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e2a70-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e2a70-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="e2a70-132">-UserSessionId</span></span>
<span data-ttu-id="e2a70-133">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="e2a70-133">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="e2a70-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2a70-134">-Confirm</span></span>
<span data-ttu-id="e2a70-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2a70-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2a70-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a70-136">-WhatIf</span></span>
<span data-ttu-id="e2a70-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2a70-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2a70-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2a70-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2a70-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a70-139">CommonParameters</span></span>
<span data-ttu-id="e2a70-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a70-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a70-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2a70-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a70-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2a70-142">INPUTS</span></span>

### <span data-ttu-id="e2a70-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e2a70-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e2a70-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2a70-144">OUTPUTS</span></span>

### <span data-ttu-id="e2a70-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2a70-145">System.Boolean</span></span>

## <span data-ttu-id="e2a70-146">Note</span><span class="sxs-lookup"><span data-stu-id="e2a70-146">NOTES</span></span>

<span data-ttu-id="e2a70-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e2a70-147">ALIASES</span></span>

<span data-ttu-id="e2a70-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2a70-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2a70-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e2a70-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2a70-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2a70-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2a70-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e2a70-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2a70-152">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="e2a70-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e2a70-153">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="e2a70-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e2a70-154">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="e2a70-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e2a70-155">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e2a70-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e2a70-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e2a70-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2a70-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2a70-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e2a70-158">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e2a70-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="e2a70-159">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="e2a70-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e2a70-160">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e2a70-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e2a70-161">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="e2a70-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e2a70-162">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e2a70-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e2a70-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2a70-163">RELATED LINKS</span></span>

