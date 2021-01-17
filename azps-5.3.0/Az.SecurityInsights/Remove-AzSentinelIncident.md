---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486167"
---
# <span data-ttu-id="bcefe-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="bcefe-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="bcefe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcefe-102">SYNOPSIS</span></span>
<span data-ttu-id="bcefe-103">Eliminare un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="bcefe-103">Delete an Incident.</span></span>

## <span data-ttu-id="bcefe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcefe-104">SYNTAX</span></span>

### <span data-ttu-id="bcefe-105">IncidentId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcefe-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcefe-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bcefe-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcefe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcefe-107">DESCRIPTION</span></span>
<span data-ttu-id="bcefe-108">Il cmdlet **Remove-AzSentinelIncident** Elimina definitivamente un evento incidentato da un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="bcefe-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="bcefe-109">Puoi passare un oggetto **Incident** usando l'operatore pipeline o in alternativa puoi specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="bcefe-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="bcefe-110">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="bcefe-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="bcefe-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcefe-111">EXAMPLES</span></span>

### <span data-ttu-id="bcefe-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bcefe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="bcefe-113">Questo comando rimuove l'evento Incident dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bcefe-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="bcefe-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcefe-114">PARAMETERS</span></span>

### <span data-ttu-id="bcefe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcefe-115">-DefaultProfile</span></span>
<span data-ttu-id="bcefe-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcefe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcefe-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="bcefe-117">-IncidentId</span></span>
<span data-ttu-id="bcefe-118">ID incidente.</span><span class="sxs-lookup"><span data-stu-id="bcefe-118">Incident Id.</span></span>

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

### <span data-ttu-id="bcefe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcefe-119">-InputObject</span></span>
<span data-ttu-id="bcefe-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="bcefe-120">InputObject.</span></span>

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

### <span data-ttu-id="bcefe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcefe-121">-PassThru</span></span>
<span data-ttu-id="bcefe-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="bcefe-122">PassThru</span></span>

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

### <span data-ttu-id="bcefe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcefe-123">-ResourceGroupName</span></span>
<span data-ttu-id="bcefe-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcefe-124">Resource group name.</span></span>

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

### <span data-ttu-id="bcefe-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bcefe-125">-WorkspaceName</span></span>
<span data-ttu-id="bcefe-126">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bcefe-126">Workspace Name.</span></span>

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

### <span data-ttu-id="bcefe-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bcefe-127">-Confirm</span></span>
<span data-ttu-id="bcefe-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcefe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcefe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcefe-129">-WhatIf</span></span>
<span data-ttu-id="bcefe-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcefe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcefe-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcefe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcefe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcefe-132">CommonParameters</span></span>
<span data-ttu-id="bcefe-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcefe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcefe-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcefe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcefe-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcefe-135">INPUTS</span></span>

### <span data-ttu-id="bcefe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bcefe-136">System.String</span></span>
### <span data-ttu-id="bcefe-137">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="bcefe-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="bcefe-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcefe-138">OUTPUTS</span></span>

### <span data-ttu-id="bcefe-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcefe-139">System.Boolean</span></span>
## <span data-ttu-id="bcefe-140">Note</span><span class="sxs-lookup"><span data-stu-id="bcefe-140">NOTES</span></span>

## <span data-ttu-id="bcefe-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcefe-141">RELATED LINKS</span></span>
