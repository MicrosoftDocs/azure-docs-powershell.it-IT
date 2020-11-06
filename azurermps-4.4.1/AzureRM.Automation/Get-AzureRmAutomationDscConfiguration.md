---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 4ac549e53054d0650c0e64e45c662c6b184067b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518423"
---
# <span data-ttu-id="f39b9-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f39b9-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="f39b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f39b9-102">SYNOPSIS</span></span>
<span data-ttu-id="f39b9-103">Ottiene le configurazioni DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="f39b9-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f39b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f39b9-104">SYNTAX</span></span>

### <span data-ttu-id="f39b9-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f39b9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f39b9-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f39b9-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f39b9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f39b9-107">DESCRIPTION</span></span>
<span data-ttu-id="f39b9-108">Il cmdlet **Get-AzureRmAutomationDscConfiguration** ottiene le configurazioni DSC (APS desired state Configuration) di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f39b9-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="f39b9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f39b9-109">EXAMPLES</span></span>

### <span data-ttu-id="f39b9-110">Esempio 1: ottenere tutte le configurazioni DSC</span><span class="sxs-lookup"><span data-stu-id="f39b9-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f39b9-111">Questo comando consente di ottenere metadati per tutte le configurazioni DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f39b9-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f39b9-112">Esempio 2: ottenere una configurazione DSC per nome</span><span class="sxs-lookup"><span data-stu-id="f39b9-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="f39b9-113">Questo comando consente di ottenere metadati per una configurazione DSC denominata configurazione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f39b9-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f39b9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f39b9-114">PARAMETERS</span></span>

### <span data-ttu-id="f39b9-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f39b9-115">-AutomationAccountName</span></span>
<span data-ttu-id="f39b9-116">Specifica il nome dell'account di automazione che contiene le configurazioni DSC ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f39b9-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f39b9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f39b9-117">-Name</span></span>
<span data-ttu-id="f39b9-118">Specifica il nome della configurazione DSC ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f39b9-118">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f39b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="f39b9-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le configurazioni DSC.</span><span class="sxs-lookup"><span data-stu-id="f39b9-120">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="f39b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39b9-121">-DefaultProfile</span></span>
<span data-ttu-id="f39b9-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f39b9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f39b9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39b9-123">CommonParameters</span></span>
<span data-ttu-id="f39b9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39b9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39b9-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39b9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39b9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f39b9-126">INPUTS</span></span>

## <span data-ttu-id="f39b9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f39b9-127">OUTPUTS</span></span>

### <span data-ttu-id="f39b9-128">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f39b9-128">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="f39b9-129">Note</span><span class="sxs-lookup"><span data-stu-id="f39b9-129">NOTES</span></span>

## <span data-ttu-id="f39b9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f39b9-130">RELATED LINKS</span></span>

[<span data-ttu-id="f39b9-131">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f39b9-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="f39b9-132">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f39b9-132">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


