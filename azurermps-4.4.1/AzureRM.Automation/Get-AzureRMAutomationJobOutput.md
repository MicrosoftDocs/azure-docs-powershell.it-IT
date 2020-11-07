---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: dd80c745c99c98d6ea5b551ab454661d4370cebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688531"
---
# <span data-ttu-id="4e12f-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="4e12f-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="4e12f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e12f-102">SYNOPSIS</span></span>
<span data-ttu-id="4e12f-103">Ottiene l'output di un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="4e12f-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e12f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e12f-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e12f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e12f-105">DESCRIPTION</span></span>
<span data-ttu-id="4e12f-106">Il cmdlet **Get-AzureRmAutomationJobOutput** Ottiene l'output di un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e12f-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="4e12f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e12f-107">EXAMPLES</span></span>

### <span data-ttu-id="4e12f-108">Esempio 1: ottenere l'output di un processo di automazione</span><span class="sxs-lookup"><span data-stu-id="4e12f-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="4e12f-109">Questo comando consente di ottenere tutto l'output del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="4e12f-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="4e12f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e12f-110">PARAMETERS</span></span>

### <span data-ttu-id="4e12f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e12f-111">-AutomationAccountName</span></span>
<span data-ttu-id="4e12f-112">Specifica il nome di un account di automazione per cui questo cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="4e12f-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="4e12f-113">-ID</span><span class="sxs-lookup"><span data-stu-id="4e12f-113">-Id</span></span>
<span data-ttu-id="4e12f-114">Specifica l'ID di un processo per cui questo cmdlet ottiene l'output.</span><span class="sxs-lookup"><span data-stu-id="4e12f-114">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e12f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e12f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e12f-116">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="4e12f-116">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="4e12f-117">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4e12f-117">-StartTime</span></span>
<span data-ttu-id="4e12f-118">Specifica un'ora di inizio come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="4e12f-118">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="4e12f-119">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="4e12f-119">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="4e12f-120">Il cmdlet recupera l'output creato dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="4e12f-120">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e12f-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="4e12f-121">-Stream</span></span>
<span data-ttu-id="4e12f-122">Specifica il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="4e12f-122">Specifies the type of output.</span></span>
<span data-ttu-id="4e12f-123">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="4e12f-123">Valid values are:</span></span> 

- <span data-ttu-id="4e12f-124">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="4e12f-124">Any</span></span>
- <span data-ttu-id="4e12f-125">Debug</span><span class="sxs-lookup"><span data-stu-id="4e12f-125">Debug</span></span>
- <span data-ttu-id="4e12f-126">Errore</span><span class="sxs-lookup"><span data-stu-id="4e12f-126">Error</span></span>
- <span data-ttu-id="4e12f-127">Output</span><span class="sxs-lookup"><span data-stu-id="4e12f-127">Output</span></span>
- <span data-ttu-id="4e12f-128">Progresso</span><span class="sxs-lookup"><span data-stu-id="4e12f-128">Progress</span></span>
- <span data-ttu-id="4e12f-129">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="4e12f-129">Verbose</span></span>
- <span data-ttu-id="4e12f-130">Avviso</span><span class="sxs-lookup"><span data-stu-id="4e12f-130">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e12f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e12f-131">-DefaultProfile</span></span>
<span data-ttu-id="4e12f-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e12f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e12f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e12f-133">CommonParameters</span></span>
<span data-ttu-id="4e12f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e12f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e12f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e12f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e12f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e12f-136">INPUTS</span></span>

## <span data-ttu-id="4e12f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e12f-137">OUTPUTS</span></span>

### <span data-ttu-id="4e12f-138">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="4e12f-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="4e12f-139">Note</span><span class="sxs-lookup"><span data-stu-id="4e12f-139">NOTES</span></span>

## <span data-ttu-id="4e12f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e12f-140">RELATED LINKS</span></span>

[<span data-ttu-id="4e12f-141">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4e12f-141">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="4e12f-142">Curriculum vitae-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4e12f-142">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="4e12f-143">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4e12f-143">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="4e12f-144">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4e12f-144">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


