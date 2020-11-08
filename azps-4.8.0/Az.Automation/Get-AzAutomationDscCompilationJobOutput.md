---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031428"
---
# <span data-ttu-id="b8c78-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b8c78-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="b8c78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8c78-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c78-103">Ottiene i flussi di registrazione di un processo di compilazione DSC di automazione.</span><span class="sxs-lookup"><span data-stu-id="b8c78-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="b8c78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8c78-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c78-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8c78-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c78-106">Il cmdlet **Get-AzAutomationDscCompilationJobOutput** ottiene i record di flusso di un processo di compilazione della configurazione DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b8c78-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="b8c78-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8c78-107">EXAMPLES</span></span>

### <span data-ttu-id="b8c78-108">Esempio 1: ottenere i registri per un processo di compilazione DSC</span><span class="sxs-lookup"><span data-stu-id="b8c78-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="b8c78-109">Il primo comando consente di ottenere i processi di compilazione nell'account di automazione denominato Contoso17 usando il cmdlet Get-AzAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="b8c78-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="b8c78-110">Il comando Archivia gli oggetti nella variabile $Jobs.</span><span class="sxs-lookup"><span data-stu-id="b8c78-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="b8c78-111">Il secondo comando ottiene l'output del processo di compilazione per qualsiasi flusso per il primo membro della matrice $Jobs.</span><span class="sxs-lookup"><span data-stu-id="b8c78-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="b8c78-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8c78-112">PARAMETERS</span></span>

### <span data-ttu-id="b8c78-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b8c78-113">-AutomationAccountName</span></span>
<span data-ttu-id="b8c78-114">Specifica il nome dell'account di automazione che contiene il processo di compilazione DSC.</span><span class="sxs-lookup"><span data-stu-id="b8c78-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="b8c78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c78-115">-DefaultProfile</span></span>
<span data-ttu-id="b8c78-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b8c78-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8c78-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b8c78-117">-Id</span></span>
<span data-ttu-id="b8c78-118">Specifica l'ID univoco del processo di compilazione DSC per cui questo cmdlet ottiene l'output.</span><span class="sxs-lookup"><span data-stu-id="b8c78-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="b8c78-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c78-119">-ResourceGroupName</span></span>
<span data-ttu-id="b8c78-120">Specifica il nome del gruppo di risorse che contiene il processo di compilazione DSC per il quale questo cmdlet ottiene i record del flusso.</span><span class="sxs-lookup"><span data-stu-id="b8c78-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="b8c78-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b8c78-121">-StartTime</span></span>
<span data-ttu-id="b8c78-122">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="b8c78-122">Specifies a start time.</span></span>
<span data-ttu-id="b8c78-123">Questo cmdlet ottiene i record Stream che il processo di compilazione DSC restituisce dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="b8c78-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="b8c78-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="b8c78-124">-Stream</span></span>
<span data-ttu-id="b8c78-125">Specifica il tipo di flusso per l'output ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c78-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="b8c78-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b8c78-126">Valid values are:</span></span> 
- <span data-ttu-id="b8c78-127">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c78-127">Any</span></span> 
- <span data-ttu-id="b8c78-128">Avviso</span><span class="sxs-lookup"><span data-stu-id="b8c78-128">Warning</span></span> 
- <span data-ttu-id="b8c78-129">Errore</span><span class="sxs-lookup"><span data-stu-id="b8c78-129">Error</span></span> 
- <span data-ttu-id="b8c78-130">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="b8c78-130">Verbose</span></span>

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

### <span data-ttu-id="b8c78-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c78-131">CommonParameters</span></span>
<span data-ttu-id="b8c78-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c78-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c78-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c78-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c78-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8c78-134">INPUTS</span></span>

### <span data-ttu-id="b8c78-135">System. Guid</span><span class="sxs-lookup"><span data-stu-id="b8c78-135">System.Guid</span></span>

### <span data-ttu-id="b8c78-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="b8c78-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="b8c78-137">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8c78-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8c78-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b8c78-138">System.String</span></span>

## <span data-ttu-id="b8c78-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8c78-139">OUTPUTS</span></span>

### <span data-ttu-id="b8c78-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="b8c78-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="b8c78-141">Note</span><span class="sxs-lookup"><span data-stu-id="b8c78-141">NOTES</span></span>

## <span data-ttu-id="b8c78-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8c78-142">RELATED LINKS</span></span>

[<span data-ttu-id="b8c78-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b8c78-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="b8c78-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b8c78-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


