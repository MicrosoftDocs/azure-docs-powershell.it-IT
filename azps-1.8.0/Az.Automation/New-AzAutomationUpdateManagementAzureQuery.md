---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 01f0902be7d31762586100cb63098707071bab3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685017"
---
# <span data-ttu-id="7d968-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="7d968-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="7d968-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d968-102">SYNOPSIS</span></span>
<span data-ttu-id="7d968-103">Crea l'oggetto di query Azure Automation Software Update Configuration di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d968-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="7d968-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d968-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Locaton <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d968-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d968-105">DESCRIPTION</span></span>
<span data-ttu-id="7d968-106">Crea un oggetto query di configurazione dell'aggiornamento software Azure che verrà usato per creare una configurazione di aggiornamento software che verrà eseguita in una programmazione per aggiornare un elenco di un elenco risolto in modo dinamico di macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d968-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="7d968-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d968-107">EXAMPLES</span></span>

### <span data-ttu-id="7d968-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d968-108">Example 1</span></span>
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
                                       -Locaton $query1Location `
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

## <span data-ttu-id="7d968-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d968-109">PARAMETERS</span></span>

### <span data-ttu-id="7d968-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7d968-110">-AutomationAccountName</span></span>
<span data-ttu-id="7d968-111">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="7d968-111">The automation account name.</span></span>

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

### <span data-ttu-id="7d968-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d968-112">-DefaultProfile</span></span>
<span data-ttu-id="7d968-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d968-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d968-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="7d968-114">-FilterOperator</span></span>
<span data-ttu-id="7d968-115">Operatore di filtro tag.</span><span class="sxs-lookup"><span data-stu-id="7d968-115">Tag filter operator.</span></span>

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

### <span data-ttu-id="7d968-116">-Locaton</span><span class="sxs-lookup"><span data-stu-id="7d968-116">-Locaton</span></span>
<span data-ttu-id="7d968-117">Elenco di posizioni per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d968-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7d968-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d968-118">-ResourceGroupName</span></span>
<span data-ttu-id="7d968-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d968-119">The resource group name.</span></span>

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

### <span data-ttu-id="7d968-120">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7d968-120">-Scope</span></span>
<span data-ttu-id="7d968-121">ID risorsa per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d968-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7d968-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d968-122">-Tag</span></span>
<span data-ttu-id="7d968-123">Tag per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d968-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7d968-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d968-124">CommonParameters</span></span>
<span data-ttu-id="7d968-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d968-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7d968-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d968-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d968-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d968-127">INPUTS</span></span>

### <span data-ttu-id="7d968-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="7d968-128">System.String[]</span></span>

### <span data-ttu-id="7d968-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7d968-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7d968-130">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. TagOperators</span><span class="sxs-lookup"><span data-stu-id="7d968-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="7d968-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7d968-131">System.String</span></span>

## <span data-ttu-id="7d968-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d968-132">OUTPUTS</span></span>

### <span data-ttu-id="7d968-133">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="7d968-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="7d968-134">Note</span><span class="sxs-lookup"><span data-stu-id="7d968-134">NOTES</span></span>

## <span data-ttu-id="7d968-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d968-135">RELATED LINKS</span></span>
