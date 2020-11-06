---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: fe8d7b4407aa5afc3454d80e4cf45c102d9006bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521999"
---
# <span data-ttu-id="8c6f7-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8c6f7-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="8c6f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6f7-103">Ottiene le manuali operativi di automazione e le pianificazioni associate.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c6f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c6f7-104">SYNTAX</span></span>

### <span data-ttu-id="8c6f7-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c6f7-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c6f7-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="8c6f7-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c6f7-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="8c6f7-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c6f7-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="8c6f7-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c6f7-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="8c6f7-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c6f7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c6f7-110">DESCRIPTION</span></span>
<span data-ttu-id="8c6f7-111">Il cmdlet **Get-AzureRmAutomationScheduledRunbook** ottiene uno o più manuali operativi di automazione Azure e pianificazioni associate.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="8c6f7-112">Per impostazione predefinita, questo cmdlet ottiene tutti i manuali operativi pianificati.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="8c6f7-113">Specificare il nome di una Runbook o di una pianificazione oppure entrambe per visualizzare le pianificazioni specifiche di Runbook.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="8c6f7-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c6f7-114">EXAMPLES</span></span>

### <span data-ttu-id="8c6f7-115">Esempio 1: ottenere tutte le manuali operativi pianificate</span><span class="sxs-lookup"><span data-stu-id="8c6f7-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8c6f7-116">Questo comando consente di ottenere tutte le manuali operativi pianificate nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="8c6f7-117">Esempio 2: ottenere tutte le pianificazioni associate a un Runbook</span><span class="sxs-lookup"><span data-stu-id="8c6f7-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="8c6f7-118">Questo comando consente di ottenere tutte le manuali operativi pianificate per Runbook Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="8c6f7-119">Esempio 3: ottenere tutti i manuali operativi associati a una pianificazione</span><span class="sxs-lookup"><span data-stu-id="8c6f7-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="8c6f7-120">Questo comando consente di ottenere tutte le manuali operativi pianificate per la pianificazione Schedule01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8c6f7-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c6f7-121">PARAMETERS</span></span>

### <span data-ttu-id="8c6f7-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8c6f7-122">-AutomationAccountName</span></span>
<span data-ttu-id="8c6f7-123">Specifica un account di automazione per il Runbook in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8c6f7-124">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="8c6f7-124">-JobScheduleId</span></span>
<span data-ttu-id="8c6f7-125">Specifica l'ID di un processo programmato ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-125">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c6f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="8c6f7-127">Specifica il nome di un gruppo di risorse per il manuali operativi programmato che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-127">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c6f7-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="8c6f7-128">-RunbookName</span></span>
<span data-ttu-id="8c6f7-129">Specifica il nome di un Runbook per cui questo cmdlet ottiene il manuali operativi programmato.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-129">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="8c6f7-130">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="8c6f7-130">-ScheduleName</span></span>
<span data-ttu-id="8c6f7-131">Specifica il nome di una pianificazione per cui questo cmdlet ottiene il manuali operativi programmato.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-131">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="8c6f7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6f7-132">-DefaultProfile</span></span>
<span data-ttu-id="8c6f7-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c6f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6f7-134">CommonParameters</span></span>
<span data-ttu-id="8c6f7-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6f7-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c6f7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6f7-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c6f7-137">INPUTS</span></span>

## <span data-ttu-id="8c6f7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c6f7-138">OUTPUTS</span></span>

### <span data-ttu-id="8c6f7-139">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="8c6f7-139">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="8c6f7-140">Note</span><span class="sxs-lookup"><span data-stu-id="8c6f7-140">NOTES</span></span>

## <span data-ttu-id="8c6f7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c6f7-141">RELATED LINKS</span></span>

[<span data-ttu-id="8c6f7-142">Registro-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8c6f7-142">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="8c6f7-143">Annullamento della registrazione-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8c6f7-143">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


