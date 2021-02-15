---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195262"
---
# <span data-ttu-id="edf23-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="edf23-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="edf23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf23-102">SYNOPSIS</span></span>
<span data-ttu-id="edf23-103">Interrompe la distribuzione della configurazione del nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="edf23-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="edf23-104">Interrompe solo il processo di distribuzione corrente, ma non annulla l'assegnazione di configurazioni di nodo già assegnate.</span><span class="sxs-lookup"><span data-stu-id="edf23-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="edf23-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edf23-105">SYNTAX</span></span>

### <span data-ttu-id="edf23-106">ByJobId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="edf23-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edf23-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="edf23-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edf23-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="edf23-108">DESCRIPTION</span></span>
<span data-ttu-id="edf23-109">Il cmdlet **Stop-AzAutomationDscNodeConfigurationDeployment** interrompe la distribuzione della configurazione del nodo Desired State Configuration (DSC) nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="edf23-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="edf23-110">Interrompe l'assegnazione della configurazione del nodo a gruppi di nodi, se ne restano altri da assegnare, ma non annulla l'assegnazione di nodi già assegnati.</span><span class="sxs-lookup"><span data-stu-id="edf23-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="edf23-111">Per annullare la registrazione di un processo pianificato, usare [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) con JobScheduleId per annullare l'assegnazione di un processo pianificato esistente.</span><span class="sxs-lookup"><span data-stu-id="edf23-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="edf23-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edf23-112">EXAMPLES</span></span>

### <span data-ttu-id="edf23-113">Esempio 1: Distribuire una configurazione del nodo DSC di Azure in Automazione</span><span class="sxs-lookup"><span data-stu-id="edf23-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="edf23-114">Il comando precedente interrompe il processo di distribuzione della configurazione del nodo DSC con jobId passato.</span><span class="sxs-lookup"><span data-stu-id="edf23-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="edf23-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edf23-115">PARAMETERS</span></span>

### <span data-ttu-id="edf23-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="edf23-116">-AutomationAccountName</span></span>
<span data-ttu-id="edf23-117">Specifica il nome dell'account di automazione che contiene la configurazione DSC compilata da questo cmdlet</span><span class="sxs-lookup"><span data-stu-id="edf23-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf23-118">-DefaultProfile</span></span>
<span data-ttu-id="edf23-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="edf23-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edf23-120">-Force</span><span class="sxs-lookup"><span data-stu-id="edf23-120">-Force</span></span>
<span data-ttu-id="edf23-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="edf23-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf23-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edf23-122">-InputObject</span></span>
<span data-ttu-id="edf23-123">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="edf23-123">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edf23-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="edf23-124">-JobId</span></span>
<span data-ttu-id="edf23-125">Specifica l'ID processo di un processo di distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="edf23-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf23-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edf23-126">-PassThru</span></span>
<span data-ttu-id="edf23-127">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="edf23-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="edf23-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="edf23-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="edf23-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf23-129">-ResourceGroupName</span></span>
<span data-ttu-id="edf23-130">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="edf23-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf23-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edf23-131">-Confirm</span></span>
<span data-ttu-id="edf23-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edf23-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf23-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf23-133">-WhatIf</span></span>
<span data-ttu-id="edf23-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edf23-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edf23-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edf23-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf23-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf23-136">CommonParameters</span></span>
<span data-ttu-id="edf23-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf23-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf23-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edf23-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf23-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="edf23-139">INPUTS</span></span>

### <span data-ttu-id="edf23-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="edf23-140">System.Guid</span></span>

### <span data-ttu-id="edf23-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="edf23-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="edf23-142">System.String</span><span class="sxs-lookup"><span data-stu-id="edf23-142">System.String</span></span>

## <span data-ttu-id="edf23-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edf23-143">OUTPUTS</span></span>

### <span data-ttu-id="edf23-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edf23-144">System.Boolean</span></span>

## <span data-ttu-id="edf23-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="edf23-145">NOTES</span></span>

## <span data-ttu-id="edf23-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edf23-146">RELATED LINKS</span></span>

[<span data-ttu-id="edf23-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="edf23-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="edf23-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="edf23-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="edf23-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="edf23-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="edf23-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="edf23-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="edf23-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="edf23-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
