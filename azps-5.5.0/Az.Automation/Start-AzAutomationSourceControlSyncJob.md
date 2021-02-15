---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182086"
---
# <span data-ttu-id="60a8b-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="60a8b-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="60a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="60a8b-103">Avvia un processo di sincronizzazione del controllo origine di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="60a8b-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="60a8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60a8b-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a8b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="60a8b-106">Il cmdlet Start-AzAutomationSourceControlSyncJob avvia un processo di sincronizzazione del controllo del codice sorgente di Azure Automation per il nome del controllo origine specificato.</span><span class="sxs-lookup"><span data-stu-id="60a8b-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="60a8b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60a8b-107">EXAMPLES</span></span>

### <span data-ttu-id="60a8b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60a8b-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="60a8b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60a8b-109">PARAMETERS</span></span>

### <span data-ttu-id="60a8b-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60a8b-110">-AutomationAccountName</span></span>
<span data-ttu-id="60a8b-111">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="60a8b-111">The automation account name.</span></span>

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

### <span data-ttu-id="60a8b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a8b-112">-DefaultProfile</span></span>
<span data-ttu-id="60a8b-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60a8b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a8b-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="60a8b-114">-JobId</span></span>
<span data-ttu-id="60a8b-115">ID processo di sincronizzazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="60a8b-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a8b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a8b-116">-ResourceGroupName</span></span>
<span data-ttu-id="60a8b-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60a8b-117">The resource group name.</span></span>

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

### <span data-ttu-id="60a8b-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="60a8b-118">-SourceControlName</span></span>
<span data-ttu-id="60a8b-119">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="60a8b-119">The source control name.</span></span>

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

### <span data-ttu-id="60a8b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60a8b-120">-Confirm</span></span>
<span data-ttu-id="60a8b-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a8b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a8b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a8b-122">-WhatIf</span></span>
<span data-ttu-id="60a8b-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a8b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a8b-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a8b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a8b-125">CommonParameters</span></span>
<span data-ttu-id="60a8b-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a8b-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a8b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a8b-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="60a8b-128">INPUTS</span></span>

### <span data-ttu-id="60a8b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="60a8b-129">System.String</span></span>

## <span data-ttu-id="60a8b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60a8b-130">OUTPUTS</span></span>

### <span data-ttu-id="60a8b-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="60a8b-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="60a8b-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="60a8b-132">NOTES</span></span>

## <span data-ttu-id="60a8b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60a8b-133">RELATED LINKS</span></span>
