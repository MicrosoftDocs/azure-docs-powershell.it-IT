---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486140"
---
# <span data-ttu-id="a3401-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a3401-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="a3401-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3401-102">SYNOPSIS</span></span>
<span data-ttu-id="a3401-103">Aggiornare un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a3401-103">Update an Incident.</span></span>

## <span data-ttu-id="a3401-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3401-104">SYNTAX</span></span>

### <span data-ttu-id="a3401-105">IncidentId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3401-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3401-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a3401-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3401-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3401-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3401-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3401-108">DESCRIPTION</span></span>
<span data-ttu-id="a3401-109">Il cmdlet **Update-AzSentinelIncident** aggiorna l'evento Incident nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="a3401-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="a3401-110">Puoi passare un oggetto **Incident** come parametro o usando l'operatore pipeline o in alternativa puoi specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="a3401-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="a3401-111">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a3401-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a3401-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3401-112">EXAMPLES</span></span>

### <span data-ttu-id="a3401-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3401-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="a3401-114">Il comando ottiene l'evento incidentato da *IncidentId* e imposta la proprietà *Severity* su *High*.</span><span class="sxs-lookup"><span data-stu-id="a3401-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="a3401-115">Tutte le altre proprietà restano invariate.</span><span class="sxs-lookup"><span data-stu-id="a3401-115">All other properties remain the same.</span></span>

## <span data-ttu-id="a3401-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3401-116">PARAMETERS</span></span>

### <span data-ttu-id="a3401-117">-Classificazione</span><span class="sxs-lookup"><span data-stu-id="a3401-117">-Classification</span></span>
<span data-ttu-id="a3401-118">Evento Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="a3401-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="a3401-119">-ClassificationComment</span></span>
<span data-ttu-id="a3401-120">Commento Classificaiton di un problema.</span><span class="sxs-lookup"><span data-stu-id="a3401-120">Incident Classificaiton Comment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="a3401-121">-ClassificationReason</span></span>
<span data-ttu-id="a3401-122">Motivo Classificaiton di incidente.</span><span class="sxs-lookup"><span data-stu-id="a3401-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3401-123">-DefaultProfile</span></span>
<span data-ttu-id="a3401-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3401-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3401-125">-Description</span></span>
<span data-ttu-id="a3401-126">Descrizione.</span><span class="sxs-lookup"><span data-stu-id="a3401-126">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="a3401-127">-IncidentID</span></span>
<span data-ttu-id="a3401-128">ID incidente.</span><span class="sxs-lookup"><span data-stu-id="a3401-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3401-129">-InputObject</span></span>
<span data-ttu-id="a3401-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="a3401-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-131">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="a3401-131">-Label</span></span>
<span data-ttu-id="a3401-132">Etichette Incident.</span><span class="sxs-lookup"><span data-stu-id="a3401-132">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-133">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="a3401-133">-Owner</span></span>
<span data-ttu-id="a3401-134">Proprietario dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a3401-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3401-135">-ResourceGroupName</span></span>
<span data-ttu-id="a3401-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a3401-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3401-137">-ResourceId</span></span>
<span data-ttu-id="a3401-138">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a3401-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-139">-Gravità</span><span class="sxs-lookup"><span data-stu-id="a3401-139">-Severity</span></span>
<span data-ttu-id="a3401-140">Gravità degli incidenti.</span><span class="sxs-lookup"><span data-stu-id="a3401-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-141">-Stato</span><span class="sxs-lookup"><span data-stu-id="a3401-141">-Status</span></span>
<span data-ttu-id="a3401-142">Stato di incidente.</span><span class="sxs-lookup"><span data-stu-id="a3401-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-143">-Titolo</span><span class="sxs-lookup"><span data-stu-id="a3401-143">-Title</span></span>
<span data-ttu-id="a3401-144">Titolo dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a3401-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a3401-145">-WorkspaceName</span></span>
<span data-ttu-id="a3401-146">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a3401-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a3401-147">-Confirm</span></span>
<span data-ttu-id="a3401-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3401-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3401-149">-WhatIf</span></span>
<span data-ttu-id="a3401-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3401-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3401-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3401-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3401-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3401-152">CommonParameters</span></span>
<span data-ttu-id="a3401-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3401-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3401-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3401-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3401-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3401-155">INPUTS</span></span>

### <span data-ttu-id="a3401-156">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a3401-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="a3401-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a3401-157">System.String</span></span>

### <span data-ttu-id="a3401-158">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncidentLabel, Microsoft. Azure. PowerShell. cmdlet. SecurityInsights, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a3401-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a3401-159">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="a3401-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="a3401-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3401-160">OUTPUTS</span></span>

### <span data-ttu-id="a3401-161">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a3401-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="a3401-162">Note</span><span class="sxs-lookup"><span data-stu-id="a3401-162">NOTES</span></span>

## <span data-ttu-id="a3401-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3401-163">RELATED LINKS</span></span>
