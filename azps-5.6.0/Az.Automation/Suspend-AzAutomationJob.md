---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 035cd77ab389b9c3cdce686620b3157b4b046c41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981277"
---
# <span data-ttu-id="dca54-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dca54-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="dca54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca54-102">SYNOPSIS</span></span>
<span data-ttu-id="dca54-103">Sospende un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="dca54-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="dca54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dca54-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dca54-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dca54-105">DESCRIPTION</span></span>
<span data-ttu-id="dca54-106">Il cmdlet **Suspend-AzAutomationJob** sospende un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dca54-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="dca54-107">Specificare un processo di automazione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dca54-107">Specify a running Automation job.</span></span>
<span data-ttu-id="dca54-108">Per riprendere un processo sospeso, usare il cmdlet Resume-AzAutomationJob lavoro sospeso.</span><span class="sxs-lookup"><span data-stu-id="dca54-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="dca54-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dca54-109">EXAMPLES</span></span>

### <span data-ttu-id="dca54-110">Esempio 1: Sospendere un processo</span><span class="sxs-lookup"><span data-stu-id="dca54-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dca54-111">Questo comando sospende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="dca54-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="dca54-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dca54-112">PARAMETERS</span></span>

### <span data-ttu-id="dca54-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dca54-113">-AutomationAccountName</span></span>
<span data-ttu-id="dca54-114">Specifica il nome di un account di automazione in cui questo cmdlet sospende un processo.</span><span class="sxs-lookup"><span data-stu-id="dca54-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="dca54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca54-115">-DefaultProfile</span></span>
<span data-ttu-id="dca54-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dca54-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dca54-117">-Id</span><span class="sxs-lookup"><span data-stu-id="dca54-117">-Id</span></span>
<span data-ttu-id="dca54-118">Specifica l'ID di un processo che il cmdlet sospende.</span><span class="sxs-lookup"><span data-stu-id="dca54-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="dca54-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca54-119">-ResourceGroupName</span></span>
<span data-ttu-id="dca54-120">Specifica l'ID di un processo che il cmdlet sospende.</span><span class="sxs-lookup"><span data-stu-id="dca54-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="dca54-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca54-121">CommonParameters</span></span>
<span data-ttu-id="dca54-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dca54-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca54-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca54-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca54-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="dca54-124">INPUTS</span></span>

### <span data-ttu-id="dca54-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="dca54-125">System.Guid</span></span>

### <span data-ttu-id="dca54-126">System.String</span><span class="sxs-lookup"><span data-stu-id="dca54-126">System.String</span></span>

## <span data-ttu-id="dca54-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dca54-127">OUTPUTS</span></span>

### <span data-ttu-id="dca54-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="dca54-128">System.Void</span></span>

## <span data-ttu-id="dca54-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="dca54-129">NOTES</span></span>

## <span data-ttu-id="dca54-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dca54-130">RELATED LINKS</span></span>

[<span data-ttu-id="dca54-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dca54-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="dca54-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="dca54-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="dca54-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dca54-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="dca54-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dca54-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


