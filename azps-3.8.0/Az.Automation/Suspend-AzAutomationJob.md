---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022612"
---
# <span data-ttu-id="11334-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11334-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="11334-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11334-102">SYNOPSIS</span></span>
<span data-ttu-id="11334-103">Sospende un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="11334-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="11334-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11334-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11334-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11334-105">DESCRIPTION</span></span>
<span data-ttu-id="11334-106">Il cmdlet **Suspend-AzAutomationJob** sospende un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="11334-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="11334-107">Specificare un processo di automazione in corso.</span><span class="sxs-lookup"><span data-stu-id="11334-107">Specify a running Automation job.</span></span>
<span data-ttu-id="11334-108">Per riprendere un processo sospeso, usare il cmdlet Resume-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="11334-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="11334-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11334-109">EXAMPLES</span></span>

### <span data-ttu-id="11334-110">Esempio 1: sospendere un processo</span><span class="sxs-lookup"><span data-stu-id="11334-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="11334-111">Questo comando sospende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="11334-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="11334-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11334-112">PARAMETERS</span></span>

### <span data-ttu-id="11334-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11334-113">-AutomationAccountName</span></span>
<span data-ttu-id="11334-114">Specifica il nome di un account di automazione in cui questo cmdlet sospende un processo.</span><span class="sxs-lookup"><span data-stu-id="11334-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="11334-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11334-115">-DefaultProfile</span></span>
<span data-ttu-id="11334-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="11334-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11334-117">-ID</span><span class="sxs-lookup"><span data-stu-id="11334-117">-Id</span></span>
<span data-ttu-id="11334-118">Specifica l'ID di un processo sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11334-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="11334-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11334-119">-ResourceGroupName</span></span>
<span data-ttu-id="11334-120">Specifica l'ID di un processo sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11334-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="11334-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11334-121">CommonParameters</span></span>
<span data-ttu-id="11334-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11334-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11334-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11334-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11334-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11334-124">INPUTS</span></span>

### <span data-ttu-id="11334-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="11334-125">System.Guid</span></span>

### <span data-ttu-id="11334-126">System. String</span><span class="sxs-lookup"><span data-stu-id="11334-126">System.String</span></span>

## <span data-ttu-id="11334-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11334-127">OUTPUTS</span></span>

### <span data-ttu-id="11334-128">System. void</span><span class="sxs-lookup"><span data-stu-id="11334-128">System.Void</span></span>

## <span data-ttu-id="11334-129">Note</span><span class="sxs-lookup"><span data-stu-id="11334-129">NOTES</span></span>

## <span data-ttu-id="11334-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11334-130">RELATED LINKS</span></span>

[<span data-ttu-id="11334-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11334-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="11334-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="11334-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="11334-133">Curriculum vitae-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11334-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="11334-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11334-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


