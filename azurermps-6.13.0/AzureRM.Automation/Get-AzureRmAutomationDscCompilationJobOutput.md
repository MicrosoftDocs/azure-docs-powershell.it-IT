---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: a7ddc25fa7c6bc52acbe9369c569db060cf63a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507692"
---
# <span data-ttu-id="defda-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="defda-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="defda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="defda-102">SYNOPSIS</span></span>
<span data-ttu-id="defda-103">Ottiene i flussi di registrazione di un processo di compilazione DSC di automazione.</span><span class="sxs-lookup"><span data-stu-id="defda-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="defda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="defda-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="defda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="defda-105">DESCRIPTION</span></span>
<span data-ttu-id="defda-106">Il cmdlet **Get-AzureRmAutomationDscCompilationJobOutput** ottiene i record di flusso di un processo di compilazione della configurazione DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="defda-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="defda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="defda-107">EXAMPLES</span></span>

### <span data-ttu-id="defda-108">Esempio 1: ottenere i registri per un processo di compilazione DSC</span><span class="sxs-lookup"><span data-stu-id="defda-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="defda-109">Il primo comando consente di ottenere i processi di compilazione nell'account di automazione denominato Contoso17 usando il cmdlet Get-AzureRmAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="defda-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="defda-110">Il comando Archivia gli oggetti nella variabile $Jobs.</span><span class="sxs-lookup"><span data-stu-id="defda-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="defda-111">Il secondo comando ottiene l'output del processo di compilazione per qualsiasi flusso per il primo membro della matrice $Jobs.</span><span class="sxs-lookup"><span data-stu-id="defda-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="defda-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="defda-112">PARAMETERS</span></span>

### <span data-ttu-id="defda-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="defda-113">-AutomationAccountName</span></span>
<span data-ttu-id="defda-114">Specifica il nome dell'account di automazione che contiene il processo di compilazione DSC.</span><span class="sxs-lookup"><span data-stu-id="defda-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="defda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="defda-115">-DefaultProfile</span></span>
<span data-ttu-id="defda-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="defda-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="defda-117">-ID</span><span class="sxs-lookup"><span data-stu-id="defda-117">-Id</span></span>
<span data-ttu-id="defda-118">Specifica l'ID univoco del processo di compilazione DSC per cui questo cmdlet ottiene l'output.</span><span class="sxs-lookup"><span data-stu-id="defda-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="defda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="defda-119">-ResourceGroupName</span></span>
<span data-ttu-id="defda-120">Specifica il nome del gruppo di risorse che contiene il processo di compilazione DSC per il quale questo cmdlet ottiene i record del flusso.</span><span class="sxs-lookup"><span data-stu-id="defda-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="defda-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="defda-121">-StartTime</span></span>
<span data-ttu-id="defda-122">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="defda-122">Specifies a start time.</span></span>
<span data-ttu-id="defda-123">Questo cmdlet ottiene i record Stream che il processo di compilazione DSC restituisce dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="defda-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defda-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="defda-124">-Stream</span></span>
<span data-ttu-id="defda-125">Specifica il tipo di flusso per l'output ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="defda-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="defda-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="defda-126">Valid values are:</span></span> 
- <span data-ttu-id="defda-127">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="defda-127">Any</span></span> 
- <span data-ttu-id="defda-128">Avviso</span><span class="sxs-lookup"><span data-stu-id="defda-128">Warning</span></span> 
- <span data-ttu-id="defda-129">Errore</span><span class="sxs-lookup"><span data-stu-id="defda-129">Error</span></span> 
- <span data-ttu-id="defda-130">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="defda-130">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defda-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defda-131">CommonParameters</span></span>
<span data-ttu-id="defda-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="defda-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defda-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="defda-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defda-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="defda-134">INPUTS</span></span>

### <span data-ttu-id="defda-135">System. Guid</span><span class="sxs-lookup"><span data-stu-id="defda-135">System.Guid</span></span>

### <span data-ttu-id="defda-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="defda-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="defda-137">System. Nullable ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="defda-137">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="defda-138">System. String</span><span class="sxs-lookup"><span data-stu-id="defda-138">System.String</span></span>

## <span data-ttu-id="defda-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="defda-139">OUTPUTS</span></span>

### <span data-ttu-id="defda-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="defda-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="defda-141">Note</span><span class="sxs-lookup"><span data-stu-id="defda-141">NOTES</span></span>

## <span data-ttu-id="defda-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="defda-142">RELATED LINKS</span></span>

[<span data-ttu-id="defda-143">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="defda-143">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="defda-144">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="defda-144">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


