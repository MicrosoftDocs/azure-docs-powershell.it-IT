---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189126"
---
# <span data-ttu-id="a836a-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a836a-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="a836a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a836a-102">SYNOPSIS</span></span>
<span data-ttu-id="a836a-103">Aggiornare un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a836a-103">Update an Incident.</span></span>

## <span data-ttu-id="a836a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a836a-104">SYNTAX</span></span>

### <span data-ttu-id="a836a-105">IncidentId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a836a-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a836a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a836a-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a836a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a836a-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a836a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a836a-108">DESCRIPTION</span></span>
<span data-ttu-id="a836a-109">Il cmdlet **Update-AzSentinelIncident** aggiorna l'evento imprevisto nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="a836a-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="a836a-110">È possibile passare un **oggetto Evento** imprevisto come parametro o usando l'operatore della pipeline oppure in alternativa è possibile specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="a836a-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="a836a-111">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a836a-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a836a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a836a-112">EXAMPLES</span></span>

### <span data-ttu-id="a836a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a836a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="a836a-114">Il comando recupera l'evento imprevisto per *IncidentId* e imposta la *proprietà Severity* su *High.*</span><span class="sxs-lookup"><span data-stu-id="a836a-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="a836a-115">Tutte le altre proprietà rimangono invariate.</span><span class="sxs-lookup"><span data-stu-id="a836a-115">All other properties remain the same.</span></span>

## <span data-ttu-id="a836a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a836a-116">PARAMETERS</span></span>

### <span data-ttu-id="a836a-117">-Classificazione</span><span class="sxs-lookup"><span data-stu-id="a836a-117">-Classification</span></span>
<span data-ttu-id="a836a-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="a836a-118">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="a836a-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="a836a-119">-ClassificationComment</span></span>
<span data-ttu-id="a836a-120">Commento evento classificaiton.</span><span class="sxs-lookup"><span data-stu-id="a836a-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="a836a-121">-Classification Più.Seti</span><span class="sxs-lookup"><span data-stu-id="a836a-121">-ClassificationReason</span></span>
<span data-ttu-id="a836a-122">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="a836a-122">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="a836a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a836a-123">-DefaultProfile</span></span>
<span data-ttu-id="a836a-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a836a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a836a-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a836a-125">-Description</span></span>
<span data-ttu-id="a836a-126">Descrizione.</span><span class="sxs-lookup"><span data-stu-id="a836a-126">Description.</span></span>

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

### <span data-ttu-id="a836a-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="a836a-127">-IncidentID</span></span>
<span data-ttu-id="a836a-128">ID evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a836a-128">Incident Id.</span></span>

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

### <span data-ttu-id="a836a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a836a-129">-InputObject</span></span>
<span data-ttu-id="a836a-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="a836a-130">InputObject.</span></span>

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

### <span data-ttu-id="a836a-131">-Label</span><span class="sxs-lookup"><span data-stu-id="a836a-131">-Label</span></span>
<span data-ttu-id="a836a-132">Etichette degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a836a-132">Incident Labels.</span></span>

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

### <span data-ttu-id="a836a-133">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="a836a-133">-Owner</span></span>
<span data-ttu-id="a836a-134">Proprietario dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a836a-134">Incident Owner.</span></span>

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

### <span data-ttu-id="a836a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a836a-135">-ResourceGroupName</span></span>
<span data-ttu-id="a836a-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a836a-136">Resource group name.</span></span>

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

### <span data-ttu-id="a836a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a836a-137">-ResourceId</span></span>
<span data-ttu-id="a836a-138">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a836a-138">Resource Id.</span></span>

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

### <span data-ttu-id="a836a-139">-Gravità</span><span class="sxs-lookup"><span data-stu-id="a836a-139">-Severity</span></span>
<span data-ttu-id="a836a-140">Gravità dell'incidente.</span><span class="sxs-lookup"><span data-stu-id="a836a-140">Incident Severity.</span></span>

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

### <span data-ttu-id="a836a-141">-Stato</span><span class="sxs-lookup"><span data-stu-id="a836a-141">-Status</span></span>
<span data-ttu-id="a836a-142">Stato evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a836a-142">Incident Status.</span></span>

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

### <span data-ttu-id="a836a-143">-Title</span><span class="sxs-lookup"><span data-stu-id="a836a-143">-Title</span></span>
<span data-ttu-id="a836a-144">Titolo dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a836a-144">Incident Title.</span></span>

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

### <span data-ttu-id="a836a-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a836a-145">-WorkspaceName</span></span>
<span data-ttu-id="a836a-146">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a836a-146">Workspace Name.</span></span>

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

### <span data-ttu-id="a836a-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a836a-147">-Confirm</span></span>
<span data-ttu-id="a836a-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a836a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a836a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a836a-149">-WhatIf</span></span>
<span data-ttu-id="a836a-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a836a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a836a-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a836a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a836a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a836a-152">CommonParameters</span></span>
<span data-ttu-id="a836a-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a836a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a836a-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a836a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a836a-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="a836a-155">INPUTS</span></span>

### <span data-ttu-id="a836a-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a836a-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="a836a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="a836a-157">System.String</span></span>

### <span data-ttu-id="a836a-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a836a-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a836a-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="a836a-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="a836a-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a836a-160">OUTPUTS</span></span>

### <span data-ttu-id="a836a-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a836a-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="a836a-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="a836a-162">NOTES</span></span>

## <span data-ttu-id="a836a-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a836a-163">RELATED LINKS</span></span>
