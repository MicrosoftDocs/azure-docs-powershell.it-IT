---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 8e84f2f66703410b626769be8c2c2d5a57e531e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511979"
---
# <span data-ttu-id="4a6bb-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4a6bb-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="4a6bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6bb-103">Riprende un processo di automazione sospesa.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a6bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a6bb-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a6bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a6bb-105">DESCRIPTION</span></span>
<span data-ttu-id="4a6bb-106">Il cmdlet **Resume-AzureRmAutomationJob** riprende un processo di automazione di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="4a6bb-107">Specificare il processo sospeso.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-107">Specify the suspended job.</span></span>
<span data-ttu-id="4a6bb-108">Per sospendere un processo, usare il cmdlet Suspend-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="4a6bb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a6bb-109">EXAMPLES</span></span>

### <span data-ttu-id="4a6bb-110">Esempio 1: riprendere un processo sospeso</span><span class="sxs-lookup"><span data-stu-id="4a6bb-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4a6bb-111">Questo comando riprende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="4a6bb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a6bb-112">PARAMETERS</span></span>

### <span data-ttu-id="4a6bb-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4a6bb-113">-AutomationAccountName</span></span>
<span data-ttu-id="4a6bb-114">Specifica il nome di un account di automazione in cui questo cmdlet riprende un processo.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="4a6bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6bb-115">-DefaultProfile</span></span>
<span data-ttu-id="4a6bb-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a6bb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a6bb-117">-ID</span><span class="sxs-lookup"><span data-stu-id="4a6bb-117">-Id</span></span>
<span data-ttu-id="4a6bb-118">Specifica l'ID di un processo che questo cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="4a6bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a6bb-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet riprende un processo.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="4a6bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6bb-121">CommonParameters</span></span>
<span data-ttu-id="4a6bb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6bb-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a6bb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6bb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a6bb-124">INPUTS</span></span>

### <span data-ttu-id="4a6bb-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="4a6bb-125">System.Guid</span></span>

### <span data-ttu-id="4a6bb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4a6bb-126">System.String</span></span>

## <span data-ttu-id="4a6bb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a6bb-127">OUTPUTS</span></span>

### <span data-ttu-id="4a6bb-128">System. void</span><span class="sxs-lookup"><span data-stu-id="4a6bb-128">System.Void</span></span>

## <span data-ttu-id="4a6bb-129">Note</span><span class="sxs-lookup"><span data-stu-id="4a6bb-129">NOTES</span></span>

## <span data-ttu-id="4a6bb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a6bb-130">RELATED LINKS</span></span>

[<span data-ttu-id="4a6bb-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4a6bb-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="4a6bb-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="4a6bb-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="4a6bb-133">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4a6bb-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="4a6bb-134">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4a6bb-134">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


