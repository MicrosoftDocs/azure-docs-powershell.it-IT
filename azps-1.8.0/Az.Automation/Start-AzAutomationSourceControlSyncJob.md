---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 5f2c72eb3b456d19b51651bbed79676093ba8685
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684948"
---
# <span data-ttu-id="ee5d9-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ee5d9-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="ee5d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5d9-103">Avvia un processo di sincronizzazione del controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="ee5d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee5d9-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee5d9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="ee5d9-106">Il cmdlet Start-AzAutomationSourceControlSyncJob avvia un processo di sincronizzazione del controllo di origine di Azure Automation per il nome del controllo del codice sorgente indicato.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="ee5d9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee5d9-107">EXAMPLES</span></span>

### <span data-ttu-id="ee5d9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee5d9-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="ee5d9-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee5d9-109">PARAMETERS</span></span>

### <span data-ttu-id="ee5d9-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ee5d9-110">-AutomationAccountName</span></span>
<span data-ttu-id="ee5d9-111">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-111">The automation account name.</span></span>

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

### <span data-ttu-id="ee5d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5d9-112">-DefaultProfile</span></span>
<span data-ttu-id="ee5d9-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee5d9-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="ee5d9-114">-JobId</span></span>
<span data-ttu-id="ee5d9-115">ID processo di sincronizzazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="ee5d9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5d9-116">-ResourceGroupName</span></span>
<span data-ttu-id="ee5d9-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-117">The resource group name.</span></span>

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

### <span data-ttu-id="ee5d9-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="ee5d9-118">-SourceControlName</span></span>
<span data-ttu-id="ee5d9-119">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-119">The source control name.</span></span>

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

### <span data-ttu-id="ee5d9-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee5d9-120">-Confirm</span></span>
<span data-ttu-id="ee5d9-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee5d9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee5d9-122">-WhatIf</span></span>
<span data-ttu-id="ee5d9-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee5d9-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee5d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5d9-125">CommonParameters</span></span>
<span data-ttu-id="ee5d9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee5d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5d9-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee5d9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5d9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee5d9-128">INPUTS</span></span>

### <span data-ttu-id="ee5d9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ee5d9-129">System.String</span></span>

## <span data-ttu-id="ee5d9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee5d9-130">OUTPUTS</span></span>

### <span data-ttu-id="ee5d9-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ee5d9-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="ee5d9-132">Note</span><span class="sxs-lookup"><span data-stu-id="ee5d9-132">NOTES</span></span>

## <span data-ttu-id="ee5d9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee5d9-133">RELATED LINKS</span></span>