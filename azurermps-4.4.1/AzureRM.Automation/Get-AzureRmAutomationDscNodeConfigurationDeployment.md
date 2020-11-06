---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 889318c911ae6f34b3655583ea2e9693da3bf80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517167"
---
# <span data-ttu-id="b1a4d-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b1a4d-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="b1a4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a4d-103">Ottiene le distribuzioni della configurazione del nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1a4d-104">SYNTAX</span></span>

### <span data-ttu-id="b1a4d-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1a4d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [[-Status] <String>] [[-StartTime] <DateTimeOffset>]
 [[-EndTime] <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a4d-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b1a4d-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a4d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1a4d-107">DESCRIPTION</span></span>
<span data-ttu-id="b1a4d-108">Il cmdlet **Get-AzureRmAutomationDscNodeConfigurationDeployment** distribuisce una configurazione di nodi DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="b1a4d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1a4d-109">EXAMPLES</span></span>

### <span data-ttu-id="b1a4d-110">Esempio 1: ottenere una distribuzione della configurazione di un nodo</span><span class="sxs-lookup"><span data-stu-id="b1a4d-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="b1a4d-111">Il comando precedente distribuisce la configurazione del nodo DSC denominata "Config01. node1" alla matrice bidimensionale specificata di nomi di nodo.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="b1a4d-112">La distribuzione avviene in modo graduale.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="b1a4d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1a4d-113">PARAMETERS</span></span>

### <span data-ttu-id="b1a4d-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="b1a4d-114">-JobId</span></span>
<span data-ttu-id="b1a4d-115">Specifica l'ID processo di un processo di distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-115">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="b1a4d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a4d-116">-ResourceGroupName</span></span>
<span data-ttu-id="b1a4d-117">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-117">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="b1a4d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b1a4d-118">-AutomationAccountName</span></span>
<span data-ttu-id="b1a4d-119">Specifica il nome dell'account di automazione che contiene la configurazione DSC che questo cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-119">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="b1a4d-120">-Stato</span><span class="sxs-lookup"><span data-stu-id="b1a4d-120">-Status</span></span>
<span data-ttu-id="b1a4d-121">Stato del filtro processo.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-121">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a4d-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b1a4d-122">-StartTime</span></span>
<span data-ttu-id="b1a4d-123">Filtro ora inizio.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-123">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a4d-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b1a4d-124">-EndTime</span></span>
<span data-ttu-id="b1a4d-125">Filtro ora di fine.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-125">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a4d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a4d-126">-DefaultProfile</span></span>
<span data-ttu-id="b1a4d-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a4d-128">CommonParameters</span></span>
<span data-ttu-id="b1a4d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a4d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a4d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a4d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1a4d-131">INPUTS</span></span>

## <span data-ttu-id="b1a4d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1a4d-132">OUTPUTS</span></span>

### <span data-ttu-id="b1a4d-133">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b1a4d-133">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="b1a4d-134">Note</span><span class="sxs-lookup"><span data-stu-id="b1a4d-134">NOTES</span></span>

## <span data-ttu-id="b1a4d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1a4d-135">RELATED LINKS</span></span>

[<span data-ttu-id="b1a4d-136">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b1a4d-136">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="b1a4d-137">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1a4d-137">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="b1a4d-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b1a4d-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="b1a4d-139">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b1a4d-139">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="b1a4d-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="b1a4d-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
