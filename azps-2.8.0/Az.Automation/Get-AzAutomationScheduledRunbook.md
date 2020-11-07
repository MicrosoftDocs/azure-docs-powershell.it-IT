---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 2444579c8a155cc2957ab8432eb63cc28300bfe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675792"
---
# <span data-ttu-id="68236-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="68236-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="68236-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68236-102">SYNOPSIS</span></span>
<span data-ttu-id="68236-103">Ottiene le manuali operativi di automazione e le pianificazioni associate.</span><span class="sxs-lookup"><span data-stu-id="68236-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="68236-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68236-104">SYNTAX</span></span>

### <span data-ttu-id="68236-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68236-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68236-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="68236-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68236-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="68236-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68236-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="68236-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68236-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="68236-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68236-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68236-110">DESCRIPTION</span></span>
<span data-ttu-id="68236-111">Il cmdlet **Get-AzAutomationScheduledRunbook** ottiene uno o più manuali operativi di automazione Azure e pianificazioni associate.</span><span class="sxs-lookup"><span data-stu-id="68236-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="68236-112">Per impostazione predefinita, questo cmdlet ottiene tutti i manuali operativi pianificati.</span><span class="sxs-lookup"><span data-stu-id="68236-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="68236-113">Specificare il nome di una Runbook o di una pianificazione oppure entrambe per visualizzare le pianificazioni specifiche di Runbook.</span><span class="sxs-lookup"><span data-stu-id="68236-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="68236-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68236-114">EXAMPLES</span></span>

### <span data-ttu-id="68236-115">Esempio 1: ottenere tutte le manuali operativi pianificate</span><span class="sxs-lookup"><span data-stu-id="68236-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="68236-116">Questo comando consente di ottenere tutte le manuali operativi pianificate nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68236-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="68236-117">Esempio 2: ottenere tutte le pianificazioni associate a un Runbook</span><span class="sxs-lookup"><span data-stu-id="68236-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="68236-118">Questo comando consente di ottenere tutte le manuali operativi pianificate per Runbook Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68236-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="68236-119">Esempio 3: ottenere tutti i manuali operativi associati a una pianificazione</span><span class="sxs-lookup"><span data-stu-id="68236-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="68236-120">Questo comando consente di ottenere tutte le manuali operativi pianificate per la pianificazione Schedule01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68236-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="68236-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68236-121">PARAMETERS</span></span>

### <span data-ttu-id="68236-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="68236-122">-AutomationAccountName</span></span>
<span data-ttu-id="68236-123">Specifica un account di automazione per il Runbook in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68236-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="68236-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68236-124">-DefaultProfile</span></span>
<span data-ttu-id="68236-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="68236-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68236-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="68236-126">-JobScheduleId</span></span>
<span data-ttu-id="68236-127">Specifica l'ID di un processo programmato ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68236-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="68236-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68236-128">-ResourceGroupName</span></span>
<span data-ttu-id="68236-129">Specifica il nome di un gruppo di risorse per il manuali operativi programmato che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="68236-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="68236-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="68236-130">-RunbookName</span></span>
<span data-ttu-id="68236-131">Specifica il nome di un Runbook per cui questo cmdlet ottiene il manuali operativi programmato.</span><span class="sxs-lookup"><span data-stu-id="68236-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68236-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="68236-132">-ScheduleName</span></span>
<span data-ttu-id="68236-133">Specifica il nome di una pianificazione per cui questo cmdlet ottiene il manuali operativi programmato.</span><span class="sxs-lookup"><span data-stu-id="68236-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68236-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68236-134">CommonParameters</span></span>
<span data-ttu-id="68236-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68236-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68236-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68236-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68236-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68236-137">INPUTS</span></span>

### <span data-ttu-id="68236-138">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="68236-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="68236-139">System. String</span><span class="sxs-lookup"><span data-stu-id="68236-139">System.String</span></span>

## <span data-ttu-id="68236-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68236-140">OUTPUTS</span></span>

### <span data-ttu-id="68236-141">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="68236-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="68236-142">Note</span><span class="sxs-lookup"><span data-stu-id="68236-142">NOTES</span></span>

## <span data-ttu-id="68236-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68236-143">RELATED LINKS</span></span>

[<span data-ttu-id="68236-144">Registro-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="68236-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="68236-145">Annullamento della registrazione-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="68236-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


