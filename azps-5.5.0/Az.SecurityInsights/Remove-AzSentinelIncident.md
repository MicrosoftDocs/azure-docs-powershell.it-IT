---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197886"
---
# <span data-ttu-id="7515b-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="7515b-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="7515b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7515b-102">SYNOPSIS</span></span>
<span data-ttu-id="7515b-103">Eliminare un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="7515b-103">Delete an Incident.</span></span>

## <span data-ttu-id="7515b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7515b-104">SYNTAX</span></span>

### <span data-ttu-id="7515b-105">IncidentId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7515b-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7515b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7515b-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7515b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7515b-107">DESCRIPTION</span></span>
<span data-ttu-id="7515b-108">Il cmdlet **Remove-AzSentinelIncident** elimina definitivamente un evento imprevisto da un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="7515b-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="7515b-109">È possibile passare un **oggetto Evento** imprevisto usando l'operatore della pipeline oppure è possibile specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="7515b-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="7515b-110">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="7515b-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="7515b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7515b-111">EXAMPLES</span></span>

### <span data-ttu-id="7515b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7515b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="7515b-113">Questo comando rimuove l'evento imprevisto dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7515b-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="7515b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7515b-114">PARAMETERS</span></span>

### <span data-ttu-id="7515b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7515b-115">-DefaultProfile</span></span>
<span data-ttu-id="7515b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7515b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7515b-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="7515b-117">-IncidentId</span></span>
<span data-ttu-id="7515b-118">ID evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="7515b-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7515b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7515b-119">-InputObject</span></span>
<span data-ttu-id="7515b-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="7515b-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7515b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7515b-121">-PassThru</span></span>
<span data-ttu-id="7515b-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="7515b-122">PassThru</span></span>

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

### <span data-ttu-id="7515b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7515b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7515b-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7515b-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7515b-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7515b-125">-WorkspaceName</span></span>
<span data-ttu-id="7515b-126">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7515b-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7515b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7515b-127">-Confirm</span></span>
<span data-ttu-id="7515b-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7515b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7515b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7515b-129">-WhatIf</span></span>
<span data-ttu-id="7515b-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7515b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7515b-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7515b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7515b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7515b-132">CommonParameters</span></span>
<span data-ttu-id="7515b-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7515b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7515b-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7515b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7515b-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="7515b-135">INPUTS</span></span>

### <span data-ttu-id="7515b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7515b-136">System.String</span></span>
### <span data-ttu-id="7515b-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="7515b-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="7515b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7515b-138">OUTPUTS</span></span>

### <span data-ttu-id="7515b-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7515b-139">System.Boolean</span></span>
## <span data-ttu-id="7515b-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="7515b-140">NOTES</span></span>

## <span data-ttu-id="7515b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7515b-141">RELATED LINKS</span></span>
