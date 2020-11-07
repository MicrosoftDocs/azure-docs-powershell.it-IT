---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 8fa14eef62ac0e8a296349ff3a47cd67086bc3ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685052"
---
# <span data-ttu-id="53d91-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="53d91-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="53d91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53d91-102">SYNOPSIS</span></span>
<span data-ttu-id="53d91-103">Ottiene i processi di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="53d91-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="53d91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53d91-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53d91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53d91-105">DESCRIPTION</span></span>
<span data-ttu-id="53d91-106">Il cmdlet Get-AzAutomationSourceControlSyncJob ottiene i processi di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="53d91-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="53d91-107">Per ottenere un processo di sincronizzazione del controllo del codice sorgente specifico, specificare il relativo ID.</span><span class="sxs-lookup"><span data-stu-id="53d91-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="53d91-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53d91-108">EXAMPLES</span></span>

### <span data-ttu-id="53d91-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53d91-109">Example 1</span></span>
<span data-ttu-id="53d91-110">Questo comando consente di ottenere tutti i processi di sincronizzazione del controllo del codice sorgente di automazione per il controllo VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="53d91-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="53d91-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="53d91-111">Example 2</span></span>
<span data-ttu-id="53d91-112">Questo comando ottiene il processo di sincronizzazione del controllo del codice sorgente con ID 08d6d266-27b6-463c-beea-bc48a67ace15 per il controllo del codice sorgente VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="53d91-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="53d91-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53d91-113">PARAMETERS</span></span>

### <span data-ttu-id="53d91-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="53d91-114">-AutomationAccountName</span></span>
<span data-ttu-id="53d91-115">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="53d91-115">The automation account name.</span></span>

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

### <span data-ttu-id="53d91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d91-116">-DefaultProfile</span></span>
<span data-ttu-id="53d91-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53d91-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53d91-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="53d91-118">-JobId</span></span>
<span data-ttu-id="53d91-119">ID processo di sincronizzazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="53d91-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53d91-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53d91-120">-ResourceGroupName</span></span>
<span data-ttu-id="53d91-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="53d91-121">The resource group name.</span></span>

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

### <span data-ttu-id="53d91-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="53d91-122">-SourceControlName</span></span>
<span data-ttu-id="53d91-123">Nome del controllo del codice sorgente del processo.</span><span class="sxs-lookup"><span data-stu-id="53d91-123">The source control name of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d91-124">CommonParameters</span></span>
<span data-ttu-id="53d91-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53d91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d91-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53d91-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d91-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53d91-127">INPUTS</span></span>

### <span data-ttu-id="53d91-128">System. String</span><span class="sxs-lookup"><span data-stu-id="53d91-128">System.String</span></span>

### <span data-ttu-id="53d91-129">System. Guid</span><span class="sxs-lookup"><span data-stu-id="53d91-129">System.Guid</span></span>

## <span data-ttu-id="53d91-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53d91-130">OUTPUTS</span></span>

### <span data-ttu-id="53d91-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="53d91-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="53d91-132">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="53d91-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="53d91-133">Note</span><span class="sxs-lookup"><span data-stu-id="53d91-133">NOTES</span></span>

## <span data-ttu-id="53d91-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53d91-134">RELATED LINKS</span></span>
