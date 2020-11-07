---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 60de6b852d516cd4742ed253d149ea031449548b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685078"
---
# <span data-ttu-id="c4d6b-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c4d6b-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="c4d6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d6b-103">Ottiene l'output di un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="c4d6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4d6b-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4d6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d6b-106">Il cmdlet **Get-AzAutomationJobOutput** Ottiene l'output di un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="c4d6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4d6b-107">EXAMPLES</span></span>

### <span data-ttu-id="c4d6b-108">Esempio 1: ottenere l'output di un processo di automazione</span><span class="sxs-lookup"><span data-stu-id="c4d6b-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="c4d6b-109">Questo comando consente di ottenere tutto l'output del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="c4d6b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4d6b-110">PARAMETERS</span></span>

### <span data-ttu-id="c4d6b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4d6b-111">-AutomationAccountName</span></span>
<span data-ttu-id="c4d6b-112">Specifica il nome di un account di automazione per cui questo cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="c4d6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d6b-113">-DefaultProfile</span></span>
<span data-ttu-id="c4d6b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c4d6b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4d6b-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c4d6b-115">-Id</span></span>
<span data-ttu-id="c4d6b-116">Specifica l'ID di un processo per cui questo cmdlet ottiene l'output.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="c4d6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4d6b-118">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="c4d6b-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c4d6b-119">-StartTime</span></span>
<span data-ttu-id="c4d6b-120">Specifica un'ora di inizio come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="c4d6b-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c4d6b-121">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c4d6b-122">Il cmdlet recupera l'output creato dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="c4d6b-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="c4d6b-123">-Stream</span></span>
<span data-ttu-id="c4d6b-124">Specifica il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-124">Specifies the type of output.</span></span>
<span data-ttu-id="c4d6b-125">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c4d6b-125">Valid values are:</span></span> 
- <span data-ttu-id="c4d6b-126">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="c4d6b-126">Any</span></span>
- <span data-ttu-id="c4d6b-127">Debug</span><span class="sxs-lookup"><span data-stu-id="c4d6b-127">Debug</span></span>
- <span data-ttu-id="c4d6b-128">Errore</span><span class="sxs-lookup"><span data-stu-id="c4d6b-128">Error</span></span>
- <span data-ttu-id="c4d6b-129">Output</span><span class="sxs-lookup"><span data-stu-id="c4d6b-129">Output</span></span>
- <span data-ttu-id="c4d6b-130">Progresso</span><span class="sxs-lookup"><span data-stu-id="c4d6b-130">Progress</span></span>
- <span data-ttu-id="c4d6b-131">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="c4d6b-131">Verbose</span></span>
- <span data-ttu-id="c4d6b-132">Avviso</span><span class="sxs-lookup"><span data-stu-id="c4d6b-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d6b-133">CommonParameters</span></span>
<span data-ttu-id="c4d6b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d6b-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d6b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d6b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4d6b-136">INPUTS</span></span>

### <span data-ttu-id="c4d6b-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c4d6b-137">System.Guid</span></span>

### <span data-ttu-id="c4d6b-138">Microsoft. Azure. Commands. Automation. Common. StreamType</span><span class="sxs-lookup"><span data-stu-id="c4d6b-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="c4d6b-139">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c4d6b-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c4d6b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d6b-140">System.String</span></span>

## <span data-ttu-id="c4d6b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4d6b-141">OUTPUTS</span></span>

### <span data-ttu-id="c4d6b-142">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="c4d6b-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="c4d6b-143">Note</span><span class="sxs-lookup"><span data-stu-id="c4d6b-143">NOTES</span></span>

## <span data-ttu-id="c4d6b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4d6b-144">RELATED LINKS</span></span>

[<span data-ttu-id="c4d6b-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c4d6b-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="c4d6b-146">Curriculum vitae-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c4d6b-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="c4d6b-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c4d6b-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="c4d6b-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c4d6b-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


