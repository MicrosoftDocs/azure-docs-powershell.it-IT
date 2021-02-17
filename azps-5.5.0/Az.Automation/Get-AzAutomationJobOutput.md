---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210211"
---
# <span data-ttu-id="f5bb4-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="f5bb4-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="f5bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="f5bb4-103">Ottiene l'output di un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="f5bb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5bb4-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5bb4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f5bb4-105">DESCRIPTION</span></span>
<span data-ttu-id="f5bb4-106">Il **cmdlet Get-AzAutomationJobOutput** ottiene l'output di un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="f5bb4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5bb4-107">EXAMPLES</span></span>

### <span data-ttu-id="f5bb4-108">Esempio 1: Ottenere l'output di un processo di automazione</span><span class="sxs-lookup"><span data-stu-id="f5bb4-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="f5bb4-109">Questo comando ottiene tutto l'output del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="f5bb4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5bb4-110">PARAMETERS</span></span>

### <span data-ttu-id="f5bb4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f5bb4-111">-AutomationAccountName</span></span>
<span data-ttu-id="f5bb4-112">Specifica il nome di un account di automazione per cui questo cmdlet ottiene l'output di processo.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="f5bb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5bb4-113">-DefaultProfile</span></span>
<span data-ttu-id="f5bb4-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f5bb4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5bb4-115">-Id</span><span class="sxs-lookup"><span data-stu-id="f5bb4-115">-Id</span></span>
<span data-ttu-id="f5bb4-116">Specifica l'ID di un processo per cui il cmdlet riceve l'output.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="f5bb4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5bb4-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5bb4-118">Specifica il nome di un gruppo di risorse per cui il cmdlet ottiene l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="f5bb4-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f5bb4-119">-StartTime</span></span>
<span data-ttu-id="f5bb4-120">Specifica un'ora di inizio come **oggetto DateTime Offset.**</span><span class="sxs-lookup"><span data-stu-id="f5bb4-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="f5bb4-121">È possibile specificare una stringa che può essere convertita in **un valore DateTime Offset valido.**</span><span class="sxs-lookup"><span data-stu-id="f5bb4-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="f5bb4-122">Il cmdlet recupera l'output creato dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="f5bb4-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="f5bb4-123">-Stream</span></span>
<span data-ttu-id="f5bb4-124">Specifica il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-124">Specifies the type of output.</span></span>
<span data-ttu-id="f5bb4-125">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f5bb4-125">Valid values are:</span></span> 
- <span data-ttu-id="f5bb4-126">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="f5bb4-126">Any</span></span>
- <span data-ttu-id="f5bb4-127">Debug</span><span class="sxs-lookup"><span data-stu-id="f5bb4-127">Debug</span></span>
- <span data-ttu-id="f5bb4-128">Errore</span><span class="sxs-lookup"><span data-stu-id="f5bb4-128">Error</span></span>
- <span data-ttu-id="f5bb4-129">Output</span><span class="sxs-lookup"><span data-stu-id="f5bb4-129">Output</span></span>
- <span data-ttu-id="f5bb4-130">Stato di avanzamento</span><span class="sxs-lookup"><span data-stu-id="f5bb4-130">Progress</span></span>
- <span data-ttu-id="f5bb4-131">Verbose</span><span class="sxs-lookup"><span data-stu-id="f5bb4-131">Verbose</span></span>
- <span data-ttu-id="f5bb4-132">Avviso</span><span class="sxs-lookup"><span data-stu-id="f5bb4-132">Warning</span></span>

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

### <span data-ttu-id="f5bb4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5bb4-133">CommonParameters</span></span>
<span data-ttu-id="f5bb4-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5bb4-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5bb4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5bb4-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="f5bb4-136">INPUTS</span></span>

### <span data-ttu-id="f5bb4-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f5bb4-137">System.Guid</span></span>

### <span data-ttu-id="f5bb4-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="f5bb4-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="f5bb4-139">System.Nullable'1[[System.DateTimeToken, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f5bb4-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f5bb4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f5bb4-140">System.String</span></span>

## <span data-ttu-id="f5bb4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5bb4-141">OUTPUTS</span></span>

### <span data-ttu-id="f5bb4-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="f5bb4-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="f5bb4-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="f5bb4-143">NOTES</span></span>

## <span data-ttu-id="f5bb4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5bb4-144">RELATED LINKS</span></span>

[<span data-ttu-id="f5bb4-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f5bb4-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="f5bb4-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f5bb4-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="f5bb4-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f5bb4-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="f5bb4-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f5bb4-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


