---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519640"
---
# <span data-ttu-id="5d774-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5d774-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="5d774-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d774-102">SYNOPSIS</span></span>
<span data-ttu-id="5d774-103">Ottiene i processi di compilazione DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="5d774-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d774-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d774-104">SYNTAX</span></span>

### <span data-ttu-id="5d774-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d774-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d774-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="5d774-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d774-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5d774-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d774-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d774-108">DESCRIPTION</span></span>
<span data-ttu-id="5d774-109">Il cmdlet **Get-AzureRmAutomationDscCompilationJob** ottiene i processi di compilazione del DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5d774-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="5d774-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d774-110">EXAMPLES</span></span>

### <span data-ttu-id="5d774-111">Esempio 1: ottenere tutti i processi di compilazione DSC</span><span class="sxs-lookup"><span data-stu-id="5d774-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5d774-112">Questo comando consente di ottenere tutti i processi di compilazione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5d774-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5d774-113">Esempio 2: ottenere processi di compilazione DSC per una configurazione</span><span class="sxs-lookup"><span data-stu-id="5d774-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="5d774-114">Questo comando consente di ottenere tutti i processi di compilazione per la configurazione DSC denominata ContosoConfiguration nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5d774-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5d774-115">Esempio 3: ottenere un processo di compilazione DSC specifico</span><span class="sxs-lookup"><span data-stu-id="5d774-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="5d774-116">Questo comando ottiene il processo di compilazione con l'ID specificato nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5d774-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5d774-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d774-117">PARAMETERS</span></span>

### <span data-ttu-id="5d774-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5d774-118">-AutomationAccountName</span></span>
<span data-ttu-id="5d774-119">Specifica il nome dell'account di automazione che contiene i processi di compilazione DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d774-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5d774-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5d774-120">-ConfigurationName</span></span>
<span data-ttu-id="5d774-121">Specifica il nome della configurazione DSC per cui questo cmdlet ottiene i processi di compilazione.</span><span class="sxs-lookup"><span data-stu-id="5d774-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="5d774-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5d774-122">-EndTime</span></span>
<span data-ttu-id="5d774-123">Specifica un'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="5d774-123">Specifies an end time.</span></span>
<span data-ttu-id="5d774-124">Questo cmdlet ottiene i processi di compilazione che sono stati avviati fino al momento in cui questo parametro specifica.</span><span class="sxs-lookup"><span data-stu-id="5d774-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="5d774-125">-ID</span><span class="sxs-lookup"><span data-stu-id="5d774-125">-Id</span></span>
<span data-ttu-id="5d774-126">Specifica l'ID univoco del processo di compilazione DSC ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d774-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5d774-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d774-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d774-128">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene i processi di compilazione DSC.</span><span class="sxs-lookup"><span data-stu-id="5d774-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="5d774-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5d774-129">-StartTime</span></span>
<span data-ttu-id="5d774-130">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="5d774-130">Specifies a start time.</span></span>
<span data-ttu-id="5d774-131">Questo cmdlet ottiene i processi che iniziano da o dopo l'ora specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5d774-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="5d774-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="5d774-132">-Status</span></span>
<span data-ttu-id="5d774-133">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d774-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5d774-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="5d774-134">Valid values are:</span></span> 

- <span data-ttu-id="5d774-135">Completato</span><span class="sxs-lookup"><span data-stu-id="5d774-135">Completed</span></span> 
- <span data-ttu-id="5d774-136">Fallito</span><span class="sxs-lookup"><span data-stu-id="5d774-136">Failed</span></span> 
- <span data-ttu-id="5d774-137">Accodati</span><span class="sxs-lookup"><span data-stu-id="5d774-137">Queued</span></span> 
- <span data-ttu-id="5d774-138">Iniziale</span><span class="sxs-lookup"><span data-stu-id="5d774-138">Starting</span></span> 
- <span data-ttu-id="5d774-139">Ripresa</span><span class="sxs-lookup"><span data-stu-id="5d774-139">Resuming</span></span> 
- <span data-ttu-id="5d774-140">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="5d774-140">Running</span></span> 
- <span data-ttu-id="5d774-141">Ha smesso</span><span class="sxs-lookup"><span data-stu-id="5d774-141">Stopped</span></span> 
- <span data-ttu-id="5d774-142">Arresto</span><span class="sxs-lookup"><span data-stu-id="5d774-142">Stopping</span></span> 
- <span data-ttu-id="5d774-143">Sospeso</span><span class="sxs-lookup"><span data-stu-id="5d774-143">Suspended</span></span> 
- <span data-ttu-id="5d774-144">Sospensione</span><span class="sxs-lookup"><span data-stu-id="5d774-144">Suspending</span></span> 
- <span data-ttu-id="5d774-145">L'attivazione</span><span class="sxs-lookup"><span data-stu-id="5d774-145">Activating</span></span>
- <span data-ttu-id="5d774-146">Nuovo</span><span class="sxs-lookup"><span data-stu-id="5d774-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d774-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d774-147">-DefaultProfile</span></span>
<span data-ttu-id="5d774-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d774-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d774-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d774-149">CommonParameters</span></span>
<span data-ttu-id="5d774-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d774-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d774-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d774-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d774-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d774-152">INPUTS</span></span>

## <span data-ttu-id="5d774-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d774-153">OUTPUTS</span></span>

### <span data-ttu-id="5d774-154">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="5d774-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="5d774-155">Note</span><span class="sxs-lookup"><span data-stu-id="5d774-155">NOTES</span></span>

## <span data-ttu-id="5d774-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d774-156">RELATED LINKS</span></span>

[<span data-ttu-id="5d774-157">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="5d774-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="5d774-158">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5d774-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


