---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 369dfd85b88b079e32e9ea65513d37c99f64b6fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014142"
---
# <span data-ttu-id="6cd51-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="6cd51-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="6cd51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cd51-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd51-103">Ottiene l'output di un processo di sincronizzazione del controllo origine di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6cd51-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="6cd51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cd51-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cd51-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6cd51-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd51-106">Il cmdlet **Get-AzAutomationSourceControlSyncJobOutput** ottiene l'output per un processo di sincronizzazione del controllo origine di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd51-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="6cd51-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cd51-107">EXAMPLES</span></span>

### <span data-ttu-id="6cd51-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6cd51-108">Example 1</span></span>
<span data-ttu-id="6cd51-109">Questo comando ottiene l'output del processo di sincronizzazione del controllo del codice sorgente con ID 08d6d266-27b6-463c-beea-bc48a67ace15 per il controllo del codice sorgente VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="6cd51-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="6cd51-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cd51-110">PARAMETERS</span></span>

### <span data-ttu-id="6cd51-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6cd51-111">-AutomationAccountName</span></span>
<span data-ttu-id="6cd51-112">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="6cd51-112">The automation account name.</span></span>

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

### <span data-ttu-id="6cd51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd51-113">-DefaultProfile</span></span>
<span data-ttu-id="6cd51-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd51-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cd51-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="6cd51-115">-JobId</span></span>
<span data-ttu-id="6cd51-116">ID del processo di sincronizzazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="6cd51-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd51-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd51-117">-ResourceGroupName</span></span>
<span data-ttu-id="6cd51-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6cd51-118">The resource group name.</span></span>

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

### <span data-ttu-id="6cd51-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="6cd51-119">-SourceControlName</span></span>
<span data-ttu-id="6cd51-120">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="6cd51-120">The source control name.</span></span>

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

### <span data-ttu-id="6cd51-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="6cd51-121">-Stream</span></span>
<span data-ttu-id="6cd51-122">Tipo di flusso.</span><span class="sxs-lookup"><span data-stu-id="6cd51-122">The stream type.</span></span>
<span data-ttu-id="6cd51-123">L'impostazione predefinita è Any.</span><span class="sxs-lookup"><span data-stu-id="6cd51-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd51-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="6cd51-124">-StreamId</span></span>
<span data-ttu-id="6cd51-125">ID flusso.</span><span class="sxs-lookup"><span data-stu-id="6cd51-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd51-126">CommonParameters</span></span>
<span data-ttu-id="6cd51-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd51-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd51-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd51-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="6cd51-129">INPUTS</span></span>

### <span data-ttu-id="6cd51-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6cd51-130">System.String</span></span>

### <span data-ttu-id="6cd51-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6cd51-131">System.Guid</span></span>

### <span data-ttu-id="6cd51-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="6cd51-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="6cd51-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cd51-133">OUTPUTS</span></span>

### <span data-ttu-id="6cd51-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="6cd51-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="6cd51-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="6cd51-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="6cd51-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="6cd51-136">NOTES</span></span>

## <span data-ttu-id="6cd51-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cd51-137">RELATED LINKS</span></span>
