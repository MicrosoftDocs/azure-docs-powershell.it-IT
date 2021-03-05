---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: f49c0bbf17ed87d782b03052d9caeb5aba51eeff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996965"
---
# <span data-ttu-id="43c3f-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="43c3f-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="43c3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="43c3f-103">Ottiene l'output di un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="43c3f-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="43c3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43c3f-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43c3f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43c3f-105">DESCRIPTION</span></span>
<span data-ttu-id="43c3f-106">Il **cmdlet Get-AzAutomationJobOutput** ottiene l'output di un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="43c3f-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="43c3f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43c3f-107">EXAMPLES</span></span>

### <span data-ttu-id="43c3f-108">Esempio 1: Ottenere l'output di un processo di automazione</span><span class="sxs-lookup"><span data-stu-id="43c3f-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="43c3f-109">Questo comando ottiene tutto l'output del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="43c3f-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="43c3f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43c3f-110">PARAMETERS</span></span>

### <span data-ttu-id="43c3f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43c3f-111">-AutomationAccountName</span></span>
<span data-ttu-id="43c3f-112">Specifica il nome di un account di automazione per cui questo cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="43c3f-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="43c3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c3f-113">-DefaultProfile</span></span>
<span data-ttu-id="43c3f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="43c3f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43c3f-115">-Id</span><span class="sxs-lookup"><span data-stu-id="43c3f-115">-Id</span></span>
<span data-ttu-id="43c3f-116">Specifica l'ID di un processo per cui il cmdlet riceve l'output.</span><span class="sxs-lookup"><span data-stu-id="43c3f-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="43c3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="43c3f-118">Specifica il nome di un gruppo di risorse per cui il cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="43c3f-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="43c3f-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="43c3f-119">-StartTime</span></span>
<span data-ttu-id="43c3f-120">Specifica un'ora di inizio come **oggetto DateTime Offset.**</span><span class="sxs-lookup"><span data-stu-id="43c3f-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="43c3f-121">È possibile specificare una stringa che può essere convertita in **un valore DateTime Offset valido.**</span><span class="sxs-lookup"><span data-stu-id="43c3f-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="43c3f-122">Il cmdlet recupera l'output creato dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="43c3f-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="43c3f-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="43c3f-123">-Stream</span></span>
<span data-ttu-id="43c3f-124">Specifica il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="43c3f-124">Specifies the type of output.</span></span>
<span data-ttu-id="43c3f-125">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="43c3f-125">Valid values are:</span></span> 
- <span data-ttu-id="43c3f-126">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="43c3f-126">Any</span></span>
- <span data-ttu-id="43c3f-127">Debug</span><span class="sxs-lookup"><span data-stu-id="43c3f-127">Debug</span></span>
- <span data-ttu-id="43c3f-128">Errore</span><span class="sxs-lookup"><span data-stu-id="43c3f-128">Error</span></span>
- <span data-ttu-id="43c3f-129">Output</span><span class="sxs-lookup"><span data-stu-id="43c3f-129">Output</span></span>
- <span data-ttu-id="43c3f-130">Stato di avanzamento</span><span class="sxs-lookup"><span data-stu-id="43c3f-130">Progress</span></span>
- <span data-ttu-id="43c3f-131">Verbose</span><span class="sxs-lookup"><span data-stu-id="43c3f-131">Verbose</span></span>
- <span data-ttu-id="43c3f-132">Avviso</span><span class="sxs-lookup"><span data-stu-id="43c3f-132">Warning</span></span>

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

### <span data-ttu-id="43c3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c3f-133">CommonParameters</span></span>
<span data-ttu-id="43c3f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c3f-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c3f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c3f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="43c3f-136">INPUTS</span></span>

### <span data-ttu-id="43c3f-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="43c3f-137">System.Guid</span></span>

### <span data-ttu-id="43c3f-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="43c3f-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="43c3f-139">System.Nullable'1[[System.DateTimeToken, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="43c3f-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="43c3f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="43c3f-140">System.String</span></span>

## <span data-ttu-id="43c3f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43c3f-141">OUTPUTS</span></span>

### <span data-ttu-id="43c3f-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="43c3f-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="43c3f-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="43c3f-143">NOTES</span></span>

## <span data-ttu-id="43c3f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43c3f-144">RELATED LINKS</span></span>

[<span data-ttu-id="43c3f-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43c3f-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="43c3f-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43c3f-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="43c3f-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43c3f-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="43c3f-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43c3f-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


