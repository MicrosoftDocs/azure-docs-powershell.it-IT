---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f4d17fa6cdcb64aab2ab373420891f686facfdf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520292"
---
# <span data-ttu-id="7c99d-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c99d-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="7c99d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c99d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c99d-103">Ottiene un elenco delle configurazioni di aggiornamento del software di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7c99d-103">Gets a list of azure automation software update configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c99d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c99d-104">SYNTAX</span></span>

### <span data-ttu-id="7c99d-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c99d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c99d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7c99d-106">ByName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c99d-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="7c99d-107">ByVMId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c99d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c99d-108">DESCRIPTION</span></span>
<span data-ttu-id="7c99d-109">La Get-AzureRmAutomationSoftwareUpdateConfiguration restituisce un elenco di configurazioni di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="7c99d-109">The Get-AzureRmAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="7c99d-110">Per ottenere una configurazione di aggiornamento software specifica, specificare il parametro Name.</span><span class="sxs-lookup"><span data-stu-id="7c99d-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="7c99d-111">È anche possibile elencare le configurazioni di aggiornamento software destinate a specifiche macchine virtuali di Azure specificando l'ID delle risorse di Azure per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c99d-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="7c99d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c99d-112">EXAMPLES</span></span>

### <span data-ttu-id="7c99d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c99d-113">Example 1</span></span>
<span data-ttu-id="7c99d-114">Ottenere una configurazione di aggiornamento software di automazione Azure per nome.</span><span class="sxs-lookup"><span data-stu-id="7c99d-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

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

## <span data-ttu-id="7c99d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c99d-115">PARAMETERS</span></span>

### <span data-ttu-id="7c99d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7c99d-116">-AutomationAccountName</span></span>
<span data-ttu-id="7c99d-117">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="7c99d-117">The automation account name.</span></span>

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

### <span data-ttu-id="7c99d-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="7c99d-118">-AzureVMResourceId</span></span>
<span data-ttu-id="7c99d-119">ID risorsa Azure della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c99d-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="7c99d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c99d-120">-DefaultProfile</span></span>
<span data-ttu-id="7c99d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c99d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c99d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c99d-122">-Name</span></span>
<span data-ttu-id="7c99d-123">Nome della configurazione di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="7c99d-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="7c99d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c99d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c99d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c99d-125">The resource group name.</span></span>

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

### <span data-ttu-id="7c99d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c99d-126">CommonParameters</span></span>
<span data-ttu-id="7c99d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c99d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c99d-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c99d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c99d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c99d-129">INPUTS</span></span>

### <span data-ttu-id="7c99d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7c99d-130">System.String</span></span>

## <span data-ttu-id="7c99d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c99d-131">OUTPUTS</span></span>

### <span data-ttu-id="7c99d-132">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c99d-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="7c99d-133">Note</span><span class="sxs-lookup"><span data-stu-id="7c99d-133">NOTES</span></span>

## <span data-ttu-id="7c99d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c99d-134">RELATED LINKS</span></span>
