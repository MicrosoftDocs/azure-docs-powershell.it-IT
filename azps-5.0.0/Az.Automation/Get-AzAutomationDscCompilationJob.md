---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199594"
---
# <span data-ttu-id="82006-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="82006-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="82006-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82006-102">SYNOPSIS</span></span>
<span data-ttu-id="82006-103">Ottiene i processi di compilazione DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="82006-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="82006-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82006-104">SYNTAX</span></span>

### <span data-ttu-id="82006-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82006-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82006-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="82006-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82006-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="82006-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82006-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82006-108">DESCRIPTION</span></span>
<span data-ttu-id="82006-109">Il cmdlet **Get-AzAutomationDscCompilationJob** ottiene i processi di compilazione del DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="82006-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="82006-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82006-110">EXAMPLES</span></span>

### <span data-ttu-id="82006-111">Esempio 1: ottenere tutti i processi di compilazione DSC</span><span class="sxs-lookup"><span data-stu-id="82006-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="82006-112">Questo comando consente di ottenere tutti i processi di compilazione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82006-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="82006-113">Esempio 2: ottenere processi di compilazione DSC per una configurazione</span><span class="sxs-lookup"><span data-stu-id="82006-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="82006-114">Questo comando consente di ottenere tutti i processi di compilazione per la configurazione DSC denominata ContosoConfiguration nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82006-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="82006-115">Esempio 3: ottenere un processo di compilazione DSC specifico</span><span class="sxs-lookup"><span data-stu-id="82006-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="82006-116">Questo comando ottiene il processo di compilazione con l'ID specificato nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82006-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="82006-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82006-117">PARAMETERS</span></span>

### <span data-ttu-id="82006-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82006-118">-AutomationAccountName</span></span>
<span data-ttu-id="82006-119">Specifica il nome dell'account di automazione che contiene i processi di compilazione DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82006-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="82006-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="82006-120">-ConfigurationName</span></span>
<span data-ttu-id="82006-121">Specifica il nome della configurazione DSC per cui questo cmdlet ottiene i processi di compilazione.</span><span class="sxs-lookup"><span data-stu-id="82006-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82006-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82006-122">-DefaultProfile</span></span>
<span data-ttu-id="82006-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="82006-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82006-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="82006-124">-EndTime</span></span>
<span data-ttu-id="82006-125">Specifica un'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="82006-125">Specifies an end time.</span></span>
<span data-ttu-id="82006-126">Questo cmdlet ottiene i processi di compilazione che sono stati avviati fino al momento in cui questo parametro specifica.</span><span class="sxs-lookup"><span data-stu-id="82006-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82006-127">-ID</span><span class="sxs-lookup"><span data-stu-id="82006-127">-Id</span></span>
<span data-ttu-id="82006-128">Specifica l'ID univoco del processo di compilazione DSC ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82006-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82006-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82006-129">-ResourceGroupName</span></span>
<span data-ttu-id="82006-130">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene i processi di compilazione DSC.</span><span class="sxs-lookup"><span data-stu-id="82006-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="82006-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="82006-131">-StartTime</span></span>
<span data-ttu-id="82006-132">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="82006-132">Specifies a start time.</span></span>
<span data-ttu-id="82006-133">Questo cmdlet ottiene i processi che iniziano da o dopo l'ora specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="82006-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82006-134">-Stato</span><span class="sxs-lookup"><span data-stu-id="82006-134">-Status</span></span>
<span data-ttu-id="82006-135">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82006-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="82006-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="82006-136">Valid values are:</span></span> 
- <span data-ttu-id="82006-137">Completato</span><span class="sxs-lookup"><span data-stu-id="82006-137">Completed</span></span> 
- <span data-ttu-id="82006-138">Fallito</span><span class="sxs-lookup"><span data-stu-id="82006-138">Failed</span></span> 
- <span data-ttu-id="82006-139">Accodati</span><span class="sxs-lookup"><span data-stu-id="82006-139">Queued</span></span> 
- <span data-ttu-id="82006-140">Iniziale</span><span class="sxs-lookup"><span data-stu-id="82006-140">Starting</span></span> 
- <span data-ttu-id="82006-141">Ripresa</span><span class="sxs-lookup"><span data-stu-id="82006-141">Resuming</span></span> 
- <span data-ttu-id="82006-142">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="82006-142">Running</span></span> 
- <span data-ttu-id="82006-143">Ha smesso</span><span class="sxs-lookup"><span data-stu-id="82006-143">Stopped</span></span> 
- <span data-ttu-id="82006-144">Arresto</span><span class="sxs-lookup"><span data-stu-id="82006-144">Stopping</span></span> 
- <span data-ttu-id="82006-145">Sospeso</span><span class="sxs-lookup"><span data-stu-id="82006-145">Suspended</span></span> 
- <span data-ttu-id="82006-146">Sospensione</span><span class="sxs-lookup"><span data-stu-id="82006-146">Suspending</span></span> 
- <span data-ttu-id="82006-147">L'attivazione</span><span class="sxs-lookup"><span data-stu-id="82006-147">Activating</span></span>
- <span data-ttu-id="82006-148">Nuovo</span><span class="sxs-lookup"><span data-stu-id="82006-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82006-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82006-149">CommonParameters</span></span>
<span data-ttu-id="82006-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82006-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82006-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82006-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82006-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82006-152">INPUTS</span></span>

### <span data-ttu-id="82006-153">System. Guid</span><span class="sxs-lookup"><span data-stu-id="82006-153">System.Guid</span></span>

### <span data-ttu-id="82006-154">System. String</span><span class="sxs-lookup"><span data-stu-id="82006-154">System.String</span></span>

## <span data-ttu-id="82006-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82006-155">OUTPUTS</span></span>

### <span data-ttu-id="82006-156">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="82006-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="82006-157">Note</span><span class="sxs-lookup"><span data-stu-id="82006-157">NOTES</span></span>

## <span data-ttu-id="82006-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82006-158">RELATED LINKS</span></span>

[<span data-ttu-id="82006-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="82006-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="82006-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="82006-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

