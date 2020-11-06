---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: 0eedf88ed078c3532eb60a00b87733937344bafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512740"
---
# <span data-ttu-id="71efd-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="71efd-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="71efd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71efd-102">SYNOPSIS</span></span>
<span data-ttu-id="71efd-103">Interrompe un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="71efd-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71efd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71efd-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71efd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71efd-105">DESCRIPTION</span></span>
<span data-ttu-id="71efd-106">Il cmdlet **Stop-AzureRmAutomationJob** arresta un processo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="71efd-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="71efd-107">Specificare un processo di automazione in corso.</span><span class="sxs-lookup"><span data-stu-id="71efd-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="71efd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71efd-108">EXAMPLES</span></span>

### <span data-ttu-id="71efd-109">Esempio 1: arrestare un processo</span><span class="sxs-lookup"><span data-stu-id="71efd-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71efd-110">Questo comando Arresta il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="71efd-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="71efd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71efd-111">PARAMETERS</span></span>

### <span data-ttu-id="71efd-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71efd-112">-AutomationAccountName</span></span>
<span data-ttu-id="71efd-113">Specifica il nome di un account di automazione in cui questo cmdlet arresta un processo.</span><span class="sxs-lookup"><span data-stu-id="71efd-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="71efd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71efd-114">-DefaultProfile</span></span>
<span data-ttu-id="71efd-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="71efd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71efd-116">-ID</span><span class="sxs-lookup"><span data-stu-id="71efd-116">-Id</span></span>
<span data-ttu-id="71efd-117">Specifica l'ID di un processo interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71efd-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="71efd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71efd-118">-ResourceGroupName</span></span>
<span data-ttu-id="71efd-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71efd-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="71efd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71efd-120">CommonParameters</span></span>
<span data-ttu-id="71efd-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71efd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71efd-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71efd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71efd-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71efd-123">INPUTS</span></span>

### <span data-ttu-id="71efd-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="71efd-124">None</span></span>
<span data-ttu-id="71efd-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="71efd-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71efd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71efd-126">OUTPUTS</span></span>

## <span data-ttu-id="71efd-127">Note</span><span class="sxs-lookup"><span data-stu-id="71efd-127">NOTES</span></span>

## <span data-ttu-id="71efd-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71efd-128">RELATED LINKS</span></span>

[<span data-ttu-id="71efd-129">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="71efd-129">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="71efd-130">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="71efd-130">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="71efd-131">Curriculum vitae-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="71efd-131">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="71efd-132">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="71efd-132">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


