---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 6d23fe3728b569cbb1a2aee498d560672ee75877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517084"
---
# <span data-ttu-id="5d74d-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5d74d-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="5d74d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d74d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d74d-103">Riprende un processo di automazione sospesa.</span><span class="sxs-lookup"><span data-stu-id="5d74d-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d74d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d74d-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d74d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d74d-105">DESCRIPTION</span></span>
<span data-ttu-id="5d74d-106">Il cmdlet **Resume-AzureRmAutomationJob** riprende un processo di automazione di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="5d74d-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="5d74d-107">Specificare il processo sospeso.</span><span class="sxs-lookup"><span data-stu-id="5d74d-107">Specify the suspended job.</span></span>

<span data-ttu-id="5d74d-108">Per sospendere un processo, usare il cmdlet Suspend-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="5d74d-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="5d74d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d74d-109">EXAMPLES</span></span>

### <span data-ttu-id="5d74d-110">Esempio 1: riprendere un processo sospeso</span><span class="sxs-lookup"><span data-stu-id="5d74d-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5d74d-111">Questo comando riprende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="5d74d-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="5d74d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d74d-112">PARAMETERS</span></span>

### <span data-ttu-id="5d74d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5d74d-113">-AutomationAccountName</span></span>
<span data-ttu-id="5d74d-114">Specifica il nome di un account di automazione in cui questo cmdlet riprende un processo.</span><span class="sxs-lookup"><span data-stu-id="5d74d-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="5d74d-115">-ID</span><span class="sxs-lookup"><span data-stu-id="5d74d-115">-Id</span></span>
<span data-ttu-id="5d74d-116">Specifica l'ID di un processo che questo cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="5d74d-116">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="5d74d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d74d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d74d-118">Specifica il nome di un gruppo di risorse per cui questo cmdlet riprende un processo.</span><span class="sxs-lookup"><span data-stu-id="5d74d-118">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="5d74d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d74d-119">-DefaultProfile</span></span>
<span data-ttu-id="5d74d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d74d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d74d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d74d-121">CommonParameters</span></span>
<span data-ttu-id="5d74d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d74d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d74d-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d74d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d74d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d74d-124">INPUTS</span></span>

## <span data-ttu-id="5d74d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d74d-125">OUTPUTS</span></span>

## <span data-ttu-id="5d74d-126">Note</span><span class="sxs-lookup"><span data-stu-id="5d74d-126">NOTES</span></span>

## <span data-ttu-id="5d74d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d74d-127">RELATED LINKS</span></span>

[<span data-ttu-id="5d74d-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5d74d-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="5d74d-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="5d74d-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="5d74d-130">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5d74d-130">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="5d74d-131">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5d74d-131">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


