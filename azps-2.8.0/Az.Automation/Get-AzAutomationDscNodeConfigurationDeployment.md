---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 4810fe549f0edd109d83391e3df56916ec48b8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675816"
---
# <span data-ttu-id="c24e9-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c24e9-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="c24e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c24e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c24e9-103">Ottiene le distribuzioni della configurazione del nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="c24e9-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="c24e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c24e9-104">SYNTAX</span></span>

### <span data-ttu-id="c24e9-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c24e9-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c24e9-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="c24e9-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c24e9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c24e9-107">DESCRIPTION</span></span>
<span data-ttu-id="c24e9-108">Il cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** distribuisce una configurazione di nodi DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c24e9-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="c24e9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c24e9-109">EXAMPLES</span></span>

### <span data-ttu-id="c24e9-110">Esempio 1: ottenere una distribuzione della configurazione di un nodo</span><span class="sxs-lookup"><span data-stu-id="c24e9-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="c24e9-111">Il comando precedente distribuisce la configurazione del nodo DSC denominata "Config01. node1" alla matrice bidimensionale specificata di nomi di nodo.</span><span class="sxs-lookup"><span data-stu-id="c24e9-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="c24e9-112">La distribuzione avviene in modo graduale.</span><span class="sxs-lookup"><span data-stu-id="c24e9-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="c24e9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c24e9-113">PARAMETERS</span></span>

### <span data-ttu-id="c24e9-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c24e9-114">-AutomationAccountName</span></span>
<span data-ttu-id="c24e9-115">Specifica il nome dell'account di automazione che contiene la configurazione DSC che questo cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="c24e9-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="c24e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24e9-116">-DefaultProfile</span></span>
<span data-ttu-id="c24e9-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c24e9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c24e9-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c24e9-118">-EndTime</span></span>
<span data-ttu-id="c24e9-119">Filtro ora di fine.</span><span class="sxs-lookup"><span data-stu-id="c24e9-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24e9-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="c24e9-120">-JobId</span></span>
<span data-ttu-id="c24e9-121">Specifica l'ID processo di un processo di distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="c24e9-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="c24e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c24e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="c24e9-123">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="c24e9-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="c24e9-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c24e9-124">-StartTime</span></span>
<span data-ttu-id="c24e9-125">Filtro ora inizio.</span><span class="sxs-lookup"><span data-stu-id="c24e9-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24e9-126">-Stato</span><span class="sxs-lookup"><span data-stu-id="c24e9-126">-Status</span></span>
<span data-ttu-id="c24e9-127">Stato del filtro processo.</span><span class="sxs-lookup"><span data-stu-id="c24e9-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24e9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24e9-128">CommonParameters</span></span>
<span data-ttu-id="c24e9-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24e9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24e9-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24e9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24e9-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c24e9-131">INPUTS</span></span>

### <span data-ttu-id="c24e9-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c24e9-132">System.Guid</span></span>

### <span data-ttu-id="c24e9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c24e9-133">System.String</span></span>

## <span data-ttu-id="c24e9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c24e9-134">OUTPUTS</span></span>

### <span data-ttu-id="c24e9-135">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c24e9-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="c24e9-136">Note</span><span class="sxs-lookup"><span data-stu-id="c24e9-136">NOTES</span></span>

## <span data-ttu-id="c24e9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c24e9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c24e9-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="c24e9-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="c24e9-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24e9-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="c24e9-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c24e9-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c24e9-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c24e9-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c24e9-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="c24e9-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)