---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 6567d479ad0db7df959e4059155149f4fc06e1a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022950"
---
# <span data-ttu-id="c95f7-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="c95f7-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="c95f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c95f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c95f7-103">Ottiene l'output di un processo di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c95f7-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="c95f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c95f7-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c95f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c95f7-105">DESCRIPTION</span></span>
<span data-ttu-id="c95f7-106">Il cmdlet **Get-AzAutomationSourceControlSyncJobOutput** Ottiene l'output per un processo di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c95f7-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="c95f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c95f7-107">EXAMPLES</span></span>

### <span data-ttu-id="c95f7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c95f7-108">Example 1</span></span>
<span data-ttu-id="c95f7-109">Questo comando ottiene l'output del processo di sincronizzazione del controllo del codice sorgente con ID 08d6d266-27b6-463c-beea-bc48a67ace15 per il controllo del codice sorgente VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="c95f7-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


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

## <span data-ttu-id="c95f7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c95f7-110">PARAMETERS</span></span>

### <span data-ttu-id="c95f7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c95f7-111">-AutomationAccountName</span></span>
<span data-ttu-id="c95f7-112">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="c95f7-112">The automation account name.</span></span>

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

### <span data-ttu-id="c95f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c95f7-113">-DefaultProfile</span></span>
<span data-ttu-id="c95f7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c95f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c95f7-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="c95f7-115">-JobId</span></span>
<span data-ttu-id="c95f7-116">ID processo di sincronizzazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="c95f7-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="c95f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c95f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c95f7-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c95f7-118">The resource group name.</span></span>

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

### <span data-ttu-id="c95f7-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="c95f7-119">-SourceControlName</span></span>
<span data-ttu-id="c95f7-120">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="c95f7-120">The source control name.</span></span>

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

### <span data-ttu-id="c95f7-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="c95f7-121">-Stream</span></span>
<span data-ttu-id="c95f7-122">Tipo di flusso.</span><span class="sxs-lookup"><span data-stu-id="c95f7-122">The stream type.</span></span>
<span data-ttu-id="c95f7-123">Il valore predefinito è any.</span><span class="sxs-lookup"><span data-stu-id="c95f7-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="c95f7-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="c95f7-124">-StreamId</span></span>
<span data-ttu-id="c95f7-125">ID flusso.</span><span class="sxs-lookup"><span data-stu-id="c95f7-125">The stream id.</span></span>

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

### <span data-ttu-id="c95f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c95f7-126">CommonParameters</span></span>
<span data-ttu-id="c95f7-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c95f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c95f7-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c95f7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c95f7-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c95f7-129">INPUTS</span></span>

### <span data-ttu-id="c95f7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c95f7-130">System.String</span></span>

### <span data-ttu-id="c95f7-131">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c95f7-131">System.Guid</span></span>

### <span data-ttu-id="c95f7-132">Microsoft. Azure. Commands. Automation. Common. SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="c95f7-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="c95f7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c95f7-133">OUTPUTS</span></span>

### <span data-ttu-id="c95f7-134">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="c95f7-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="c95f7-135">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="c95f7-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="c95f7-136">Note</span><span class="sxs-lookup"><span data-stu-id="c95f7-136">NOTES</span></span>

## <span data-ttu-id="c95f7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c95f7-137">RELATED LINKS</span></span>
