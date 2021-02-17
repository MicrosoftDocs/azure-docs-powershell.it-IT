---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210187"
---
# <span data-ttu-id="e8c39-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="e8c39-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="e8c39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8c39-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c39-103">Ottiene l'output completo di un record di output del processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="e8c39-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="e8c39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8c39-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8c39-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8c39-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c39-106">Il cmdlet **Get-AzAutomationJobOutputRecord** ottiene l'output completo di un record di output del processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="e8c39-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="e8c39-107">Anche se il cmdlet **Get-AzAutomationJobOutput** elenca uno o più record di output di processo, restituisce solo un riepilogo, in forma di stringa, del valore di qualsiasi record di output.</span><span class="sxs-lookup"><span data-stu-id="e8c39-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="e8c39-108">Non restituisce il valore completo del valore restituito dal record di output nel tipo originale.</span><span class="sxs-lookup"><span data-stu-id="e8c39-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="e8c39-109">Inoltre, il riepilogo ha una lunghezza massima, che il valore completo restituito dal cmdlet può essere superiore.</span><span class="sxs-lookup"><span data-stu-id="e8c39-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="e8c39-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8c39-110">EXAMPLES</span></span>

### <span data-ttu-id="e8c39-111">Esempio 1: Ottenere l'output completo di un processo di automazione</span><span class="sxs-lookup"><span data-stu-id="e8c39-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="e8c39-112">Questo comando ottiene l'output completo del processo con l'ID processo specificato.</span><span class="sxs-lookup"><span data-stu-id="e8c39-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="e8c39-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8c39-113">PARAMETERS</span></span>

### <span data-ttu-id="e8c39-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8c39-114">-AutomationAccountName</span></span>
<span data-ttu-id="e8c39-115">Specifica il nome di un account di automazione per cui questo cmdlet ottiene un record di output dei processi.</span><span class="sxs-lookup"><span data-stu-id="e8c39-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="e8c39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c39-116">-DefaultProfile</span></span>
<span data-ttu-id="e8c39-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e8c39-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8c39-118">-Id</span><span class="sxs-lookup"><span data-stu-id="e8c39-118">-Id</span></span>
<span data-ttu-id="e8c39-119">Specifica l'ID di un record di output del processo che il cmdlet deve recuperare.</span><span class="sxs-lookup"><span data-stu-id="e8c39-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c39-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="e8c39-120">-JobId</span></span>
<span data-ttu-id="e8c39-121">Specifica l'ID di un processo per cui questo cmdlet ottiene un record di output.</span><span class="sxs-lookup"><span data-stu-id="e8c39-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c39-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c39-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8c39-123">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene un record di output del processo.</span><span class="sxs-lookup"><span data-stu-id="e8c39-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="e8c39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c39-124">CommonParameters</span></span>
<span data-ttu-id="e8c39-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8c39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c39-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8c39-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c39-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8c39-127">INPUTS</span></span>

### <span data-ttu-id="e8c39-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e8c39-128">System.Guid</span></span>

### <span data-ttu-id="e8c39-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e8c39-129">System.String</span></span>

## <span data-ttu-id="e8c39-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8c39-130">OUTPUTS</span></span>

### <span data-ttu-id="e8c39-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="e8c39-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="e8c39-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8c39-132">NOTES</span></span>

## <span data-ttu-id="e8c39-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8c39-133">RELATED LINKS</span></span>

[<span data-ttu-id="e8c39-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e8c39-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


