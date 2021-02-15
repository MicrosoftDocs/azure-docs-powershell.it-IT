---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182190"
---
# <span data-ttu-id="7b217-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b217-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="7b217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b217-102">SYNOPSIS</span></span>
<span data-ttu-id="7b217-103">Recupera le configurazioni DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="7b217-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="7b217-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b217-104">SYNTAX</span></span>

### <span data-ttu-id="7b217-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b217-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b217-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7b217-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b217-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b217-107">DESCRIPTION</span></span>
<span data-ttu-id="7b217-108">Il cmdlet **Get-AzAutomationDscConfiguration** recupera le configurazioni DSC (Desired State Configuration) di APS dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b217-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="7b217-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b217-109">EXAMPLES</span></span>

### <span data-ttu-id="7b217-110">Esempio 1: Ottenere tutte le configurazioni DSC</span><span class="sxs-lookup"><span data-stu-id="7b217-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7b217-111">Questo comando recupera i metadati per tutte le configurazioni DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7b217-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7b217-112">Esempio 2: Ottenere una configurazione DSC in base al nome</span><span class="sxs-lookup"><span data-stu-id="7b217-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="7b217-113">Questo comando recupera i metadati per una configurazione DSC denominata MyConfiguration nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7b217-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7b217-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b217-114">PARAMETERS</span></span>

### <span data-ttu-id="7b217-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7b217-115">-AutomationAccountName</span></span>
<span data-ttu-id="7b217-116">Specifica il nome dell'account di automazione che contiene le configurazioni DSC recuperate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b217-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7b217-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b217-117">-DefaultProfile</span></span>
<span data-ttu-id="7b217-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="7b217-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b217-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7b217-119">-Name</span></span>
<span data-ttu-id="7b217-120">Specifica il nome della configurazione DSC che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b217-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b217-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b217-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b217-122">Specifica il nome di un gruppo di risorse per cui il cmdlet ottiene configurazioni DSC.</span><span class="sxs-lookup"><span data-stu-id="7b217-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="7b217-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b217-123">CommonParameters</span></span>
<span data-ttu-id="7b217-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b217-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b217-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b217-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b217-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b217-126">INPUTS</span></span>

### <span data-ttu-id="7b217-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7b217-127">System.String</span></span>

## <span data-ttu-id="7b217-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b217-128">OUTPUTS</span></span>

### <span data-ttu-id="7b217-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b217-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="7b217-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b217-130">NOTES</span></span>

## <span data-ttu-id="7b217-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b217-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b217-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b217-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="7b217-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b217-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


