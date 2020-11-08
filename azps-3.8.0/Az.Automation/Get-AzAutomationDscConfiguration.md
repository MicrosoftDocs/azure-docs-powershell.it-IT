---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020661"
---
# <span data-ttu-id="e2023-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2023-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="e2023-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2023-102">SYNOPSIS</span></span>
<span data-ttu-id="e2023-103">Ottiene le configurazioni DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="e2023-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="e2023-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2023-104">SYNTAX</span></span>

### <span data-ttu-id="e2023-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2023-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2023-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e2023-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2023-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2023-107">DESCRIPTION</span></span>
<span data-ttu-id="e2023-108">Il cmdlet **Get-AzAutomationDscConfiguration** ottiene le configurazioni DSC (APS desired state Configuration) di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e2023-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="e2023-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2023-109">EXAMPLES</span></span>

### <span data-ttu-id="e2023-110">Esempio 1: ottenere tutte le configurazioni DSC</span><span class="sxs-lookup"><span data-stu-id="e2023-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e2023-111">Questo comando consente di ottenere metadati per tutte le configurazioni DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e2023-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e2023-112">Esempio 2: ottenere una configurazione DSC per nome</span><span class="sxs-lookup"><span data-stu-id="e2023-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="e2023-113">Questo comando consente di ottenere metadati per una configurazione DSC denominata configurazione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e2023-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e2023-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2023-114">PARAMETERS</span></span>

### <span data-ttu-id="e2023-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e2023-115">-AutomationAccountName</span></span>
<span data-ttu-id="e2023-116">Specifica il nome dell'account di automazione che contiene le configurazioni DSC ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2023-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2023-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2023-117">-DefaultProfile</span></span>
<span data-ttu-id="e2023-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e2023-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2023-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2023-119">-Name</span></span>
<span data-ttu-id="e2023-120">Specifica il nome della configurazione DSC ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2023-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2023-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2023-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2023-122">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le configurazioni DSC.</span><span class="sxs-lookup"><span data-stu-id="e2023-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="e2023-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2023-123">CommonParameters</span></span>
<span data-ttu-id="e2023-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2023-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2023-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2023-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2023-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2023-126">INPUTS</span></span>

### <span data-ttu-id="e2023-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e2023-127">System.String</span></span>

## <span data-ttu-id="e2023-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2023-128">OUTPUTS</span></span>

### <span data-ttu-id="e2023-129">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2023-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="e2023-130">Note</span><span class="sxs-lookup"><span data-stu-id="e2023-130">NOTES</span></span>

## <span data-ttu-id="e2023-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2023-131">RELATED LINKS</span></span>

[<span data-ttu-id="e2023-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2023-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="e2023-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2023-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


