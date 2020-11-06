---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: f5de98b4f64b4f9adb03493638cdf4e1e613e10f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517160"
---
# <span data-ttu-id="e986e-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e986e-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="e986e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e986e-102">SYNOPSIS</span></span>
<span data-ttu-id="e986e-103">Ottiene i metadati per le configurazioni dei nodi DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="e986e-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e986e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e986e-104">SYNTAX</span></span>

### <span data-ttu-id="e986e-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e986e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e986e-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e986e-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e986e-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e986e-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e986e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e986e-108">DESCRIPTION</span></span>
<span data-ttu-id="e986e-109">Il cmdlet **Get-AzureRmAutomationDscNodeConfiguration** ottiene i metadati per le configurazioni di nodi DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e986e-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="e986e-110">Automation archivia la configurazione del nodo DSC come documento di configurazione MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="e986e-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="e986e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e986e-111">EXAMPLES</span></span>

### <span data-ttu-id="e986e-112">Esempio 1: ottenere tutte le configurazioni dei nodi DSC</span><span class="sxs-lookup"><span data-stu-id="e986e-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e986e-113">Questo comando consente di ottenere metadati per tutte le configurazioni di nodi DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e986e-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e986e-114">Esempio 2: ottenere tutte le configurazioni di nodi DSC per una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="e986e-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="e986e-115">Questo comando consente di ottenere metadati per tutte le configurazioni di nodi DSC nell'account di automazione denominato Contoso17 che viene generata la configurazione DSC denominata ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e986e-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="e986e-116">Esempio 3: ottenere una configurazione del nodo DSC per nome</span><span class="sxs-lookup"><span data-stu-id="e986e-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="e986e-117">Questo comando consente di ottenere metadati per una configurazione di nodi DSC con il nome ContosoConfiguration. webserver nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e986e-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e986e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e986e-118">PARAMETERS</span></span>

### <span data-ttu-id="e986e-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e986e-119">-AutomationAccountName</span></span>
<span data-ttu-id="e986e-120">Specifica il nome di un account di automazione che contiene le configurazioni dei nodi DSC per cui questo cmdlet ottiene i metadati.</span><span class="sxs-lookup"><span data-stu-id="e986e-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="e986e-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e986e-121">-ConfigurationName</span></span>
<span data-ttu-id="e986e-122">Specifica il nome della configurazione DSC per cui questo cmdlet ottiene i metadati di configurazione dei nodi.</span><span class="sxs-lookup"><span data-stu-id="e986e-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e986e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e986e-123">-Name</span></span>
<span data-ttu-id="e986e-124">Specifica il nome della configurazione del nodo DSC per cui questo cmdlet ottiene i metadati.</span><span class="sxs-lookup"><span data-stu-id="e986e-124">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e986e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e986e-125">-ResourceGroupName</span></span>
<span data-ttu-id="e986e-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e986e-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e986e-127">Questo cmdlet consente di ottenere metadati per le configurazioni dei nodi DSC nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e986e-127">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e986e-128">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="e986e-128">-RollupStatus</span></span>
<span data-ttu-id="e986e-129">Specifica lo stato di rollup delle configurazioni dei nodi DSC ottenute dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e986e-129">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="e986e-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e986e-130">Valid values are:</span></span> 

- <span data-ttu-id="e986e-131">Male</span><span class="sxs-lookup"><span data-stu-id="e986e-131">Bad</span></span> 
- <span data-ttu-id="e986e-132">Buona</span><span class="sxs-lookup"><span data-stu-id="e986e-132">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e986e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e986e-133">-DefaultProfile</span></span>
<span data-ttu-id="e986e-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e986e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e986e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e986e-135">CommonParameters</span></span>
<span data-ttu-id="e986e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e986e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e986e-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e986e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e986e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e986e-138">INPUTS</span></span>

## <span data-ttu-id="e986e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e986e-139">OUTPUTS</span></span>

### <span data-ttu-id="e986e-140">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="e986e-140">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="e986e-141">Note</span><span class="sxs-lookup"><span data-stu-id="e986e-141">NOTES</span></span>

## <span data-ttu-id="e986e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e986e-142">RELATED LINKS</span></span>

[<span data-ttu-id="e986e-143">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e986e-143">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


