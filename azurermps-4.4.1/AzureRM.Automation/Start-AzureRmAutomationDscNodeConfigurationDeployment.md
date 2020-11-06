---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: f822f6060827718945f12f998662caeee3b349eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519637"
---
# <span data-ttu-id="f7b32-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f7b32-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="f7b32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7b32-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b32-103">Distribuisce una configurazione del nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="f7b32-103">Deploys a DSC Node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7b32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7b32-104">SYNTAX</span></span>

### <span data-ttu-id="f7b32-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7b32-105">ByAll (Default)</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7b32-106">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="f7b32-106">ByByInputObject</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7b32-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7b32-107">DESCRIPTION</span></span>
<span data-ttu-id="f7b32-108">Il cmdlet **Start-AzureRmAutomationDscNodeConfigurationDeployment** distribuisce una configurazione di nodo DSC (Desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f7b32-108">The **Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="f7b32-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7b32-109">EXAMPLES</span></span>

### <span data-ttu-id="f7b32-110">Esempio 1: distribuire una configurazione di nodi DSC di Azure nell'automazione</span><span class="sxs-lookup"><span data-stu-id="f7b32-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="f7b32-111">Il comando precedente distribuisce la configurazione del nodo DSC denominata "Config01. node1" alla matrice bidimensionale specificata di nomi di nodo.</span><span class="sxs-lookup"><span data-stu-id="f7b32-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="f7b32-112">La distribuzione avviene in modo graduale.</span><span class="sxs-lookup"><span data-stu-id="f7b32-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="f7b32-113">Esempio 2: pianificare una distribuzione della configurazione di un nodo DSC di Azure nell'automazione</span><span class="sxs-lookup"><span data-stu-id="f7b32-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzureRmAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="f7b32-114">Il comando precedente pianifica una distribuzione di una configurazione di nodi DSC denominata "Config01. node1" alla matrice bidimensionale specificata di nomi di nodo.</span><span class="sxs-lookup"><span data-stu-id="f7b32-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="f7b32-115">La distribuzione avviene in modalità a fasi e verrà eseguita in base alla programmazione.</span><span class="sxs-lookup"><span data-stu-id="f7b32-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="f7b32-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7b32-116">PARAMETERS</span></span>

### <span data-ttu-id="f7b32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b32-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7b32-118">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="f7b32-118">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="f7b32-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f7b32-119">-AutomationAccountName</span></span>
<span data-ttu-id="f7b32-120">Specifica il nome dell'account di automazione che contiene la configurazione DSC che questo cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="f7b32-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="f7b32-121">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f7b32-121">-NodeConfigurationName</span></span>
<span data-ttu-id="f7b32-122">Specifica il nome della configurazione del nodo DSC che viene distribuita da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b32-122">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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
Parameter Sets: ByByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b32-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="f7b32-123">-NodeName</span></span>
<span data-ttu-id="f7b32-124">Specifica i nomi dei nodi a cui verrà distribuita la configurazione del nodo.</span><span class="sxs-lookup"><span data-stu-id="f7b32-124">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="f7b32-125">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="f7b32-125">-Schedule</span></span>
<span data-ttu-id="f7b32-126">Oggetto pianificazione automazione per pianificare il processo di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f7b32-126">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="f7b32-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f7b32-127">-Force</span></span>
<span data-ttu-id="f7b32-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="f7b32-128">ps_force</span></span>

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

### <span data-ttu-id="f7b32-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7b32-129">-Confirm</span></span>
<span data-ttu-id="f7b32-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b32-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b32-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b32-131">-WhatIf</span></span>
<span data-ttu-id="f7b32-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7b32-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b32-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7b32-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b32-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b32-134">-DefaultProfile</span></span>
<span data-ttu-id="f7b32-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b32-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b32-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7b32-136">-InputObject</span></span>
<span data-ttu-id="f7b32-137">Oggetto di input per piping.</span><span class="sxs-lookup"><span data-stu-id="f7b32-137">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b32-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b32-138">CommonParameters</span></span>
<span data-ttu-id="f7b32-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b32-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b32-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b32-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b32-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7b32-141">INPUTS</span></span>

## <span data-ttu-id="f7b32-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7b32-142">OUTPUTS</span></span>

### <span data-ttu-id="f7b32-143">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f7b32-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="f7b32-144">Note</span><span class="sxs-lookup"><span data-stu-id="f7b32-144">NOTES</span></span>

## <span data-ttu-id="f7b32-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7b32-145">RELATED LINKS</span></span>

[<span data-ttu-id="f7b32-146">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f7b32-146">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="f7b32-147">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7b32-147">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="f7b32-148">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f7b32-148">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f7b32-149">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f7b32-149">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f7b32-150">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="f7b32-150">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="f7b32-151">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f7b32-151">New-AzureRmAutomationSchedule</span></span>](./New-AzureRmAutomationSchedule.md)
