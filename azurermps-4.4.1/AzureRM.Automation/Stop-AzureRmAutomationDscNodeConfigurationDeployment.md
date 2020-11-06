---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3ddaf0d4ae609305bf9740fbbe38a5fddd414e18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520798"
---
# <span data-ttu-id="7abb5-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7abb5-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="7abb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7abb5-102">SYNOPSIS</span></span>
<span data-ttu-id="7abb5-103">Interrompe una distribuzione della configurazione del nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="7abb5-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="7abb5-104">Interrompe solo il processo di distribuzione corrente, ma non annulla l'assegnazione delle configurazioni di nodi già assegnate.</span><span class="sxs-lookup"><span data-stu-id="7abb5-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7abb5-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7abb5-105">SYNTAX</span></span>

### <span data-ttu-id="7abb5-106">ByJobId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7abb5-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7abb5-107">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="7abb5-107">ByByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7abb5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7abb5-108">DESCRIPTION</span></span>
<span data-ttu-id="7abb5-109">Il cmdlet **Stop-AzureRmAutomationDscNodeConfigurationDeployment** interrompe la distribuzione di una configurazione del nodo DSC (Desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7abb5-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="7abb5-110">Interrompe l'assegnazione della configurazione dei nodi a gruppi di nodi, se ne restano da assegnare, ma non annulla l'assegnazione di nodi già assegnati.</span><span class="sxs-lookup"><span data-stu-id="7abb5-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="7abb5-111">Per annullare la registrazione di un processo programmato, usare l' [annullamento della registrazione-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) con JobScheduleId per annullare l'assegnazione di un processo programmato esistente.</span><span class="sxs-lookup"><span data-stu-id="7abb5-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="7abb5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7abb5-112">EXAMPLES</span></span>

### <span data-ttu-id="7abb5-113">Esempio 1: distribuire una configurazione di nodi DSC di Azure nell'automazione</span><span class="sxs-lookup"><span data-stu-id="7abb5-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="7abb5-114">Il comando precedente interrompe il processo di distribuzione della configurazione del nodo DSC con il jobId passato.</span><span class="sxs-lookup"><span data-stu-id="7abb5-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="7abb5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7abb5-115">PARAMETERS</span></span>

### <span data-ttu-id="7abb5-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7abb5-116">-AutomationAccountName</span></span>
<span data-ttu-id="7abb5-117">Specifica il nome dell'account di automazione che contiene la configurazione DSC che questo cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="7abb5-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7abb5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7abb5-118">-ResourceGroupName</span></span>
<span data-ttu-id="7abb5-119">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="7abb5-119">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="7abb5-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="7abb5-120">-JobId</span></span>
<span data-ttu-id="7abb5-121">Specifica l'ID processo di un processo di distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="7abb5-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="7abb5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7abb5-122">-PassThru</span></span>
<span data-ttu-id="7abb5-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="7abb5-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7abb5-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7abb5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7abb5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7abb5-125">-Force</span></span>
<span data-ttu-id="7abb5-126">ps_force</span><span class="sxs-lookup"><span data-stu-id="7abb5-126">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7abb5-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7abb5-127">-Confirm</span></span>
<span data-ttu-id="7abb5-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7abb5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7abb5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7abb5-129">-WhatIf</span></span>
<span data-ttu-id="7abb5-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7abb5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7abb5-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7abb5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7abb5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abb5-132">-DefaultProfile</span></span>
<span data-ttu-id="7abb5-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7abb5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7abb5-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7abb5-134">-InputObject</span></span>
<span data-ttu-id="7abb5-135">Oggetto di input per piping.</span><span class="sxs-lookup"><span data-stu-id="7abb5-135">Input object for Piping.</span></span>

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

### <span data-ttu-id="7abb5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abb5-136">CommonParameters</span></span>
<span data-ttu-id="7abb5-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7abb5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abb5-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abb5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abb5-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7abb5-139">INPUTS</span></span>

## <span data-ttu-id="7abb5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7abb5-140">OUTPUTS</span></span>

## <span data-ttu-id="7abb5-141">Note</span><span class="sxs-lookup"><span data-stu-id="7abb5-141">NOTES</span></span>

## <span data-ttu-id="7abb5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7abb5-142">RELATED LINKS</span></span>

[<span data-ttu-id="7abb5-143">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7abb5-143">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="7abb5-144">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7abb5-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="7abb5-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7abb5-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="7abb5-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7abb5-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="7abb5-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="7abb5-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
