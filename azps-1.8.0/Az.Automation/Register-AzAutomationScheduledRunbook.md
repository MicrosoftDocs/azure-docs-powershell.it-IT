---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: df6fc949fe1aa105a84ede2329c71feb4b27a449
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685008"
---
# <span data-ttu-id="4fb14-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4fb14-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="4fb14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fb14-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb14-103">Associa un Runbook a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4fb14-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="4fb14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fb14-104">SYNTAX</span></span>

### <span data-ttu-id="4fb14-105">ByRunbookName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4fb14-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fb14-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="4fb14-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb14-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb14-107">DESCRIPTION</span></span>
<span data-ttu-id="4fb14-108">Il cmdlet **Register-AzAutomationScheduledRunbook** associa un Runbook di automazione Azure a una programmazione.</span><span class="sxs-lookup"><span data-stu-id="4fb14-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="4fb14-109">Runbook inizia in base alla pianificazione specificata usando il parametro *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="4fb14-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="4fb14-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fb14-110">EXAMPLES</span></span>

### <span data-ttu-id="4fb14-111">Esempio 1: associare un Runbook a una pianificazione</span><span class="sxs-lookup"><span data-stu-id="4fb14-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4fb14-112">Questo comando associa il Runbook denominato Runbk01 con la pianificazione denominata Sched01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4fb14-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4fb14-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fb14-113">PARAMETERS</span></span>

### <span data-ttu-id="4fb14-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4fb14-114">-AutomationAccountName</span></span>
<span data-ttu-id="4fb14-115">Specifica un account di automazione per il Runbook in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fb14-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4fb14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb14-116">-DefaultProfile</span></span>
<span data-ttu-id="4fb14-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4fb14-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fb14-118">-Parameters</span><span class="sxs-lookup"><span data-stu-id="4fb14-118">-Parameters</span></span>
<span data-ttu-id="4fb14-119">Specifica una tabella hash di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="4fb14-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="4fb14-120">Le chiavi sono nomi di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="4fb14-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="4fb14-121">I valori sono valori di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="4fb14-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="4fb14-122">Quando Runbook inizia in risposta alla pianificazione associata, questi parametri vengono passati a Runbook.</span><span class="sxs-lookup"><span data-stu-id="4fb14-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb14-123">-ResourceGroupName</span></span>
<span data-ttu-id="4fb14-124">Specifica il nome di un gruppo di risorse per il Runbook programmato.</span><span class="sxs-lookup"><span data-stu-id="4fb14-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="4fb14-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="4fb14-125">-RunbookName</span></span>
<span data-ttu-id="4fb14-126">Specifica il nome del Runbook che questo cmdlet associa a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4fb14-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="4fb14-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="4fb14-127">-RunOn</span></span>
<span data-ttu-id="4fb14-128">Nome del gruppo di lavoro Runbook ibrido.</span><span class="sxs-lookup"><span data-stu-id="4fb14-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb14-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="4fb14-129">-ScheduleName</span></span>
<span data-ttu-id="4fb14-130">Specifica il nome della pianificazione a cui questo cmdlet associa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="4fb14-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="4fb14-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb14-131">CommonParameters</span></span>
<span data-ttu-id="4fb14-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb14-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb14-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb14-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb14-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fb14-134">INPUTS</span></span>

### <span data-ttu-id="4fb14-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4fb14-135">System.String</span></span>

## <span data-ttu-id="4fb14-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fb14-136">OUTPUTS</span></span>

### <span data-ttu-id="4fb14-137">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb14-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="4fb14-138">Note</span><span class="sxs-lookup"><span data-stu-id="4fb14-138">NOTES</span></span>

## <span data-ttu-id="4fb14-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fb14-139">RELATED LINKS</span></span>

[<span data-ttu-id="4fb14-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4fb14-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="4fb14-141">Annullamento della registrazione-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4fb14-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


