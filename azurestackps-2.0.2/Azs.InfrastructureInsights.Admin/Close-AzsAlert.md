---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030437"
---
# <span data-ttu-id="96b46-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="96b46-101">Close-AzsAlert</span></span>

## <span data-ttu-id="96b46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96b46-102">SYNOPSIS</span></span>
<span data-ttu-id="96b46-103">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="96b46-103">Closes the given alert.</span></span>

## <span data-ttu-id="96b46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96b46-104">SYNTAX</span></span>

### <span data-ttu-id="96b46-105">CloseExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96b46-105">CloseExpanded (Default)</span></span>
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

### <span data-ttu-id="96b46-106">Vicino</span><span class="sxs-lookup"><span data-stu-id="96b46-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="96b46-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96b46-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96b46-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="96b46-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96b46-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96b46-109">DESCRIPTION</span></span>
<span data-ttu-id="96b46-110">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="96b46-110">Closes the given alert.</span></span>

## <span data-ttu-id="96b46-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96b46-111">EXAMPLES</span></span>

### <span data-ttu-id="96b46-112">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="96b46-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="96b46-113">Chiudere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="96b46-113">Close an alert by Name.</span></span>

### <span data-ttu-id="96b46-114">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="96b46-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="96b46-115">Chiudere un avviso tramite piping.</span><span class="sxs-lookup"><span data-stu-id="96b46-115">Close an alert through piping.</span></span>

## <span data-ttu-id="96b46-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96b46-116">PARAMETERS</span></span>

### <span data-ttu-id="96b46-117">-Avviso</span><span class="sxs-lookup"><span data-stu-id="96b46-117">-Alert</span></span>
<span data-ttu-id="96b46-118">Questo oggetto rappresenta una risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-118">This object represents an alert resource.</span></span>
<span data-ttu-id="96b46-119">Per costruire, vedere la sezione Note per le proprietà degli avvisi e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="96b46-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96b46-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="96b46-120">-AlertId</span></span>
<span data-ttu-id="96b46-121">Ottiene o imposta l'ID dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-121">Gets or sets the ID of the alert.</span></span>

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

### <span data-ttu-id="96b46-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="96b46-122">-AlertProperty</span></span>
<span data-ttu-id="96b46-123">Proprietà dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-123">Properties of the alert.</span></span>

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

### <span data-ttu-id="96b46-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="96b46-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="96b46-125">Alias utente che ha chiuso l'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-125">User alias who closed the alert.</span></span>

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

### <span data-ttu-id="96b46-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="96b46-126">-ClosedTimestamp</span></span>
<span data-ttu-id="96b46-127">Timestamp quando l'avviso è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="96b46-127">Timestamp when the alert was closed.</span></span>

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

### <span data-ttu-id="96b46-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="96b46-128">-CreatedTimestamp</span></span>
<span data-ttu-id="96b46-129">Timestamp quando l'avviso è stato creato.</span><span class="sxs-lookup"><span data-stu-id="96b46-129">Timestamp when the alert was created.</span></span>

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

### <span data-ttu-id="96b46-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b46-130">-DefaultProfile</span></span>
<span data-ttu-id="96b46-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96b46-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96b46-132">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="96b46-132">-Description</span></span>
<span data-ttu-id="96b46-133">Descrizione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-133">Description of the alert.</span></span>

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

### <span data-ttu-id="96b46-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="96b46-134">-FaultId</span></span>
<span data-ttu-id="96b46-135">Ottiene o imposta l'ID errore dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-135">Gets or sets the fault ID of the alert.</span></span>

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

### <span data-ttu-id="96b46-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="96b46-136">-FaultTypeId</span></span>
<span data-ttu-id="96b46-137">Ottiene o imposta l'ID del tipo di errore dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-137">Gets or sets the fault type ID of the alert.</span></span>

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

### <span data-ttu-id="96b46-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="96b46-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="96b46-139">Indica se l'avviso può essere rimediato.</span><span class="sxs-lookup"><span data-stu-id="96b46-139">Indicates if the alert can be remediated.</span></span>

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

### <span data-ttu-id="96b46-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="96b46-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="96b46-141">Nome visualizzato per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="96b46-141">Display name for the impacted item.</span></span>

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

### <span data-ttu-id="96b46-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="96b46-142">-ImpactedResourceId</span></span>
<span data-ttu-id="96b46-143">Ottiene o imposta l'ID risorsa per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="96b46-143">Gets or sets the Resource ID for the impacted item.</span></span>

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

### <span data-ttu-id="96b46-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96b46-144">-InputObject</span></span>
<span data-ttu-id="96b46-145">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="96b46-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96b46-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="96b46-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="96b46-147">Timestamp quando l'avviso è stato aggiornato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="96b46-147">Timestamp when the alert was last updated.</span></span>

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

### <span data-ttu-id="96b46-148">-Posizione</span><span class="sxs-lookup"><span data-stu-id="96b46-148">-Location</span></span>
<span data-ttu-id="96b46-149">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="96b46-149">Name of the region</span></span>

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

### <span data-ttu-id="96b46-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="96b46-150">-Location1</span></span>
<span data-ttu-id="96b46-151">Area di Azure in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="96b46-151">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="96b46-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="96b46-152">-Name</span></span>
<span data-ttu-id="96b46-153">Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-153">Name of the alert.</span></span>

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

### <span data-ttu-id="96b46-154">-Correzione</span><span class="sxs-lookup"><span data-stu-id="96b46-154">-Remediation</span></span>
<span data-ttu-id="96b46-155">Ottiene o imposta le istruzioni per l'aggiornamento dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

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

### <span data-ttu-id="96b46-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b46-156">-ResourceGroupName</span></span>
<span data-ttu-id="96b46-157">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96b46-157">The name of the resource group.</span></span>

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

### <span data-ttu-id="96b46-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="96b46-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="96b46-159">Ottiene o imposta l'ID di registrazione del servizio a cui appartiene l'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

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

### <span data-ttu-id="96b46-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="96b46-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="96b46-161">Ottiene o imposta l'ID di registrazione della risorsa associata all'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="96b46-162">Se l'avviso non è associato a una risorsa, l'ID di registrazione delle risorse è null.</span><span class="sxs-lookup"><span data-stu-id="96b46-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

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

### <span data-ttu-id="96b46-163">-Gravità</span><span class="sxs-lookup"><span data-stu-id="96b46-163">-Severity</span></span>
<span data-ttu-id="96b46-164">Gravità dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-164">Severity of the alert.</span></span>

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

### <span data-ttu-id="96b46-165">-Stato</span><span class="sxs-lookup"><span data-stu-id="96b46-165">-State</span></span>
<span data-ttu-id="96b46-166">Stato dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-166">State of the alert.</span></span>

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

### <span data-ttu-id="96b46-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96b46-167">-SubscriptionId</span></span>
<span data-ttu-id="96b46-168">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="96b46-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="96b46-169">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="96b46-169">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96b46-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="96b46-170">-Tag</span></span>
<span data-ttu-id="96b46-171">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="96b46-171">Resource tags.</span></span>

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

### <span data-ttu-id="96b46-172">-Titolo</span><span class="sxs-lookup"><span data-stu-id="96b46-172">-Title</span></span>
<span data-ttu-id="96b46-173">Ottiene o imposta l'ID risorsa per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="96b46-173">Gets or sets the Resource ID for the impacted item.</span></span>

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

### <span data-ttu-id="96b46-174">-Utente</span><span class="sxs-lookup"><span data-stu-id="96b46-174">-User</span></span>
<span data-ttu-id="96b46-175">Nome utente usato per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="96b46-175">The username used to perform the operation.</span></span>

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

### <span data-ttu-id="96b46-176">-Confermare</span><span class="sxs-lookup"><span data-stu-id="96b46-176">-Confirm</span></span>
<span data-ttu-id="96b46-177">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96b46-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96b46-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b46-178">-WhatIf</span></span>
<span data-ttu-id="96b46-179">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96b46-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96b46-180">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96b46-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96b46-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b46-181">CommonParameters</span></span>
<span data-ttu-id="96b46-182">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96b46-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b46-183">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96b46-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b46-184">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96b46-184">INPUTS</span></span>

### <span data-ttu-id="96b46-185">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="96b46-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="96b46-186">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="96b46-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="96b46-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96b46-187">OUTPUTS</span></span>

### <span data-ttu-id="96b46-188">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="96b46-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="96b46-189">Note</span><span class="sxs-lookup"><span data-stu-id="96b46-189">NOTES</span></span>

<span data-ttu-id="96b46-190">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="96b46-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96b46-191">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96b46-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="96b46-192">AVVISO <IAlert> : questo oggetto rappresenta una risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="96b46-193">`[Location <String>]`: L'area di Azure in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="96b46-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="96b46-194">`[Tag <ITrackedResourceTags>]`: Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="96b46-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="96b46-195">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="96b46-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="96b46-196">`[AlertId <String>]`: Ottiene o imposta l'ID dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="96b46-197">`[AlertProperty <IAlertModelAlertProperties>]`: Proprietà dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="96b46-198">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="96b46-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="96b46-199">`[ClosedByUserAlias <String>]`: Alias utente che ha chiuso l'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="96b46-200">`[ClosedTimestamp <String>]`: Timestamp quando l'avviso è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="96b46-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="96b46-201">`[CreatedTimestamp <String>]`: Timestamp quando l'avviso è stato creato.</span><span class="sxs-lookup"><span data-stu-id="96b46-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="96b46-202">`[Description <IDictionary[]>]`: Descrizione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="96b46-203">`[FaultId <String>]`: Ottiene o imposta l'ID errore dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="96b46-204">`[FaultTypeId <String>]`: Ottiene o imposta l'ID del tipo di errore dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="96b46-205">`[HasValidRemediationAction <Boolean?>]`: Indica se l'avviso può essere rimediato.</span><span class="sxs-lookup"><span data-stu-id="96b46-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="96b46-206">`[ImpactedResourceDisplayName <String>]`: Nome visualizzato per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="96b46-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="96b46-207">`[ImpactedResourceId <String>]`: Ottiene o imposta l'ID risorsa per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="96b46-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="96b46-208">`[LastUpdatedTimestamp <String>]`: Timestamp quando l'avviso è stato aggiornato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="96b46-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="96b46-209">`[Remediation <IDictionary[]>]`: Ottiene o imposta le istruzioni per l'aggiornamento per l'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="96b46-210">`[ResourceProviderRegistrationId <String>]`: Ottiene o imposta l'ID di registrazione del servizio a cui appartiene l'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="96b46-211">`[ResourceRegistrationId <String>]`: Ottiene o imposta l'ID di registrazione della risorsa associata all'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="96b46-212">Se l'avviso non è associato a una risorsa, l'ID di registrazione delle risorse è null.</span><span class="sxs-lookup"><span data-stu-id="96b46-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="96b46-213">`[Severity <String>]`: Gravità dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="96b46-214">`[State <String>]`: Stato dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="96b46-215">`[Title <String>]`: Ottiene o imposta l'ID risorsa per l'elemento impattato.</span><span class="sxs-lookup"><span data-stu-id="96b46-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="96b46-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="96b46-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96b46-217">`[AlertName <String>]`: Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="96b46-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="96b46-218">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="96b46-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96b46-219">`[Location <String>]`: Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="96b46-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="96b46-220">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96b46-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="96b46-221">`[ResourceRegistrationId <String>]`: ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="96b46-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="96b46-222">`[ServiceHealth <String>]`: Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="96b46-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="96b46-223">`[ServiceRegistrationId <String>]`: ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="96b46-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="96b46-224">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="96b46-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="96b46-225">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="96b46-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="96b46-226">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96b46-226">RELATED LINKS</span></span>

