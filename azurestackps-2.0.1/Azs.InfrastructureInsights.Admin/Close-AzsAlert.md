---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023257"
---
# <span data-ttu-id="4ea03-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="4ea03-101">Close-AzsAlert</span></span>

## <span data-ttu-id="4ea03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ea03-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea03-103">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-103">Closes the given alert.</span></span>

## <span data-ttu-id="4ea03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ea03-104">SYNTAX</span></span>

### <span data-ttu-id="4ea03-105">CloseExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ea03-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ea03-106">Vicino</span><span class="sxs-lookup"><span data-stu-id="4ea03-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4ea03-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4ea03-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ea03-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4ea03-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ea03-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ea03-109">DESCRIPTION</span></span>
<span data-ttu-id="4ea03-110">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-110">Closes the given alert.</span></span>

## <span data-ttu-id="4ea03-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ea03-111">EXAMPLES</span></span>

### <span data-ttu-id="4ea03-112">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="4ea03-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="4ea03-113">Chiudere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="4ea03-113">Close an alert by Name.</span></span>

### <span data-ttu-id="4ea03-114">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="4ea03-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="4ea03-115">Chiudere un avviso tramite piping.</span><span class="sxs-lookup"><span data-stu-id="4ea03-115">Close an alert through piping.</span></span>

## <span data-ttu-id="4ea03-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ea03-116">PARAMETERS</span></span>

### <span data-ttu-id="4ea03-117">-Avviso</span><span class="sxs-lookup"><span data-stu-id="4ea03-117">-Alert</span></span>
<span data-ttu-id="4ea03-118">Questo oggetto rappresenta una risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-118">This object represents an alert resource.</span></span>
<span data-ttu-id="4ea03-119">Per costruire, vedere la sezione Note per le proprietà degli avvisi e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4ea03-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="4ea03-120">-AlertId</span></span>
<span data-ttu-id="4ea03-121">Ottiene o imposta l'ID dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="4ea03-122">-AlertProperty</span></span>
<span data-ttu-id="4ea03-123">Proprietà dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="4ea03-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="4ea03-125">Alias utente che ha chiuso l'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="4ea03-126">-ClosedTimestamp</span></span>
<span data-ttu-id="4ea03-127">Timestamp quando l'avviso è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="4ea03-128">-CreatedTimestamp</span></span>
<span data-ttu-id="4ea03-129">Timestamp quando l'avviso è stato creato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea03-130">-DefaultProfile</span></span>
<span data-ttu-id="4ea03-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea03-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea03-132">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ea03-132">-Description</span></span>
<span data-ttu-id="4ea03-133">Descrizione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="4ea03-134">-FaultId</span></span>
<span data-ttu-id="4ea03-135">Ottiene o imposta l'ID errore dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="4ea03-136">-FaultTypeId</span></span>
<span data-ttu-id="4ea03-137">Ottiene o imposta l'ID del tipo di errore dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="4ea03-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="4ea03-139">Indica se l'avviso può essere rimediato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="4ea03-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="4ea03-141">Nome visualizzato per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="4ea03-142">-ImpactedResourceId</span></span>
<span data-ttu-id="4ea03-143">Ottiene o imposta l'ID risorsa per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ea03-144">-InputObject</span></span>
<span data-ttu-id="4ea03-145">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4ea03-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="4ea03-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="4ea03-147">Timestamp quando l'avviso è stato aggiornato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="4ea03-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-148">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4ea03-148">-Location</span></span>
<span data-ttu-id="4ea03-149">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="4ea03-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="4ea03-150">-Location1</span></span>
<span data-ttu-id="4ea03-151">Area di Azure in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="4ea03-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ea03-152">-Name</span></span>
<span data-ttu-id="4ea03-153">Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-154">-Correzione</span><span class="sxs-lookup"><span data-stu-id="4ea03-154">-Remediation</span></span>
<span data-ttu-id="4ea03-155">Ottiene o imposta le istruzioni per l'aggiornamento dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea03-156">-ResourceGroupName</span></span>
<span data-ttu-id="4ea03-157">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ea03-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="4ea03-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="4ea03-159">Ottiene o imposta l'ID di registrazione del servizio a cui appartiene l'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="4ea03-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="4ea03-161">Ottiene o imposta l'ID di registrazione della risorsa associata all'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="4ea03-162">Se l'avviso non è associato a una risorsa, l'ID di registrazione delle risorse è null.</span><span class="sxs-lookup"><span data-stu-id="4ea03-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-163">-Gravità</span><span class="sxs-lookup"><span data-stu-id="4ea03-163">-Severity</span></span>
<span data-ttu-id="4ea03-164">Gravità dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-165">-Stato</span><span class="sxs-lookup"><span data-stu-id="4ea03-165">-State</span></span>
<span data-ttu-id="4ea03-166">Stato dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ea03-167">-SubscriptionId</span></span>
<span data-ttu-id="4ea03-168">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea03-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ea03-169">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="4ea03-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ea03-170">-Tag</span></span>
<span data-ttu-id="4ea03-171">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4ea03-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-172">-Titolo</span><span class="sxs-lookup"><span data-stu-id="4ea03-172">-Title</span></span>
<span data-ttu-id="4ea03-173">Ottiene o imposta l'ID risorsa per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-174">-Utente</span><span class="sxs-lookup"><span data-stu-id="4ea03-174">-User</span></span>
<span data-ttu-id="4ea03-175">Nome utente usato per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4ea03-175">The username used to perform the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ea03-176">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ea03-176">-Confirm</span></span>
<span data-ttu-id="4ea03-177">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ea03-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea03-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea03-178">-WhatIf</span></span>
<span data-ttu-id="4ea03-179">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ea03-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea03-180">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ea03-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea03-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea03-181">CommonParameters</span></span>
<span data-ttu-id="4ea03-182">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea03-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea03-183">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ea03-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea03-184">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ea03-184">INPUTS</span></span>

### <span data-ttu-id="4ea03-185">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="4ea03-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="4ea03-186">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4ea03-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="4ea03-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ea03-187">OUTPUTS</span></span>

### <span data-ttu-id="4ea03-188">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="4ea03-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="4ea03-189">Note</span><span class="sxs-lookup"><span data-stu-id="4ea03-189">NOTES</span></span>

<span data-ttu-id="4ea03-190">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4ea03-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ea03-191">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ea03-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4ea03-192">AVVISO <IAlert> : questo oggetto rappresenta una risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="4ea03-193">`[Location <String>]`: L'area di Azure in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="4ea03-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="4ea03-194">`[Tag <ITrackedResourceTags>]`: Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4ea03-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="4ea03-195">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="4ea03-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4ea03-196">`[AlertId <String>]`: Ottiene o imposta l'ID dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="4ea03-197">`[AlertProperty <IAlertModelAlertProperties>]`: Proprietà dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="4ea03-198">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="4ea03-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4ea03-199">`[ClosedByUserAlias <String>]`: Alias utente che ha chiuso l'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="4ea03-200">`[ClosedTimestamp <String>]`: Timestamp quando l'avviso è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="4ea03-201">`[CreatedTimestamp <String>]`: Timestamp quando l'avviso è stato creato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="4ea03-202">`[Description <IDictionary[]>]`: Descrizione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="4ea03-203">`[FaultId <String>]`: Ottiene o imposta l'ID errore dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="4ea03-204">`[FaultTypeId <String>]`: Ottiene o imposta l'ID del tipo di errore dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="4ea03-205">`[HasValidRemediationAction <Boolean?>]`: Indica se l'avviso può essere rimediato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="4ea03-206">`[ImpactedResourceDisplayName <String>]`: Nome visualizzato per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="4ea03-207">`[ImpactedResourceId <String>]`: Ottiene o imposta l'ID risorsa per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="4ea03-208">`[LastUpdatedTimestamp <String>]`: Timestamp quando l'avviso è stato aggiornato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="4ea03-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="4ea03-209">`[Remediation <IDictionary[]>]`: Ottiene o imposta le istruzioni per l'aggiornamento per l'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="4ea03-210">`[ResourceProviderRegistrationId <String>]`: Ottiene o imposta l'ID di registrazione del servizio a cui appartiene l'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="4ea03-211">`[ResourceRegistrationId <String>]`: Ottiene o imposta l'ID di registrazione della risorsa associata all'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="4ea03-212">Se l'avviso non è associato a una risorsa, l'ID di registrazione delle risorse è null.</span><span class="sxs-lookup"><span data-stu-id="4ea03-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="4ea03-213">`[Severity <String>]`: Gravità dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="4ea03-214">`[State <String>]`: Stato dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="4ea03-215">`[Title <String>]`: Ottiene o imposta l'ID risorsa per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="4ea03-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="4ea03-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="4ea03-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ea03-217">`[AlertName <String>]`: Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4ea03-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="4ea03-218">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="4ea03-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ea03-219">`[Location <String>]`: Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="4ea03-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="4ea03-220">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ea03-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4ea03-221">`[ResourceRegistrationId <String>]`: ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="4ea03-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="4ea03-222">`[ServiceHealth <String>]`: Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="4ea03-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="4ea03-223">`[ServiceRegistrationId <String>]`: ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="4ea03-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="4ea03-224">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea03-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4ea03-225">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="4ea03-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4ea03-226">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ea03-226">RELATED LINKS</span></span>

