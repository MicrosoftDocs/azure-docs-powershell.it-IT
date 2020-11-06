---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 213df264e4ecd458c8505d521556f49265577333
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519769"
---
# <span data-ttu-id="ec1f9-101">Get-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ec1f9-101">Get-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="ec1f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ec1f9-103">Ottiene i processi di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-103">Gets Azure Automation source control sync jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec1f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec1f9-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec1f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec1f9-105">DESCRIPTION</span></span>
<span data-ttu-id="ec1f9-106">Il cmdlet Get-AzureRmAutomationSourceControlSyncJob ottiene i processi di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-106">The Get-AzureRmAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="ec1f9-107">Per ottenere un processo di sincronizzazione del controllo del codice sorgente specifico, specificare il relativo ID.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="ec1f9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec1f9-108">EXAMPLES</span></span>

### <span data-ttu-id="ec1f9-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec1f9-109">Example 1</span></span>
<span data-ttu-id="ec1f9-110">Questo comando consente di ottenere tutti i processi di sincronizzazione del controllo del codice sorgente di automazione per il controllo VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="ec1f9-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ec1f9-111">Example 2</span></span>
<span data-ttu-id="ec1f9-112">Questo comando ottiene il processo di sincronizzazione del controllo del codice sorgente con ID 08d6d266-27b6-463c-beea-bc48a67ace15 per il controllo del codice sorgente VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="ec1f9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec1f9-113">PARAMETERS</span></span>

### <span data-ttu-id="ec1f9-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ec1f9-114">-AutomationAccountName</span></span>
<span data-ttu-id="ec1f9-115">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-115">The automation account name.</span></span>

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

### <span data-ttu-id="ec1f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec1f9-116">-DefaultProfile</span></span>
<span data-ttu-id="ec1f9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec1f9-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="ec1f9-118">-JobId</span></span>
<span data-ttu-id="ec1f9-119">ID processo di sincronizzazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-119">The source control sync job id.</span></span>

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

### <span data-ttu-id="ec1f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec1f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec1f9-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-121">The resource group name.</span></span>

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

### <span data-ttu-id="ec1f9-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="ec1f9-122">-SourceControlName</span></span>
<span data-ttu-id="ec1f9-123">Nome del controllo del codice sorgente del processo.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="ec1f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec1f9-124">CommonParameters</span></span>
<span data-ttu-id="ec1f9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec1f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec1f9-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec1f9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec1f9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec1f9-127">INPUTS</span></span>

### <span data-ttu-id="ec1f9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ec1f9-128">System.String</span></span>

### <span data-ttu-id="ec1f9-129">System. Guid</span><span class="sxs-lookup"><span data-stu-id="ec1f9-129">System.Guid</span></span>

## <span data-ttu-id="ec1f9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec1f9-130">OUTPUTS</span></span>

### <span data-ttu-id="ec1f9-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ec1f9-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="ec1f9-132">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="ec1f9-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="ec1f9-133">Note</span><span class="sxs-lookup"><span data-stu-id="ec1f9-133">NOTES</span></span>

## <span data-ttu-id="ec1f9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec1f9-134">RELATED LINKS</span></span>
