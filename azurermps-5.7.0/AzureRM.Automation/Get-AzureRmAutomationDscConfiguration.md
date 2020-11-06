---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 3d6d3628ba15fa4b775f4c747a29645ec0628402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522078"
---
# <span data-ttu-id="88dc5-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="88dc5-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="88dc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="88dc5-103">Ottiene le configurazioni DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="88dc5-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88dc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88dc5-104">SYNTAX</span></span>

### <span data-ttu-id="88dc5-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88dc5-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88dc5-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="88dc5-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88dc5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88dc5-107">DESCRIPTION</span></span>
<span data-ttu-id="88dc5-108">Il cmdlet **Get-AzureRmAutomationDscConfiguration** ottiene le configurazioni DSC (APS desired state Configuration) di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="88dc5-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="88dc5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88dc5-109">EXAMPLES</span></span>

### <span data-ttu-id="88dc5-110">Esempio 1: ottenere tutte le configurazioni DSC</span><span class="sxs-lookup"><span data-stu-id="88dc5-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="88dc5-111">Questo comando consente di ottenere metadati per tutte le configurazioni DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="88dc5-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="88dc5-112">Esempio 2: ottenere una configurazione DSC per nome</span><span class="sxs-lookup"><span data-stu-id="88dc5-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="88dc5-113">Questo comando consente di ottenere metadati per una configurazione DSC denominata configurazione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="88dc5-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="88dc5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88dc5-114">PARAMETERS</span></span>

### <span data-ttu-id="88dc5-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="88dc5-115">-AutomationAccountName</span></span>
<span data-ttu-id="88dc5-116">Specifica il nome dell'account di automazione che contiene le configurazioni DSC ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88dc5-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="88dc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88dc5-117">-DefaultProfile</span></span>
<span data-ttu-id="88dc5-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="88dc5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88dc5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="88dc5-119">-Name</span></span>
<span data-ttu-id="88dc5-120">Specifica il nome della configurazione DSC ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88dc5-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88dc5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88dc5-121">-ResourceGroupName</span></span>
<span data-ttu-id="88dc5-122">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le configurazioni DSC.</span><span class="sxs-lookup"><span data-stu-id="88dc5-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="88dc5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dc5-123">CommonParameters</span></span>
<span data-ttu-id="88dc5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88dc5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dc5-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88dc5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dc5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88dc5-126">INPUTS</span></span>

### <span data-ttu-id="88dc5-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="88dc5-127">None</span></span>
<span data-ttu-id="88dc5-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="88dc5-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88dc5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88dc5-129">OUTPUTS</span></span>

### <span data-ttu-id="88dc5-130">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="88dc5-130">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="88dc5-131">Note</span><span class="sxs-lookup"><span data-stu-id="88dc5-131">NOTES</span></span>

## <span data-ttu-id="88dc5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88dc5-132">RELATED LINKS</span></span>

[<span data-ttu-id="88dc5-133">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="88dc5-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="88dc5-134">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="88dc5-134">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


