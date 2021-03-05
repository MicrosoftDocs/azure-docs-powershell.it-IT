---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: 6cb65832484c7038f5740c481836d8fe889ebc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005646"
---
# <span data-ttu-id="c9fb2-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="c9fb2-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="c9fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="c9fb2-103">Creare un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-103">Create an Incident.</span></span>

## <span data-ttu-id="c9fb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9fb2-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9fb2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="c9fb2-106">Il cmdlet **New-AzSentinelIncident** crea un evento imprevisto dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="c9fb2-107">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c9fb2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9fb2-108">EXAMPLES</span></span>

### <span data-ttu-id="c9fb2-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9fb2-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="c9fb2-110">Questo esempio crea un evento **imprevisto** nell'area di lavoro specificata e quindi lo archivia nella $Incident variabile.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="c9fb2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9fb2-111">PARAMETERS</span></span>

### <span data-ttu-id="c9fb2-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="c9fb2-112">-ClassificationComment</span></span>
<span data-ttu-id="c9fb2-113">Commento evento classificaiton.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="c9fb2-114">-Classification Syeis</span><span class="sxs-lookup"><span data-stu-id="c9fb2-114">-ClassificationReason</span></span>
<span data-ttu-id="c9fb2-115">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fb2-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="c9fb2-116">-Classificaton</span></span>
<span data-ttu-id="c9fb2-117">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fb2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9fb2-118">-DefaultProfile</span></span>
<span data-ttu-id="c9fb2-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fb2-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9fb2-120">-Description</span></span>
<span data-ttu-id="c9fb2-121">Descrizione.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-121">Description.</span></span>

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

### <span data-ttu-id="c9fb2-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="c9fb2-122">-IncidentId</span></span>
<span data-ttu-id="c9fb2-123">ID evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-123">Incident Id.</span></span>

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

### <span data-ttu-id="c9fb2-124">-Label</span><span class="sxs-lookup"><span data-stu-id="c9fb2-124">-Label</span></span>
<span data-ttu-id="c9fb2-125">Etichette degli eventi.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-125">Incident Labels.</span></span>

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

### <span data-ttu-id="c9fb2-126">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="c9fb2-126">-Owner</span></span>
<span data-ttu-id="c9fb2-127">Proprietario dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9fb2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9fb2-128">-ResourceGroupName</span></span>
<span data-ttu-id="c9fb2-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-129">Resource group name.</span></span>

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

### <span data-ttu-id="c9fb2-130">-Gravità</span><span class="sxs-lookup"><span data-stu-id="c9fb2-130">-Severity</span></span>
<span data-ttu-id="c9fb2-131">Gravità dell'incidente.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fb2-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="c9fb2-132">-Status</span></span>
<span data-ttu-id="c9fb2-133">Stato evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fb2-134">-Title</span><span class="sxs-lookup"><span data-stu-id="c9fb2-134">-Title</span></span>
<span data-ttu-id="c9fb2-135">Titolo dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-135">Incident Title.</span></span>

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

### <span data-ttu-id="c9fb2-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c9fb2-136">-WorkspaceName</span></span>
<span data-ttu-id="c9fb2-137">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-137">Workspace Name.</span></span>

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

### <span data-ttu-id="c9fb2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9fb2-138">-Confirm</span></span>
<span data-ttu-id="c9fb2-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9fb2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9fb2-140">-WhatIf</span></span>
<span data-ttu-id="c9fb2-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9fb2-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9fb2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fb2-143">CommonParameters</span></span>
<span data-ttu-id="c9fb2-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fb2-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9fb2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fb2-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9fb2-146">INPUTS</span></span>

### <span data-ttu-id="c9fb2-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c9fb2-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="c9fb2-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="c9fb2-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="c9fb2-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9fb2-149">OUTPUTS</span></span>

### <span data-ttu-id="c9fb2-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="c9fb2-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="c9fb2-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9fb2-151">NOTES</span></span>

## <span data-ttu-id="c9fb2-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9fb2-152">RELATED LINKS</span></span>
