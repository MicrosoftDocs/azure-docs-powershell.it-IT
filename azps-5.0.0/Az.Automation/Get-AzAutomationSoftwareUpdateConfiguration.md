---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311605"
---
# <span data-ttu-id="5ba73-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ba73-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="5ba73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ba73-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba73-103">Ottiene un elenco delle configurazioni di aggiornamento del software di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba73-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="5ba73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ba73-104">SYNTAX</span></span>

### <span data-ttu-id="5ba73-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ba73-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ba73-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5ba73-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ba73-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="5ba73-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba73-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ba73-108">DESCRIPTION</span></span>
<span data-ttu-id="5ba73-109">La Get-AzAutomationSoftwareUpdateConfiguration restituisce un elenco di configurazioni di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="5ba73-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="5ba73-110">Per ottenere una configurazione di aggiornamento software specifica, specificare il parametro Name.</span><span class="sxs-lookup"><span data-stu-id="5ba73-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="5ba73-111">È anche possibile elencare le configurazioni di aggiornamento software destinate a specifiche macchine virtuali di Azure specificando l'ID delle risorse di Azure per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5ba73-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="5ba73-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ba73-112">EXAMPLES</span></span>

### <span data-ttu-id="5ba73-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ba73-113">Example 1</span></span>
<span data-ttu-id="5ba73-114">Ottenere una configurazione di aggiornamento software di automazione Azure per nome.</span><span class="sxs-lookup"><span data-stu-id="5ba73-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="5ba73-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ba73-115">PARAMETERS</span></span>

### <span data-ttu-id="5ba73-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5ba73-116">-AutomationAccountName</span></span>
<span data-ttu-id="5ba73-117">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="5ba73-117">The automation account name.</span></span>

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

### <span data-ttu-id="5ba73-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="5ba73-118">-AzureVMResourceId</span></span>
<span data-ttu-id="5ba73-119">ID risorsa Azure della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5ba73-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="5ba73-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba73-120">-DefaultProfile</span></span>
<span data-ttu-id="5ba73-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba73-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba73-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ba73-122">-Name</span></span>
<span data-ttu-id="5ba73-123">Nome della configurazione di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="5ba73-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="5ba73-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba73-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ba73-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ba73-125">The resource group name.</span></span>

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

### <span data-ttu-id="5ba73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba73-126">CommonParameters</span></span>
<span data-ttu-id="5ba73-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba73-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba73-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba73-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ba73-129">INPUTS</span></span>

### <span data-ttu-id="5ba73-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba73-130">System.String</span></span>

## <span data-ttu-id="5ba73-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ba73-131">OUTPUTS</span></span>

### <span data-ttu-id="5ba73-132">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ba73-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="5ba73-133">Note</span><span class="sxs-lookup"><span data-stu-id="5ba73-133">NOTES</span></span>

## <span data-ttu-id="5ba73-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ba73-134">RELATED LINKS</span></span>
