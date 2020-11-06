---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 05747721219610524e0a245df5b5a67e8e69b483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519931"
---
# <span data-ttu-id="c7528-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c7528-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="c7528-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7528-102">SYNOPSIS</span></span>
<span data-ttu-id="c7528-103">Sospende un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="c7528-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7528-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7528-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7528-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7528-105">DESCRIPTION</span></span>
<span data-ttu-id="c7528-106">Il cmdlet **Suspend-AzureRmAutomationJob** sospende un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7528-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="c7528-107">Specificare un processo di automazione in corso.</span><span class="sxs-lookup"><span data-stu-id="c7528-107">Specify a running Automation job.</span></span>

<span data-ttu-id="c7528-108">Per riprendere un processo sospeso, usare il cmdlet Resume-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="c7528-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="c7528-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7528-109">EXAMPLES</span></span>

### <span data-ttu-id="c7528-110">Esempio 1: sospendere un processo</span><span class="sxs-lookup"><span data-stu-id="c7528-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c7528-111">Questo comando sospende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="c7528-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="c7528-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7528-112">PARAMETERS</span></span>

### <span data-ttu-id="c7528-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c7528-113">-AutomationAccountName</span></span>
<span data-ttu-id="c7528-114">Specifica il nome di un account di automazione in cui questo cmdlet sospende un processo.</span><span class="sxs-lookup"><span data-stu-id="c7528-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7528-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7528-115">-DefaultProfile</span></span>
<span data-ttu-id="c7528-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c7528-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7528-117">-ID</span><span class="sxs-lookup"><span data-stu-id="c7528-117">-Id</span></span>
<span data-ttu-id="c7528-118">Specifica l'ID di un processo sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7528-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7528-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7528-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7528-120">Specifica l'ID di un processo sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7528-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7528-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7528-121">CommonParameters</span></span>
<span data-ttu-id="c7528-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7528-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7528-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7528-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7528-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7528-124">INPUTS</span></span>

### <span data-ttu-id="c7528-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c7528-125">None</span></span>
<span data-ttu-id="c7528-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c7528-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7528-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7528-127">OUTPUTS</span></span>

## <span data-ttu-id="c7528-128">Note</span><span class="sxs-lookup"><span data-stu-id="c7528-128">NOTES</span></span>

## <span data-ttu-id="c7528-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7528-129">RELATED LINKS</span></span>

[<span data-ttu-id="c7528-130">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c7528-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="c7528-131">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c7528-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="c7528-132">Curriculum vitae-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c7528-132">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="c7528-133">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c7528-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


