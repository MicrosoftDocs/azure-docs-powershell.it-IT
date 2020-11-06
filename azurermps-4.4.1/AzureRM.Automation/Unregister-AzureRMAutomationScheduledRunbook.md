---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: aa970f71be1e80f9eb5fcc1b4ec24cf0ce7f0e9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520796"
---
# <span data-ttu-id="9d2ac-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9d2ac-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="9d2ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="9d2ac-103">Rimuove un'associazione tra un Runbook e una programmazione.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d2ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d2ac-104">SYNTAX</span></span>

### <span data-ttu-id="9d2ac-105">ByJobScheduleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d2ac-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d2ac-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="9d2ac-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d2ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d2ac-107">DESCRIPTION</span></span>
<span data-ttu-id="9d2ac-108">Il cmdlet **Unregister-AzureRmAutomationScheduledRunbook** rimuove l'associazione tra un Runbook di automazione di Azure e una programmazione.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="9d2ac-109">La programmazione non avvia più il Runbook.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="9d2ac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d2ac-110">EXAMPLES</span></span>

### <span data-ttu-id="9d2ac-111">Esempio 1: rimuovere l'associazione tra un Runbook e una programmazione</span><span class="sxs-lookup"><span data-stu-id="9d2ac-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="9d2ac-112">Questo comando rimuove l'associazione tra Runbook denominata Runbk01 e la pianificazione denominata Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="9d2ac-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d2ac-113">PARAMETERS</span></span>

### <span data-ttu-id="9d2ac-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d2ac-114">-AutomationAccountName</span></span>
<span data-ttu-id="9d2ac-115">Specifica un account di automazione per il Runbook in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9d2ac-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9d2ac-116">-Force</span></span>
<span data-ttu-id="9d2ac-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="9d2ac-117">ps_force</span></span>

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

### <span data-ttu-id="9d2ac-118">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="9d2ac-118">-JobScheduleId</span></span>
<span data-ttu-id="9d2ac-119">Specifica l'ID di un Runbook programmato.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-119">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="9d2ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d2ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="9d2ac-121">Specifica il nome di un gruppo di risorse per il Runbook programmato.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-121">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="9d2ac-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="9d2ac-122">-RunbookName</span></span>
<span data-ttu-id="9d2ac-123">Specifica il nome del Runbook che questo cmdlet dissocia da una programmazione.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-123">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="9d2ac-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="9d2ac-124">-ScheduleName</span></span>
<span data-ttu-id="9d2ac-125">Specifica il nome della programmazione da cui questo cmdlet dissocia un Runbook.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-125">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="9d2ac-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d2ac-126">-Confirm</span></span>
<span data-ttu-id="9d2ac-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d2ac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d2ac-128">-WhatIf</span></span>
<span data-ttu-id="9d2ac-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d2ac-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d2ac-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d2ac-131">-DefaultProfile</span></span>
<span data-ttu-id="9d2ac-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d2ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d2ac-133">CommonParameters</span></span>
<span data-ttu-id="9d2ac-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d2ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d2ac-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d2ac-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d2ac-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d2ac-136">INPUTS</span></span>

## <span data-ttu-id="9d2ac-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d2ac-137">OUTPUTS</span></span>

## <span data-ttu-id="9d2ac-138">Note</span><span class="sxs-lookup"><span data-stu-id="9d2ac-138">NOTES</span></span>

## <span data-ttu-id="9d2ac-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d2ac-139">RELATED LINKS</span></span>

[<span data-ttu-id="9d2ac-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9d2ac-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="9d2ac-141">Registro-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9d2ac-141">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


