---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478467"
---
# <span data-ttu-id="3659c-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3659c-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="3659c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3659c-102">SYNOPSIS</span></span>
<span data-ttu-id="3659c-103">Rimuove un'associazione tra un Runbook e una programmazione.</span><span class="sxs-lookup"><span data-stu-id="3659c-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="3659c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3659c-104">SYNTAX</span></span>

### <span data-ttu-id="3659c-105">ByJobScheduleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3659c-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3659c-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="3659c-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3659c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3659c-107">DESCRIPTION</span></span>
<span data-ttu-id="3659c-108">Il cmdlet **Unregister-AzAutomationScheduledRunbook** rimuove l'associazione tra un Runbook di automazione di Azure e una programmazione.</span><span class="sxs-lookup"><span data-stu-id="3659c-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="3659c-109">La programmazione non avvia più il Runbook.</span><span class="sxs-lookup"><span data-stu-id="3659c-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="3659c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3659c-110">EXAMPLES</span></span>

### <span data-ttu-id="3659c-111">Esempio 1: rimuovere l'associazione tra un Runbook e una programmazione</span><span class="sxs-lookup"><span data-stu-id="3659c-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="3659c-112">Questo comando rimuove l'associazione tra Runbook denominata Runbk01 e la pianificazione denominata Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="3659c-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="3659c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3659c-113">PARAMETERS</span></span>

### <span data-ttu-id="3659c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3659c-114">-AutomationAccountName</span></span>
<span data-ttu-id="3659c-115">Specifica un account di automazione per il Runbook in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3659c-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3659c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3659c-116">-DefaultProfile</span></span>
<span data-ttu-id="3659c-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3659c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3659c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3659c-118">-Force</span></span>
<span data-ttu-id="3659c-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="3659c-119">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3659c-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="3659c-120">-JobScheduleId</span></span>
<span data-ttu-id="3659c-121">Specifica l'ID di un Runbook programmato.</span><span class="sxs-lookup"><span data-stu-id="3659c-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3659c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3659c-122">-ResourceGroupName</span></span>
<span data-ttu-id="3659c-123">Specifica il nome di un gruppo di risorse per il Runbook programmato.</span><span class="sxs-lookup"><span data-stu-id="3659c-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="3659c-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="3659c-124">-RunbookName</span></span>
<span data-ttu-id="3659c-125">Specifica il nome del Runbook che questo cmdlet dissocia da una programmazione.</span><span class="sxs-lookup"><span data-stu-id="3659c-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3659c-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="3659c-126">-ScheduleName</span></span>
<span data-ttu-id="3659c-127">Specifica il nome della programmazione da cui questo cmdlet dissocia un Runbook.</span><span class="sxs-lookup"><span data-stu-id="3659c-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3659c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3659c-128">-Confirm</span></span>
<span data-ttu-id="3659c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3659c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3659c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3659c-130">-WhatIf</span></span>
<span data-ttu-id="3659c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3659c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3659c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3659c-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3659c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3659c-133">CommonParameters</span></span>
<span data-ttu-id="3659c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3659c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3659c-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3659c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3659c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3659c-136">INPUTS</span></span>

### <span data-ttu-id="3659c-137">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3659c-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3659c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3659c-138">System.String</span></span>

## <span data-ttu-id="3659c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3659c-139">OUTPUTS</span></span>

### <span data-ttu-id="3659c-140">System. void</span><span class="sxs-lookup"><span data-stu-id="3659c-140">System.Void</span></span>

## <span data-ttu-id="3659c-141">Note</span><span class="sxs-lookup"><span data-stu-id="3659c-141">NOTES</span></span>

## <span data-ttu-id="3659c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3659c-142">RELATED LINKS</span></span>

[<span data-ttu-id="3659c-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3659c-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="3659c-144">Registro-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3659c-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


