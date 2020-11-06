---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: c7e4043cb6883020b8af15d13dd46c395997e116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522082"
---
# <span data-ttu-id="0c823-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="0c823-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="0c823-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c823-102">SYNOPSIS</span></span>
<span data-ttu-id="0c823-103">Ottiene i processi di compilazione DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="0c823-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c823-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c823-104">SYNTAX</span></span>

### <span data-ttu-id="0c823-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c823-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c823-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="0c823-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c823-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0c823-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c823-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c823-108">DESCRIPTION</span></span>
<span data-ttu-id="0c823-109">Il cmdlet **Get-AzureRmAutomationDscCompilationJob** ottiene i processi di compilazione del DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0c823-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="0c823-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c823-110">EXAMPLES</span></span>

### <span data-ttu-id="0c823-111">Esempio 1: ottenere tutti i processi di compilazione DSC</span><span class="sxs-lookup"><span data-stu-id="0c823-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0c823-112">Questo comando consente di ottenere tutti i processi di compilazione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0c823-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0c823-113">Esempio 2: ottenere processi di compilazione DSC per una configurazione</span><span class="sxs-lookup"><span data-stu-id="0c823-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="0c823-114">Questo comando consente di ottenere tutti i processi di compilazione per la configurazione DSC denominata ContosoConfiguration nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0c823-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0c823-115">Esempio 3: ottenere un processo di compilazione DSC specifico</span><span class="sxs-lookup"><span data-stu-id="0c823-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="0c823-116">Questo comando ottiene il processo di compilazione con l'ID specificato nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0c823-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0c823-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c823-117">PARAMETERS</span></span>

### <span data-ttu-id="0c823-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0c823-118">-AutomationAccountName</span></span>
<span data-ttu-id="0c823-119">Specifica il nome dell'account di automazione che contiene i processi di compilazione DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c823-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c823-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0c823-120">-ConfigurationName</span></span>
<span data-ttu-id="0c823-121">Specifica il nome della configurazione DSC per cui questo cmdlet ottiene i processi di compilazione.</span><span class="sxs-lookup"><span data-stu-id="0c823-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c823-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c823-122">-DefaultProfile</span></span>
<span data-ttu-id="0c823-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c823-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c823-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0c823-124">-EndTime</span></span>
<span data-ttu-id="0c823-125">Specifica un'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="0c823-125">Specifies an end time.</span></span>
<span data-ttu-id="0c823-126">Questo cmdlet ottiene i processi di compilazione che sono stati avviati fino al momento in cui questo parametro specifica.</span><span class="sxs-lookup"><span data-stu-id="0c823-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c823-127">-ID</span><span class="sxs-lookup"><span data-stu-id="0c823-127">-Id</span></span>
<span data-ttu-id="0c823-128">Specifica l'ID univoco del processo di compilazione DSC ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c823-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c823-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c823-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c823-130">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene i processi di compilazione DSC.</span><span class="sxs-lookup"><span data-stu-id="0c823-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="0c823-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0c823-131">-StartTime</span></span>
<span data-ttu-id="0c823-132">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="0c823-132">Specifies a start time.</span></span>
<span data-ttu-id="0c823-133">Questo cmdlet ottiene i processi che iniziano da o dopo l'ora specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0c823-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c823-134">-Stato</span><span class="sxs-lookup"><span data-stu-id="0c823-134">-Status</span></span>
<span data-ttu-id="0c823-135">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c823-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0c823-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="0c823-136">Valid values are:</span></span> 

- <span data-ttu-id="0c823-137">Completato</span><span class="sxs-lookup"><span data-stu-id="0c823-137">Completed</span></span> 
- <span data-ttu-id="0c823-138">Fallito</span><span class="sxs-lookup"><span data-stu-id="0c823-138">Failed</span></span> 
- <span data-ttu-id="0c823-139">Accodati</span><span class="sxs-lookup"><span data-stu-id="0c823-139">Queued</span></span> 
- <span data-ttu-id="0c823-140">Iniziale</span><span class="sxs-lookup"><span data-stu-id="0c823-140">Starting</span></span> 
- <span data-ttu-id="0c823-141">Ripresa</span><span class="sxs-lookup"><span data-stu-id="0c823-141">Resuming</span></span> 
- <span data-ttu-id="0c823-142">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="0c823-142">Running</span></span> 
- <span data-ttu-id="0c823-143">Ha smesso</span><span class="sxs-lookup"><span data-stu-id="0c823-143">Stopped</span></span> 
- <span data-ttu-id="0c823-144">Arresto</span><span class="sxs-lookup"><span data-stu-id="0c823-144">Stopping</span></span> 
- <span data-ttu-id="0c823-145">Sospeso</span><span class="sxs-lookup"><span data-stu-id="0c823-145">Suspended</span></span> 
- <span data-ttu-id="0c823-146">Sospensione</span><span class="sxs-lookup"><span data-stu-id="0c823-146">Suspending</span></span> 
- <span data-ttu-id="0c823-147">L'attivazione</span><span class="sxs-lookup"><span data-stu-id="0c823-147">Activating</span></span>
- <span data-ttu-id="0c823-148">Nuovo</span><span class="sxs-lookup"><span data-stu-id="0c823-148">New</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c823-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c823-149">CommonParameters</span></span>
<span data-ttu-id="0c823-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c823-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c823-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c823-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c823-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c823-152">INPUTS</span></span>

### <span data-ttu-id="0c823-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0c823-153">None</span></span>
<span data-ttu-id="0c823-154">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0c823-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c823-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c823-155">OUTPUTS</span></span>

### <span data-ttu-id="0c823-156">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="0c823-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="0c823-157">Note</span><span class="sxs-lookup"><span data-stu-id="0c823-157">NOTES</span></span>

## <span data-ttu-id="0c823-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c823-158">RELATED LINKS</span></span>

[<span data-ttu-id="0c823-159">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="0c823-159">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="0c823-160">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="0c823-160">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


