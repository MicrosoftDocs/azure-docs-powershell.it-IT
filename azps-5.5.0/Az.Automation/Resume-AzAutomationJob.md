---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177967"
---
# <span data-ttu-id="db2be-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="db2be-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="db2be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db2be-102">SYNOPSIS</span></span>
<span data-ttu-id="db2be-103">Riprende un processo di automazione sospeso.</span><span class="sxs-lookup"><span data-stu-id="db2be-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="db2be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db2be-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db2be-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db2be-105">DESCRIPTION</span></span>
<span data-ttu-id="db2be-106">Il cmdlet **Resume-AzAutomationJob** riprende un processo sospeso di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="db2be-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="db2be-107">Specificare il processo sospeso.</span><span class="sxs-lookup"><span data-stu-id="db2be-107">Specify the suspended job.</span></span>
<span data-ttu-id="db2be-108">Per sospendere un processo, usare il cmdlet Suspend-AzAutomationJob lavoro.</span><span class="sxs-lookup"><span data-stu-id="db2be-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="db2be-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db2be-109">EXAMPLES</span></span>

### <span data-ttu-id="db2be-110">Esempio 1: Riprendere un processo sospeso</span><span class="sxs-lookup"><span data-stu-id="db2be-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="db2be-111">Questo comando riprende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="db2be-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="db2be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db2be-112">PARAMETERS</span></span>

### <span data-ttu-id="db2be-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="db2be-113">-AutomationAccountName</span></span>
<span data-ttu-id="db2be-114">Specifica il nome di un account di automazione in cui questo cmdlet riprende un processo.</span><span class="sxs-lookup"><span data-stu-id="db2be-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="db2be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2be-115">-DefaultProfile</span></span>
<span data-ttu-id="db2be-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="db2be-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db2be-117">-Id</span><span class="sxs-lookup"><span data-stu-id="db2be-117">-Id</span></span>
<span data-ttu-id="db2be-118">Specifica l'ID di un processo che il cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="db2be-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="db2be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db2be-119">-ResourceGroupName</span></span>
<span data-ttu-id="db2be-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet riprende un processo.</span><span class="sxs-lookup"><span data-stu-id="db2be-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="db2be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2be-121">CommonParameters</span></span>
<span data-ttu-id="db2be-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2be-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2be-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2be-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="db2be-124">INPUTS</span></span>

### <span data-ttu-id="db2be-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="db2be-125">System.Guid</span></span>

### <span data-ttu-id="db2be-126">System.String</span><span class="sxs-lookup"><span data-stu-id="db2be-126">System.String</span></span>

## <span data-ttu-id="db2be-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db2be-127">OUTPUTS</span></span>

### <span data-ttu-id="db2be-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="db2be-128">System.Void</span></span>

## <span data-ttu-id="db2be-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="db2be-129">NOTES</span></span>

## <span data-ttu-id="db2be-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db2be-130">RELATED LINKS</span></span>

[<span data-ttu-id="db2be-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="db2be-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="db2be-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="db2be-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="db2be-133">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="db2be-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="db2be-134">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="db2be-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


