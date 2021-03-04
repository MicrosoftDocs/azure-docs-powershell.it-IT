---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 90534fa058da876a09456d421bfa59d9906d6055
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956493"
---
# <span data-ttu-id="e3c43-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="e3c43-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="e3c43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3c43-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c43-103">Crea un oggetto query di azure per la configurazione dell'aggiornamento software di azure.</span><span class="sxs-lookup"><span data-stu-id="e3c43-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="e3c43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3c43-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3c43-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3c43-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c43-106">Crea un oggetto query di azure per la configurazione degli aggiornamenti software che verrà usato per creare una configurazione di aggiornamento software che verrà eseguita in base a una pianificazione per aggiornare un elenco di macchine virtuali di Azure risolte dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="e3c43-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="e3c43-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3c43-107">EXAMPLES</span></span>

### <span data-ttu-id="e3c43-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3c43-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="e3c43-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3c43-109">PARAMETERS</span></span>

### <span data-ttu-id="e3c43-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e3c43-110">-AutomationAccountName</span></span>
<span data-ttu-id="e3c43-111">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e3c43-111">The automation account name.</span></span>

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

### <span data-ttu-id="e3c43-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c43-112">-DefaultProfile</span></span>
<span data-ttu-id="e3c43-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c43-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c43-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="e3c43-114">-FilterOperator</span></span>
<span data-ttu-id="e3c43-115">Operatore filtro tag.</span><span class="sxs-lookup"><span data-stu-id="e3c43-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="e3c43-116">-Location</span><span class="sxs-lookup"><span data-stu-id="e3c43-116">-Location</span></span>
<span data-ttu-id="e3c43-117">Elenco di posizioni per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c43-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="e3c43-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c43-118">-ResourceGroupName</span></span>
<span data-ttu-id="e3c43-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3c43-119">The resource group name.</span></span>

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

### <span data-ttu-id="e3c43-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="e3c43-120">-Scope</span></span>
<span data-ttu-id="e3c43-121">ID risorsa per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c43-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="e3c43-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3c43-122">-Tag</span></span>
<span data-ttu-id="e3c43-123">Tag per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c43-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="e3c43-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c43-124">CommonParameters</span></span>
<span data-ttu-id="e3c43-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c43-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e3c43-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c43-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c43-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3c43-127">INPUTS</span></span>

### <span data-ttu-id="e3c43-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e3c43-128">System.String[]</span></span>

### <span data-ttu-id="e3c43-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3c43-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e3c43-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span><span class="sxs-lookup"><span data-stu-id="e3c43-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="e3c43-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e3c43-131">System.String</span></span>

## <span data-ttu-id="e3c43-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3c43-132">OUTPUTS</span></span>

### <span data-ttu-id="e3c43-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="e3c43-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="e3c43-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3c43-134">NOTES</span></span>

## <span data-ttu-id="e3c43-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3c43-135">RELATED LINKS</span></span>
