---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: 67100c80a3a0ca822fc1f37f63968be282925b76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509367"
---
# <span data-ttu-id="03b8d-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="03b8d-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="03b8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="03b8d-103">Interrompe un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="03b8d-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03b8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03b8d-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03b8d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="03b8d-106">Il cmdlet **Stop-AzureRmAutomationJob** arresta un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="03b8d-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="03b8d-107">Specificare un processo di automazione in corso.</span><span class="sxs-lookup"><span data-stu-id="03b8d-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="03b8d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03b8d-108">EXAMPLES</span></span>

### <span data-ttu-id="03b8d-109">Esempio 1: arrestare un processo</span><span class="sxs-lookup"><span data-stu-id="03b8d-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="03b8d-110">Questo comando Arresta il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="03b8d-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="03b8d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03b8d-111">PARAMETERS</span></span>

### <span data-ttu-id="03b8d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03b8d-112">-AutomationAccountName</span></span>
<span data-ttu-id="03b8d-113">Specifica il nome di un account di automazione in cui questo cmdlet arresta un processo.</span><span class="sxs-lookup"><span data-stu-id="03b8d-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="03b8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b8d-114">-DefaultProfile</span></span>
<span data-ttu-id="03b8d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="03b8d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03b8d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="03b8d-116">-Id</span></span>
<span data-ttu-id="03b8d-117">Specifica l'ID di un processo interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b8d-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="03b8d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b8d-118">-ResourceGroupName</span></span>
<span data-ttu-id="03b8d-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03b8d-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="03b8d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b8d-120">CommonParameters</span></span>
<span data-ttu-id="03b8d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b8d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b8d-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b8d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b8d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03b8d-123">INPUTS</span></span>

### <span data-ttu-id="03b8d-124">System. Guid</span><span class="sxs-lookup"><span data-stu-id="03b8d-124">System.Guid</span></span>

### <span data-ttu-id="03b8d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="03b8d-125">System.String</span></span>

## <span data-ttu-id="03b8d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03b8d-126">OUTPUTS</span></span>

### <span data-ttu-id="03b8d-127">System. void</span><span class="sxs-lookup"><span data-stu-id="03b8d-127">System.Void</span></span>

## <span data-ttu-id="03b8d-128">Note</span><span class="sxs-lookup"><span data-stu-id="03b8d-128">NOTES</span></span>

## <span data-ttu-id="03b8d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03b8d-129">RELATED LINKS</span></span>

[<span data-ttu-id="03b8d-130">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="03b8d-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="03b8d-131">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="03b8d-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="03b8d-132">Curriculum vitae-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="03b8d-132">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="03b8d-133">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="03b8d-133">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


