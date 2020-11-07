---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: d46dd2e314aa8064b305adb0501ae20480a34418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685639"
---
# <span data-ttu-id="8aaef-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="8aaef-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="8aaef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8aaef-102">SYNOPSIS</span></span>
<span data-ttu-id="8aaef-103">Ottiene l'output di un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="8aaef-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8aaef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8aaef-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8aaef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8aaef-105">DESCRIPTION</span></span>
<span data-ttu-id="8aaef-106">Il cmdlet **Get-AzureRmAutomationJobOutput** Ottiene l'output di un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8aaef-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="8aaef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8aaef-107">EXAMPLES</span></span>

### <span data-ttu-id="8aaef-108">Esempio 1: ottenere l'output di un processo di automazione</span><span class="sxs-lookup"><span data-stu-id="8aaef-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="8aaef-109">Questo comando consente di ottenere tutto l'output del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="8aaef-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="8aaef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8aaef-110">PARAMETERS</span></span>

### <span data-ttu-id="8aaef-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8aaef-111">-AutomationAccountName</span></span>
<span data-ttu-id="8aaef-112">Specifica il nome di un account di automazione per cui questo cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="8aaef-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="8aaef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aaef-113">-DefaultProfile</span></span>
<span data-ttu-id="8aaef-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8aaef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aaef-115">-ID</span><span class="sxs-lookup"><span data-stu-id="8aaef-115">-Id</span></span>
<span data-ttu-id="8aaef-116">Specifica l'ID di un processo per cui questo cmdlet ottiene l'output.</span><span class="sxs-lookup"><span data-stu-id="8aaef-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aaef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aaef-117">-ResourceGroupName</span></span>
<span data-ttu-id="8aaef-118">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="8aaef-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="8aaef-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8aaef-119">-StartTime</span></span>
<span data-ttu-id="8aaef-120">Specifica un'ora di inizio come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="8aaef-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="8aaef-121">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="8aaef-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="8aaef-122">Il cmdlet recupera l'output creato dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="8aaef-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aaef-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="8aaef-123">-Stream</span></span>
<span data-ttu-id="8aaef-124">Specifica il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="8aaef-124">Specifies the type of output.</span></span>
<span data-ttu-id="8aaef-125">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="8aaef-125">Valid values are:</span></span> 

- <span data-ttu-id="8aaef-126">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="8aaef-126">Any</span></span>
- <span data-ttu-id="8aaef-127">Debug</span><span class="sxs-lookup"><span data-stu-id="8aaef-127">Debug</span></span>
- <span data-ttu-id="8aaef-128">Errore</span><span class="sxs-lookup"><span data-stu-id="8aaef-128">Error</span></span>
- <span data-ttu-id="8aaef-129">Output</span><span class="sxs-lookup"><span data-stu-id="8aaef-129">Output</span></span>
- <span data-ttu-id="8aaef-130">Progresso</span><span class="sxs-lookup"><span data-stu-id="8aaef-130">Progress</span></span>
- <span data-ttu-id="8aaef-131">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="8aaef-131">Verbose</span></span>
- <span data-ttu-id="8aaef-132">Avviso</span><span class="sxs-lookup"><span data-stu-id="8aaef-132">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aaef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aaef-133">CommonParameters</span></span>
<span data-ttu-id="8aaef-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aaef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aaef-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aaef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aaef-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8aaef-136">INPUTS</span></span>

### <span data-ttu-id="8aaef-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8aaef-137">None</span></span>
<span data-ttu-id="8aaef-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8aaef-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8aaef-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8aaef-139">OUTPUTS</span></span>

### <span data-ttu-id="8aaef-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="8aaef-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="8aaef-141">Note</span><span class="sxs-lookup"><span data-stu-id="8aaef-141">NOTES</span></span>

## <span data-ttu-id="8aaef-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8aaef-142">RELATED LINKS</span></span>

[<span data-ttu-id="8aaef-143">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8aaef-143">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="8aaef-144">Curriculum vitae-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8aaef-144">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="8aaef-145">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8aaef-145">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="8aaef-146">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8aaef-146">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


