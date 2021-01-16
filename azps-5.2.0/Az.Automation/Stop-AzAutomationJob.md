---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344992"
---
# <span data-ttu-id="2bd88-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="2bd88-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="2bd88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bd88-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd88-103">Interrompe un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="2bd88-103">Stops an Automation job.</span></span>

## <span data-ttu-id="2bd88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bd88-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bd88-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bd88-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd88-106">Il cmdlet **Stop-AzAutomationJob** arresta un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd88-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="2bd88-107">Specificare un processo di automazione in corso.</span><span class="sxs-lookup"><span data-stu-id="2bd88-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="2bd88-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bd88-108">EXAMPLES</span></span>

### <span data-ttu-id="2bd88-109">Esempio 1: arrestare un processo</span><span class="sxs-lookup"><span data-stu-id="2bd88-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2bd88-110">Questo comando Arresta il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="2bd88-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="2bd88-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bd88-111">PARAMETERS</span></span>

### <span data-ttu-id="2bd88-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2bd88-112">-AutomationAccountName</span></span>
<span data-ttu-id="2bd88-113">Specifica il nome di un account di automazione in cui questo cmdlet arresta un processo.</span><span class="sxs-lookup"><span data-stu-id="2bd88-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="2bd88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd88-114">-DefaultProfile</span></span>
<span data-ttu-id="2bd88-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2bd88-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bd88-116">-ID</span><span class="sxs-lookup"><span data-stu-id="2bd88-116">-Id</span></span>
<span data-ttu-id="2bd88-117">Specifica l'ID di un processo interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd88-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2bd88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd88-118">-ResourceGroupName</span></span>
<span data-ttu-id="2bd88-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2bd88-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2bd88-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd88-120">CommonParameters</span></span>
<span data-ttu-id="2bd88-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd88-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd88-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd88-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd88-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bd88-123">INPUTS</span></span>

### <span data-ttu-id="2bd88-124">System. Guid</span><span class="sxs-lookup"><span data-stu-id="2bd88-124">System.Guid</span></span>

### <span data-ttu-id="2bd88-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2bd88-125">System.String</span></span>

## <span data-ttu-id="2bd88-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bd88-126">OUTPUTS</span></span>

### <span data-ttu-id="2bd88-127">System. void</span><span class="sxs-lookup"><span data-stu-id="2bd88-127">System.Void</span></span>

## <span data-ttu-id="2bd88-128">Note</span><span class="sxs-lookup"><span data-stu-id="2bd88-128">NOTES</span></span>

## <span data-ttu-id="2bd88-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bd88-129">RELATED LINKS</span></span>

[<span data-ttu-id="2bd88-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="2bd88-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="2bd88-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="2bd88-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="2bd88-132">Curriculum vitae-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="2bd88-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="2bd88-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="2bd88-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


