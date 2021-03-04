---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 3bb0f095550394991bb74065e8d1c34c346b0c4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954894"
---
# <span data-ttu-id="307fa-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="307fa-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="307fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="307fa-102">SYNOPSIS</span></span>
<span data-ttu-id="307fa-103">Recupera una pianificazione del processo di distribuzione della configurazione del nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="307fa-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="307fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="307fa-104">SYNTAX</span></span>

### <span data-ttu-id="307fa-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="307fa-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="307fa-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="307fa-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="307fa-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="307fa-107">DESCRIPTION</span></span>
<span data-ttu-id="307fa-108">Il cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** distribuisce una configurazione del nodo APS Desired State Configuration (DSC) nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="307fa-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="307fa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="307fa-109">EXAMPLES</span></span>

### <span data-ttu-id="307fa-110">Esempio 1: Ottenere tutte le pianificazioni della distribuzione</span><span class="sxs-lookup"><span data-stu-id="307fa-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="307fa-111">Esempio 2: Ottenere una pianificazione della distribuzione</span><span class="sxs-lookup"><span data-stu-id="307fa-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="307fa-112">Il comando precedente distribuisce la configurazione del nodo DSC denominata "Config01.Node1" nella matrice bidimensionale specificata di Nomi nodo.</span><span class="sxs-lookup"><span data-stu-id="307fa-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="307fa-113">La distribuzione avviene a fasi.</span><span class="sxs-lookup"><span data-stu-id="307fa-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="307fa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="307fa-114">PARAMETERS</span></span>

### <span data-ttu-id="307fa-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="307fa-115">-AutomationAccountName</span></span>
<span data-ttu-id="307fa-116">Specifica il nome dell'account di automazione che contiene la configurazione DSC compilata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="307fa-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="307fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307fa-117">-DefaultProfile</span></span>
<span data-ttu-id="307fa-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="307fa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="307fa-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="307fa-119">-JobScheduleId</span></span>
<span data-ttu-id="307fa-120">Specifica l'ID pianificazione processo di un processo di distribuzione pianificato esistente.</span><span class="sxs-lookup"><span data-stu-id="307fa-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307fa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="307fa-121">-ResourceGroupName</span></span>
<span data-ttu-id="307fa-122">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="307fa-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="307fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307fa-123">CommonParameters</span></span>
<span data-ttu-id="307fa-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="307fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307fa-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="307fa-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307fa-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="307fa-126">INPUTS</span></span>

### <span data-ttu-id="307fa-127">System.Guid</span><span class="sxs-lookup"><span data-stu-id="307fa-127">System.Guid</span></span>

### <span data-ttu-id="307fa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="307fa-128">System.String</span></span>

## <span data-ttu-id="307fa-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="307fa-129">OUTPUTS</span></span>

### <span data-ttu-id="307fa-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="307fa-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="307fa-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="307fa-131">NOTES</span></span>

## <span data-ttu-id="307fa-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="307fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="307fa-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="307fa-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="307fa-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="307fa-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="307fa-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="307fa-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="307fa-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="307fa-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="307fa-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="307fa-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
