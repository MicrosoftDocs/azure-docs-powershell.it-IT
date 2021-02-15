---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195263"
---
# <span data-ttu-id="e294d-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e294d-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="e294d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e294d-102">SYNOPSIS</span></span>
<span data-ttu-id="e294d-103">Ottiene un elenco delle configurazioni di aggiornamento software di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e294d-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="e294d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e294d-104">SYNTAX</span></span>

### <span data-ttu-id="e294d-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e294d-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e294d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e294d-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e294d-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="e294d-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e294d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e294d-108">DESCRIPTION</span></span>
<span data-ttu-id="e294d-109">La Get-AzAutomationSoftwareUpdateConfiguration restituisce un elenco di configurazioni di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="e294d-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="e294d-110">Per ottenere una configurazione di aggiornamento software specifica, specificare il parametro del nome.</span><span class="sxs-lookup"><span data-stu-id="e294d-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="e294d-111">È anche possibile elencare le configurazioni di aggiornamento software per una macchina virtuale di Azure specifica specificando l'ID risorsa azure per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e294d-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="e294d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e294d-112">EXAMPLES</span></span>

### <span data-ttu-id="e294d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e294d-113">Example 1</span></span>
<span data-ttu-id="e294d-114">Ottenere una configurazione dell'aggiornamento software di automazione di Azure in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e294d-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="e294d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e294d-115">PARAMETERS</span></span>

### <span data-ttu-id="e294d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e294d-116">-AutomationAccountName</span></span>
<span data-ttu-id="e294d-117">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e294d-117">The automation account name.</span></span>

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

### <span data-ttu-id="e294d-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="e294d-118">-AzureVMResourceId</span></span>
<span data-ttu-id="e294d-119">ID risorsa Azure della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e294d-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e294d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e294d-120">-DefaultProfile</span></span>
<span data-ttu-id="e294d-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e294d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e294d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e294d-122">-Name</span></span>
<span data-ttu-id="e294d-123">Nome della configurazione di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="e294d-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e294d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e294d-124">-ResourceGroupName</span></span>
<span data-ttu-id="e294d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e294d-125">The resource group name.</span></span>

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

### <span data-ttu-id="e294d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e294d-126">CommonParameters</span></span>
<span data-ttu-id="e294d-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e294d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e294d-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e294d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e294d-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="e294d-129">INPUTS</span></span>

### <span data-ttu-id="e294d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e294d-130">System.String</span></span>

## <span data-ttu-id="e294d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e294d-131">OUTPUTS</span></span>

### <span data-ttu-id="e294d-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e294d-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="e294d-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="e294d-133">NOTES</span></span>

## <span data-ttu-id="e294d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e294d-134">RELATED LINKS</span></span>
