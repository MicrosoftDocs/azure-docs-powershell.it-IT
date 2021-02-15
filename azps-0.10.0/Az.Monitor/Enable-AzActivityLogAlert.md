---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 89a2d96b79fa771b18e085978c85c7a98da4e9b5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398768"
---
# <span data-ttu-id="0eb31-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0eb31-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="0eb31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb31-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb31-103">Abilita un avviso del log attività e ne imposta i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="0eb31-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="0eb31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0eb31-104">SYNTAX</span></span>

### <span data-ttu-id="0eb31-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0eb31-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb31-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="0eb31-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb31-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="0eb31-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0eb31-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0eb31-108">DESCRIPTION</span></span>
<span data-ttu-id="0eb31-109">Il cmdlet **Enable-AzActivityLogAlert** consente di abilitare un avviso del log attività e di impostarne i tag.</span><span class="sxs-lookup"><span data-stu-id="0eb31-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="0eb31-110">Questo cmdlet implementa il modello ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di applicare effettivamente le patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="0eb31-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="0eb31-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0eb31-111">EXAMPLES</span></span>

### <span data-ttu-id="0eb31-112">Esempio 1: Abilitare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="0eb31-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="0eb31-113">Questo comando abilita l'avviso del log attività denominato avviso1 nel gruppo di risorse Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="0eb31-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="0eb31-114">Esempio 2: Abilitare un avviso del log attività usando un oggetto PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="0eb31-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="0eb31-115">Questo comando abilita un avviso del log attività denominato avviso1.</span><span class="sxs-lookup"><span data-stu-id="0eb31-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="0eb31-116">A questo scopo usa un oggetto PSActivityLogAlertResource come argomento di input.</span><span class="sxs-lookup"><span data-stu-id="0eb31-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="0eb31-117">Esempio 3: Abilitare ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eb31-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="0eb31-118">Questo comando abilita ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="0eb31-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="0eb31-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eb31-119">PARAMETERS</span></span>

### <span data-ttu-id="0eb31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb31-120">-DefaultProfile</span></span>
<span data-ttu-id="0eb31-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0eb31-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eb31-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb31-122">-InputObject</span></span>
<span data-ttu-id="0eb31-123">Imposta la proprietà tag InputObject della chiamata per estrarre il nome richiesto, il nome del gruppo di risorse e le proprietà dei tag facoltativi.</span><span class="sxs-lookup"><span data-stu-id="0eb31-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb31-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0eb31-124">-Name</span></span>
<span data-ttu-id="0eb31-125">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="0eb31-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb31-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb31-126">-ResourceGroupName</span></span>
<span data-ttu-id="0eb31-127">Nome del gruppo di risorse in cui si trova la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="0eb31-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb31-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eb31-128">-ResourceId</span></span>
<span data-ttu-id="0eb31-129">Imposta la proprietà tag ResourceId della chiamata per estrarre il nome richiesto e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0eb31-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb31-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0eb31-130">-Confirm</span></span>
<span data-ttu-id="0eb31-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb31-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb31-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb31-132">-WhatIf</span></span>
<span data-ttu-id="0eb31-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0eb31-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eb31-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0eb31-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb31-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb31-135">CommonParameters</span></span>
<span data-ttu-id="0eb31-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb31-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb31-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0eb31-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb31-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="0eb31-138">INPUTS</span></span>

### <span data-ttu-id="0eb31-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0eb31-139">System.String</span></span>

### <span data-ttu-id="0eb31-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="0eb31-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="0eb31-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0eb31-141">OUTPUTS</span></span>

### <span data-ttu-id="0eb31-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="0eb31-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="0eb31-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="0eb31-143">NOTES</span></span>

## <span data-ttu-id="0eb31-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0eb31-144">RELATED LINKS</span></span>

[<span data-ttu-id="0eb31-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0eb31-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="0eb31-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0eb31-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="0eb31-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0eb31-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="0eb31-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="0eb31-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="0eb31-149">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0eb31-149">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
