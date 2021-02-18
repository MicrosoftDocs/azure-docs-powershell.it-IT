---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: a6d8a618ea9561c244b161407807ddfbe99b854a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201151"
---
# <span data-ttu-id="63a6f-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="63a6f-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="63a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="63a6f-103">Recupera i processi di sincronizzazione del controllo origine di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="63a6f-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="63a6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63a6f-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63a6f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="63a6f-106">Il cmdlet Get-AzAutomationSourceControlSyncJob cmdlet recupera i processi di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="63a6f-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="63a6f-107">Per ottenere un processo di sincronizzazione del controllo del codice sorgente specifico, specificarne l'ID.</span><span class="sxs-lookup"><span data-stu-id="63a6f-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="63a6f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63a6f-108">EXAMPLES</span></span>

### <span data-ttu-id="63a6f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="63a6f-109">Example 1</span></span>
<span data-ttu-id="63a6f-110">Questo comando recupera tutti i processi di sincronizzazione del controllo origine di automazione per il controllo di origine VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="63a6f-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="63a6f-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="63a6f-111">Example 2</span></span>
<span data-ttu-id="63a6f-112">Questo comando recupera il processo di sincronizzazione del controllo del codice sorgente con ID 08d6d266-27b6-463c-beea-bc48a67ace15 per il controllo di origine VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="63a6f-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="63a6f-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="63a6f-113">Example 3</span></span>

<span data-ttu-id="63a6f-114">Recupera i processi di sincronizzazione del controllo origine di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="63a6f-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="63a6f-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="63a6f-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="63a6f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63a6f-116">PARAMETERS</span></span>

### <span data-ttu-id="63a6f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="63a6f-117">-AutomationAccountName</span></span>
<span data-ttu-id="63a6f-118">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="63a6f-118">The automation account name.</span></span>

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

### <span data-ttu-id="63a6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a6f-119">-DefaultProfile</span></span>
<span data-ttu-id="63a6f-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63a6f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a6f-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="63a6f-121">-JobId</span></span>
<span data-ttu-id="63a6f-122">ID processo di sincronizzazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="63a6f-122">The source control sync job id.</span></span>

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

### <span data-ttu-id="63a6f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a6f-123">-ResourceGroupName</span></span>
<span data-ttu-id="63a6f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63a6f-124">The resource group name.</span></span>

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

### <span data-ttu-id="63a6f-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="63a6f-125">-SourceControlName</span></span>
<span data-ttu-id="63a6f-126">Nome del controllo dell'origine del processo.</span><span class="sxs-lookup"><span data-stu-id="63a6f-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="63a6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a6f-127">CommonParameters</span></span>
<span data-ttu-id="63a6f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a6f-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63a6f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a6f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="63a6f-130">INPUTS</span></span>

### <span data-ttu-id="63a6f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="63a6f-131">System.String</span></span>

### <span data-ttu-id="63a6f-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="63a6f-132">System.Guid</span></span>

## <span data-ttu-id="63a6f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63a6f-133">OUTPUTS</span></span>

### <span data-ttu-id="63a6f-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="63a6f-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="63a6f-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="63a6f-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="63a6f-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="63a6f-136">NOTES</span></span>

## <span data-ttu-id="63a6f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63a6f-137">RELATED LINKS</span></span>
