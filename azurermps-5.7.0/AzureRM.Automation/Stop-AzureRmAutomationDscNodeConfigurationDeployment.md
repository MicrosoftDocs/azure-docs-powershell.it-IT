---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 17106fed79fdec90bad6615560553dcdb5d46703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687048"
---
# <span data-ttu-id="61a68-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="61a68-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="61a68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61a68-102">SYNOPSIS</span></span>
<span data-ttu-id="61a68-103">Interrompe una distribuzione della configurazione del nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="61a68-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="61a68-104">Interrompe solo il processo di distribuzione corrente, ma non annulla l'assegnazione delle configurazioni di nodi già assegnate.</span><span class="sxs-lookup"><span data-stu-id="61a68-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61a68-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61a68-105">SYNTAX</span></span>

### <span data-ttu-id="61a68-106">ByJobId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61a68-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a68-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="61a68-107">ByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61a68-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61a68-108">DESCRIPTION</span></span>
<span data-ttu-id="61a68-109">Il cmdlet **Stop-AzureRmAutomationDscNodeConfigurationDeployment** interrompe la distribuzione di una configurazione del nodo DSC (Desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="61a68-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="61a68-110">Interrompe l'assegnazione della configurazione dei nodi a gruppi di nodi, se ne restano da assegnare, ma non annulla l'assegnazione di nodi già assegnati.</span><span class="sxs-lookup"><span data-stu-id="61a68-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="61a68-111">Per annullare la registrazione di un processo programmato, usare l' [annullamento della registrazione-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) con JobScheduleId per annullare l'assegnazione di un processo programmato esistente.</span><span class="sxs-lookup"><span data-stu-id="61a68-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="61a68-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61a68-112">EXAMPLES</span></span>

### <span data-ttu-id="61a68-113">Esempio 1: distribuire una configurazione di nodi DSC di Azure nell'automazione</span><span class="sxs-lookup"><span data-stu-id="61a68-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="61a68-114">Il comando precedente interrompe il processo di distribuzione della configurazione del nodo DSC con il jobId passato.</span><span class="sxs-lookup"><span data-stu-id="61a68-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="61a68-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61a68-115">PARAMETERS</span></span>

### <span data-ttu-id="61a68-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="61a68-116">-AutomationAccountName</span></span>
<span data-ttu-id="61a68-117">Specifica il nome dell'account di automazione che contiene la configurazione DSC che questo cmdlet compila</span><span class="sxs-lookup"><span data-stu-id="61a68-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a68-118">-DefaultProfile</span></span>
<span data-ttu-id="61a68-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="61a68-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-120">-Force</span><span class="sxs-lookup"><span data-stu-id="61a68-120">-Force</span></span>
<span data-ttu-id="61a68-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="61a68-121">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61a68-122">-InputObject</span></span>
<span data-ttu-id="61a68-123">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="61a68-123">Input object for Piping</span></span>

```yaml
Type: NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="61a68-124">-JobId</span></span>
<span data-ttu-id="61a68-125">Specifica l'ID processo di un processo di distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="61a68-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61a68-126">-PassThru</span></span>
<span data-ttu-id="61a68-127">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="61a68-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="61a68-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="61a68-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a68-129">-ResourceGroupName</span></span>
<span data-ttu-id="61a68-130">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="61a68-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61a68-131">-Confirm</span></span>
<span data-ttu-id="61a68-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61a68-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a68-133">-WhatIf</span></span>
<span data-ttu-id="61a68-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61a68-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a68-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61a68-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a68-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a68-136">CommonParameters</span></span>
<span data-ttu-id="61a68-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a68-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a68-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a68-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a68-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61a68-139">INPUTS</span></span>

### <span data-ttu-id="61a68-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61a68-140">None</span></span>
<span data-ttu-id="61a68-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="61a68-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61a68-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61a68-142">OUTPUTS</span></span>

## <span data-ttu-id="61a68-143">Note</span><span class="sxs-lookup"><span data-stu-id="61a68-143">NOTES</span></span>

## <span data-ttu-id="61a68-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61a68-144">RELATED LINKS</span></span>

[<span data-ttu-id="61a68-145">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="61a68-145">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="61a68-146">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="61a68-146">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="61a68-147">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="61a68-147">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="61a68-148">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="61a68-148">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="61a68-149">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="61a68-149">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
