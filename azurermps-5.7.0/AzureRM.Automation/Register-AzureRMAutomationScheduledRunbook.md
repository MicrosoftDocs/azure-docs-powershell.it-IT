---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: ec89359453af2dd997aed6359914ac499a6a3f7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510172"
---
# <span data-ttu-id="83d8c-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="83d8c-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="83d8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="83d8c-103">Associa un Runbook a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="83d8c-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83d8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83d8c-104">SYNTAX</span></span>

### <span data-ttu-id="83d8c-105">ByRunbookName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83d8c-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83d8c-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="83d8c-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83d8c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83d8c-107">DESCRIPTION</span></span>
<span data-ttu-id="83d8c-108">Il cmdlet **Register-AzureRmAutomationScheduledRunbook** associa un Runbook di automazione Azure a una programmazione.</span><span class="sxs-lookup"><span data-stu-id="83d8c-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="83d8c-109">Runbook inizia in base alla pianificazione specificata usando il parametro *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="83d8c-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="83d8c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83d8c-110">EXAMPLES</span></span>

### <span data-ttu-id="83d8c-111">Esempio 1: associare un Runbook a una pianificazione</span><span class="sxs-lookup"><span data-stu-id="83d8c-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="83d8c-112">Questo comando associa il Runbook denominato Runbk01 con la pianificazione denominata Sched01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="83d8c-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="83d8c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83d8c-113">PARAMETERS</span></span>

### <span data-ttu-id="83d8c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="83d8c-114">-AutomationAccountName</span></span>
<span data-ttu-id="83d8c-115">Specifica un account di automazione per il Runbook in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83d8c-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d8c-116">-DefaultProfile</span></span>
<span data-ttu-id="83d8c-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="83d8c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d8c-118">-Parameters</span><span class="sxs-lookup"><span data-stu-id="83d8c-118">-Parameters</span></span>
<span data-ttu-id="83d8c-119">Specifica una tabella hash di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="83d8c-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="83d8c-120">Le chiavi sono nomi di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="83d8c-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="83d8c-121">I valori sono valori di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="83d8c-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="83d8c-122">Quando Runbook inizia in risposta alla pianificazione associata, questi parametri vengono passati a Runbook.</span><span class="sxs-lookup"><span data-stu-id="83d8c-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="83d8c-124">Specifica il nome di un gruppo di risorse per il Runbook programmato.</span><span class="sxs-lookup"><span data-stu-id="83d8c-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d8c-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="83d8c-125">-RunbookName</span></span>
<span data-ttu-id="83d8c-126">Specifica il nome del Runbook che questo cmdlet associa a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="83d8c-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d8c-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="83d8c-127">-RunOn</span></span>
<span data-ttu-id="83d8c-128">Nome del gruppo di lavoro Runbook ibrido.</span><span class="sxs-lookup"><span data-stu-id="83d8c-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d8c-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="83d8c-129">-ScheduleName</span></span>
<span data-ttu-id="83d8c-130">Specifica il nome della pianificazione a cui questo cmdlet associa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="83d8c-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d8c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d8c-131">CommonParameters</span></span>
<span data-ttu-id="83d8c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d8c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d8c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d8c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d8c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83d8c-134">INPUTS</span></span>

### <span data-ttu-id="83d8c-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="83d8c-135">None</span></span>
<span data-ttu-id="83d8c-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="83d8c-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83d8c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83d8c-137">OUTPUTS</span></span>

### <span data-ttu-id="83d8c-138">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="83d8c-138">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="83d8c-139">Note</span><span class="sxs-lookup"><span data-stu-id="83d8c-139">NOTES</span></span>

## <span data-ttu-id="83d8c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83d8c-140">RELATED LINKS</span></span>

[<span data-ttu-id="83d8c-141">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="83d8c-141">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="83d8c-142">Annullamento della registrazione-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="83d8c-142">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


