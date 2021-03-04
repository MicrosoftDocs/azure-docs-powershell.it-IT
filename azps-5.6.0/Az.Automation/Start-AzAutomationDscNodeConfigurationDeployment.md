---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 477b8f5853d9a5dbe3dd030e7419316825088807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957710"
---
# <span data-ttu-id="1dc2d-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1dc2d-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="1dc2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc2d-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc2d-103">Distribuisce la configurazione di un nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="1dc2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dc2d-104">SYNTAX</span></span>

### <span data-ttu-id="1dc2d-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dc2d-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc2d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1dc2d-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc2d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1dc2d-107">DESCRIPTION</span></span>
<span data-ttu-id="1dc2d-108">Il cmdlet **Start-AzAutomationDscNodeConfigurationDeployment** distribuisce una configurazione del nodo Desired State Configuration (DSC) in Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="1dc2d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dc2d-109">EXAMPLES</span></span>

### <span data-ttu-id="1dc2d-110">Esempio 1: Distribuire una configurazione del nodo DSC di Azure nell'automazione</span><span class="sxs-lookup"><span data-stu-id="1dc2d-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="1dc2d-111">Il comando precedente distribuisce la configurazione del nodo DSC denominata "Config01.Node1" nella matrice bidimensionale specificata di Nomi nodo.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="1dc2d-112">La distribuzione avviene a fasi.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="1dc2d-113">Esempio 2: Pianificare la distribuzione di una configurazione del nodo DSC di Azure nell'automazione</span><span class="sxs-lookup"><span data-stu-id="1dc2d-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="1dc2d-114">Il comando precedente pianifica una distribuzione di una configurazione del nodo DSC denominata "Config01.Node1" nella matrice bidimensionale specificata di nomi di nodo.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="1dc2d-115">La distribuzione avviene in fasi e verrà eseguita in base alla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="1dc2d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dc2d-116">PARAMETERS</span></span>

### <span data-ttu-id="1dc2d-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1dc2d-117">-AutomationAccountName</span></span>
<span data-ttu-id="1dc2d-118">Specifica il nome dell'account di automazione che contiene la configurazione DSC compilata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="1dc2d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc2d-119">-DefaultProfile</span></span>
<span data-ttu-id="1dc2d-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1dc2d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dc2d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc2d-121">-Force</span></span>
<span data-ttu-id="1dc2d-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="1dc2d-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc2d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc2d-123">-InputObject</span></span>
<span data-ttu-id="1dc2d-124">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="1dc2d-124">Input object for Piping</span></span>

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

### <span data-ttu-id="1dc2d-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1dc2d-125">-NodeConfigurationName</span></span>
<span data-ttu-id="1dc2d-126">Specifica il nome della configurazione del nodo DSC distribuito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc2d-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="1dc2d-127">-NodeName</span></span>
<span data-ttu-id="1dc2d-128">Specifica i nomi dei nodi in cui verrà distribuita la configurazione nodo.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc2d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc2d-129">-ResourceGroupName</span></span>
<span data-ttu-id="1dc2d-130">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="1dc2d-131">-Pianificazione</span><span class="sxs-lookup"><span data-stu-id="1dc2d-131">-Schedule</span></span>
<span data-ttu-id="1dc2d-132">Oggetto Automation Schedule per pianificare il processo di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc2d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dc2d-133">-Confirm</span></span>
<span data-ttu-id="1dc2d-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc2d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc2d-135">-WhatIf</span></span>
<span data-ttu-id="1dc2d-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc2d-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc2d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc2d-138">CommonParameters</span></span>
<span data-ttu-id="1dc2d-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc2d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc2d-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc2d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc2d-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="1dc2d-141">INPUTS</span></span>

### <span data-ttu-id="1dc2d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1dc2d-142">System.String</span></span>

### <span data-ttu-id="1dc2d-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1dc2d-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="1dc2d-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dc2d-144">OUTPUTS</span></span>

### <span data-ttu-id="1dc2d-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1dc2d-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="1dc2d-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="1dc2d-146">NOTES</span></span>

## <span data-ttu-id="1dc2d-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dc2d-147">RELATED LINKS</span></span>

[<span data-ttu-id="1dc2d-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="1dc2d-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="1dc2d-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dc2d-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="1dc2d-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1dc2d-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="1dc2d-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1dc2d-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="1dc2d-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="1dc2d-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="1dc2d-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1dc2d-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
