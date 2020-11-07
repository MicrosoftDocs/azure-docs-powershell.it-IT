---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: cc9f402400b0290d8cf36dc38d59a45e29ce770c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687735"
---
# <span data-ttu-id="d1407-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d1407-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="d1407-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1407-102">SYNOPSIS</span></span>
<span data-ttu-id="d1407-103">Sospende un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="d1407-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1407-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1407-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1407-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1407-105">DESCRIPTION</span></span>
<span data-ttu-id="d1407-106">Il cmdlet **Suspend-AzureRmAutomationJob** sospende un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1407-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="d1407-107">Specificare un processo di automazione in corso.</span><span class="sxs-lookup"><span data-stu-id="d1407-107">Specify a running Automation job.</span></span>

<span data-ttu-id="d1407-108">Per riprendere un processo sospeso, usare il cmdlet Resume-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="d1407-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="d1407-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1407-109">EXAMPLES</span></span>

### <span data-ttu-id="d1407-110">Esempio 1: sospendere un processo</span><span class="sxs-lookup"><span data-stu-id="d1407-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d1407-111">Questo comando sospende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="d1407-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="d1407-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1407-112">PARAMETERS</span></span>

### <span data-ttu-id="d1407-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d1407-113">-AutomationAccountName</span></span>
<span data-ttu-id="d1407-114">Specifica il nome di un account di automazione in cui questo cmdlet sospende un processo.</span><span class="sxs-lookup"><span data-stu-id="d1407-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="d1407-115">-ID</span><span class="sxs-lookup"><span data-stu-id="d1407-115">-Id</span></span>
<span data-ttu-id="d1407-116">Specifica l'ID di un processo sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1407-116">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="d1407-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1407-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1407-118">Specifica l'ID di un processo sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1407-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="d1407-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1407-119">-DefaultProfile</span></span>
<span data-ttu-id="d1407-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1407-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1407-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1407-121">CommonParameters</span></span>
<span data-ttu-id="d1407-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1407-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1407-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1407-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1407-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1407-124">INPUTS</span></span>

## <span data-ttu-id="d1407-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1407-125">OUTPUTS</span></span>

## <span data-ttu-id="d1407-126">Note</span><span class="sxs-lookup"><span data-stu-id="d1407-126">NOTES</span></span>

## <span data-ttu-id="d1407-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1407-127">RELATED LINKS</span></span>

[<span data-ttu-id="d1407-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d1407-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="d1407-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d1407-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="d1407-130">Curriculum vitae-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d1407-130">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="d1407-131">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d1407-131">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


