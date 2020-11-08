---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: a6d8a618ea9561c244b161407807ddfbe99b854a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201315"
---
# <span data-ttu-id="45381-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="45381-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="45381-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45381-102">SYNOPSIS</span></span>
<span data-ttu-id="45381-103">Ottiene i processi di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="45381-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="45381-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45381-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45381-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45381-105">DESCRIPTION</span></span>
<span data-ttu-id="45381-106">Il cmdlet Get-AzAutomationSourceControlSyncJob ottiene i processi di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="45381-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="45381-107">Per ottenere un processo di sincronizzazione del controllo del codice sorgente specifico, specificare il relativo ID.</span><span class="sxs-lookup"><span data-stu-id="45381-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="45381-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45381-108">EXAMPLES</span></span>

### <span data-ttu-id="45381-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45381-109">Example 1</span></span>
<span data-ttu-id="45381-110">Questo comando consente di ottenere tutti i processi di sincronizzazione del controllo del codice sorgente di automazione per il controllo VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="45381-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="45381-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="45381-111">Example 2</span></span>
<span data-ttu-id="45381-112">Questo comando ottiene il processo di sincronizzazione del controllo del codice sorgente con ID 08d6d266-27b6-463c-beea-bc48a67ace15 per il controllo del codice sorgente VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="45381-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="45381-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="45381-113">Example 3</span></span>

<span data-ttu-id="45381-114">Ottiene i processi di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="45381-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="45381-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="45381-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="45381-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45381-116">PARAMETERS</span></span>

### <span data-ttu-id="45381-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="45381-117">-AutomationAccountName</span></span>
<span data-ttu-id="45381-118">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="45381-118">The automation account name.</span></span>

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

### <span data-ttu-id="45381-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45381-119">-DefaultProfile</span></span>
<span data-ttu-id="45381-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45381-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45381-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="45381-121">-JobId</span></span>
<span data-ttu-id="45381-122">ID processo di sincronizzazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="45381-122">The source control sync job id.</span></span>

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

### <span data-ttu-id="45381-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45381-123">-ResourceGroupName</span></span>
<span data-ttu-id="45381-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="45381-124">The resource group name.</span></span>

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

### <span data-ttu-id="45381-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="45381-125">-SourceControlName</span></span>
<span data-ttu-id="45381-126">Nome del controllo del codice sorgente del processo.</span><span class="sxs-lookup"><span data-stu-id="45381-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="45381-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45381-127">CommonParameters</span></span>
<span data-ttu-id="45381-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45381-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45381-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45381-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45381-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45381-130">INPUTS</span></span>

### <span data-ttu-id="45381-131">System. String</span><span class="sxs-lookup"><span data-stu-id="45381-131">System.String</span></span>

### <span data-ttu-id="45381-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="45381-132">System.Guid</span></span>

## <span data-ttu-id="45381-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45381-133">OUTPUTS</span></span>

### <span data-ttu-id="45381-134">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="45381-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="45381-135">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="45381-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="45381-136">Note</span><span class="sxs-lookup"><span data-stu-id="45381-136">NOTES</span></span>

## <span data-ttu-id="45381-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45381-137">RELATED LINKS</span></span>
