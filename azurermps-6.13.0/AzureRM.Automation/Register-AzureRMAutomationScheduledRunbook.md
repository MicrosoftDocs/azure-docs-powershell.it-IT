---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: deb6611fedbb1f88b9668b4750e096056ea8b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686269"
---
# <span data-ttu-id="179ae-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="179ae-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="179ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="179ae-102">SYNOPSIS</span></span>
<span data-ttu-id="179ae-103">Associa un Runbook a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="179ae-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="179ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="179ae-104">SYNTAX</span></span>

### <span data-ttu-id="179ae-105">ByRunbookName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="179ae-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="179ae-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="179ae-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="179ae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="179ae-107">DESCRIPTION</span></span>
<span data-ttu-id="179ae-108">Il cmdlet **Register-AzureRmAutomationScheduledRunbook** associa un Runbook di automazione Azure a una programmazione.</span><span class="sxs-lookup"><span data-stu-id="179ae-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="179ae-109">Runbook inizia in base alla pianificazione specificata usando il parametro *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="179ae-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="179ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="179ae-110">EXAMPLES</span></span>

### <span data-ttu-id="179ae-111">Esempio 1: associare un Runbook a una pianificazione</span><span class="sxs-lookup"><span data-stu-id="179ae-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="179ae-112">Questo comando associa il Runbook denominato Runbk01 con la pianificazione denominata Sched01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="179ae-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="179ae-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="179ae-113">PARAMETERS</span></span>

### <span data-ttu-id="179ae-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="179ae-114">-AutomationAccountName</span></span>
<span data-ttu-id="179ae-115">Specifica un account di automazione per il Runbook in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="179ae-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="179ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179ae-116">-DefaultProfile</span></span>
<span data-ttu-id="179ae-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="179ae-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="179ae-118">-Parameters</span><span class="sxs-lookup"><span data-stu-id="179ae-118">-Parameters</span></span>
<span data-ttu-id="179ae-119">Specifica una tabella hash di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="179ae-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="179ae-120">Le chiavi sono nomi di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="179ae-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="179ae-121">I valori sono valori di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="179ae-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="179ae-122">Quando Runbook inizia in risposta alla pianificazione associata, questi parametri vengono passati a Runbook.</span><span class="sxs-lookup"><span data-stu-id="179ae-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="179ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="179ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="179ae-124">Specifica il nome di un gruppo di risorse per il Runbook programmato.</span><span class="sxs-lookup"><span data-stu-id="179ae-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="179ae-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="179ae-125">-RunbookName</span></span>
<span data-ttu-id="179ae-126">Specifica il nome del Runbook che questo cmdlet associa a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="179ae-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="179ae-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="179ae-127">-RunOn</span></span>
<span data-ttu-id="179ae-128">Nome del gruppo di lavoro Runbook ibrido.</span><span class="sxs-lookup"><span data-stu-id="179ae-128">The name of the hybrid runbook worker group.</span></span>

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

### <span data-ttu-id="179ae-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="179ae-129">-ScheduleName</span></span>
<span data-ttu-id="179ae-130">Specifica il nome della pianificazione a cui questo cmdlet associa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="179ae-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="179ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179ae-131">CommonParameters</span></span>
<span data-ttu-id="179ae-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="179ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179ae-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="179ae-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179ae-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="179ae-134">INPUTS</span></span>

### <span data-ttu-id="179ae-135">System. String</span><span class="sxs-lookup"><span data-stu-id="179ae-135">System.String</span></span>

## <span data-ttu-id="179ae-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="179ae-136">OUTPUTS</span></span>

### <span data-ttu-id="179ae-137">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="179ae-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="179ae-138">Note</span><span class="sxs-lookup"><span data-stu-id="179ae-138">NOTES</span></span>

## <span data-ttu-id="179ae-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="179ae-139">RELATED LINKS</span></span>

[<span data-ttu-id="179ae-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="179ae-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="179ae-141">Annullamento della registrazione-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="179ae-141">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


