---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191683"
---
# <span data-ttu-id="1d42b-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d42b-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="1d42b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d42b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d42b-103">Ottiene i metadati per le configurazioni dei nodi DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="1d42b-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="1d42b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d42b-104">SYNTAX</span></span>

### <span data-ttu-id="1d42b-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d42b-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d42b-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1d42b-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d42b-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1d42b-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d42b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d42b-108">DESCRIPTION</span></span>
<span data-ttu-id="1d42b-109">Il cmdlet **Get-AzAutomationDscNodeConfiguration** ottiene i metadati per le configurazioni di nodi DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1d42b-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="1d42b-110">Automation archivia la configurazione del nodo DSC come documento di configurazione MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="1d42b-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="1d42b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d42b-111">EXAMPLES</span></span>

### <span data-ttu-id="1d42b-112">Esempio 1: ottenere tutte le configurazioni dei nodi DSC</span><span class="sxs-lookup"><span data-stu-id="1d42b-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1d42b-113">Questo comando consente di ottenere metadati per tutte le configurazioni di nodi DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1d42b-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1d42b-114">Esempio 2: ottenere tutte le configurazioni di nodi DSC per una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="1d42b-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="1d42b-115">Questo comando consente di ottenere metadati per tutte le configurazioni di nodi DSC nell'account di automazione denominato Contoso17 che viene generata la configurazione DSC denominata ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1d42b-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="1d42b-116">Esempio 3: ottenere una configurazione del nodo DSC per nome</span><span class="sxs-lookup"><span data-stu-id="1d42b-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="1d42b-117">Questo comando consente di ottenere metadati per una configurazione di nodi DSC con il nome ContosoConfiguration. webserver nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1d42b-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1d42b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d42b-118">PARAMETERS</span></span>

### <span data-ttu-id="1d42b-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d42b-119">-AutomationAccountName</span></span>
<span data-ttu-id="1d42b-120">Specifica il nome di un account di automazione che contiene le configurazioni dei nodi DSC per cui questo cmdlet ottiene i metadati.</span><span class="sxs-lookup"><span data-stu-id="1d42b-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="1d42b-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1d42b-121">-ConfigurationName</span></span>
<span data-ttu-id="1d42b-122">Specifica il nome della configurazione DSC per cui questo cmdlet ottiene i metadati di configurazione dei nodi.</span><span class="sxs-lookup"><span data-stu-id="1d42b-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="1d42b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d42b-123">-DefaultProfile</span></span>
<span data-ttu-id="1d42b-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1d42b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d42b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d42b-125">-Name</span></span>
<span data-ttu-id="1d42b-126">Specifica il nome della configurazione del nodo DSC per cui questo cmdlet ottiene i metadati.</span><span class="sxs-lookup"><span data-stu-id="1d42b-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="1d42b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d42b-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d42b-128">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d42b-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1d42b-129">Questo cmdlet consente di ottenere metadati per le configurazioni dei nodi DSC nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1d42b-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d42b-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="1d42b-130">-RollupStatus</span></span>
<span data-ttu-id="1d42b-131">Specifica lo stato di rollup delle configurazioni dei nodi DSC ottenute dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d42b-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="1d42b-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1d42b-132">Valid values are:</span></span> 
- <span data-ttu-id="1d42b-133">Male</span><span class="sxs-lookup"><span data-stu-id="1d42b-133">Bad</span></span> 
- <span data-ttu-id="1d42b-134">Buona</span><span class="sxs-lookup"><span data-stu-id="1d42b-134">Good</span></span>

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

### <span data-ttu-id="1d42b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d42b-135">CommonParameters</span></span>
<span data-ttu-id="1d42b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d42b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d42b-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d42b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d42b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d42b-138">INPUTS</span></span>

### <span data-ttu-id="1d42b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1d42b-139">System.String</span></span>

## <span data-ttu-id="1d42b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d42b-140">OUTPUTS</span></span>

### <span data-ttu-id="1d42b-141">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="1d42b-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="1d42b-142">Note</span><span class="sxs-lookup"><span data-stu-id="1d42b-142">NOTES</span></span>

## <span data-ttu-id="1d42b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d42b-143">RELATED LINKS</span></span>

[<span data-ttu-id="1d42b-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d42b-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


