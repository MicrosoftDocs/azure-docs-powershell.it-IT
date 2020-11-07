---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: 9d4efbccffeae2654b5be6d6db8635e588fd87f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685090"
---
# <span data-ttu-id="7a7ec-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7a7ec-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="7a7ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7ec-103">Ottiene i nodi DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="7a7ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a7ec-104">SYNTAX</span></span>

### <span data-ttu-id="7a7ec-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a7ec-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a7ec-106">ById</span><span class="sxs-lookup"><span data-stu-id="7a7ec-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a7ec-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7a7ec-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a7ec-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a7ec-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a7ec-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a7ec-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7ec-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a7ec-110">DESCRIPTION</span></span>
<span data-ttu-id="7a7ec-111">Il cmdlet **Get-AzAutomationDscNode** ottiene i nodi di configurazione di stato (DSC) APS di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="7a7ec-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a7ec-112">EXAMPLES</span></span>

### <span data-ttu-id="7a7ec-113">Esempio 1: ottenere tutti i nodi DSC</span><span class="sxs-lookup"><span data-stu-id="7a7ec-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7a7ec-114">Questo comando consente di ottenere metadati per tutti i nodi DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7a7ec-115">Esempio 2: ottenere tutti i nodi DSC per una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="7a7ec-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="7a7ec-116">Questo comando consente di ottenere metadati per tutti i nodi DSC nell'account di automazione denominato Contoso17 mappati a una configurazione di nodi DSC generata da ContosoConfiguration di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="7a7ec-117">Esempio 3: ottenere un nodo DSC in base all'ID</span><span class="sxs-lookup"><span data-stu-id="7a7ec-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="7a7ec-118">Questo comando consente di ottenere metadati in un nodo DSC con l'ID specificato nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7a7ec-119">Esempio 4: ottenere un nodo DSC per nome</span><span class="sxs-lookup"><span data-stu-id="7a7ec-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="7a7ec-120">Questo comando consente di ottenere metadati in un nodo DSC con il nome Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7a7ec-121">Esempio 5: ottenere tutti i nodi DSC mappati a una configurazione di nodi DSC</span><span class="sxs-lookup"><span data-stu-id="7a7ec-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="7a7ec-122">Questo comando consente di ottenere metadati in tutti i nodi DSC nell'account di automazione denominato Contoso17 mappati a una configurazione di nodi DSC denominata ContosoConfiguration. webserver.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="7a7ec-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a7ec-123">PARAMETERS</span></span>

### <span data-ttu-id="7a7ec-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a7ec-124">-AutomationAccountName</span></span>
<span data-ttu-id="7a7ec-125">Specifica il nome dell'account di automazione che contiene i nodi DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7a7ec-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7a7ec-126">-ConfigurationName</span></span>
<span data-ttu-id="7a7ec-127">Specifica il nome di una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="7a7ec-128">Questo cmdlet ottiene i nodi DSC che corrispondono alle configurazioni di nodi generate dalla configurazione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7ec-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7ec-129">-DefaultProfile</span></span>
<span data-ttu-id="7a7ec-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7a7ec-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a7ec-131">-ID</span><span class="sxs-lookup"><span data-stu-id="7a7ec-131">-Id</span></span>
<span data-ttu-id="7a7ec-132">Specifica l'ID univoco del nodo DSC ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7ec-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a7ec-133">-Name</span></span>
<span data-ttu-id="7a7ec-134">Specifica il nome di un nodo DSC che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7ec-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7a7ec-135">-NodeConfigurationName</span></span>
<span data-ttu-id="7a7ec-136">Specifica il nome di una configurazione di nodo ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7ec-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7ec-137">-ResourceGroupName</span></span>
<span data-ttu-id="7a7ec-138">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene i nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="7a7ec-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="7a7ec-139">-Status</span></span>
<span data-ttu-id="7a7ec-140">Specifica lo stato dei nodi DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="7a7ec-141">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7a7ec-141">Valid values are:</span></span> 
- <span data-ttu-id="7a7ec-142">Conformi</span><span class="sxs-lookup"><span data-stu-id="7a7ec-142">Compliant</span></span> 
- <span data-ttu-id="7a7ec-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="7a7ec-143">NotCompliant</span></span>
- <span data-ttu-id="7a7ec-144">Fallito</span><span class="sxs-lookup"><span data-stu-id="7a7ec-144">Failed</span></span>
- <span data-ttu-id="7a7ec-145">In sospeso</span><span class="sxs-lookup"><span data-stu-id="7a7ec-145">Pending</span></span> 
- <span data-ttu-id="7a7ec-146">Ricevuto</span><span class="sxs-lookup"><span data-stu-id="7a7ec-146">Received</span></span>
- <span data-ttu-id="7a7ec-147">Risponde</span><span class="sxs-lookup"><span data-stu-id="7a7ec-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7ec-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7ec-148">CommonParameters</span></span>
<span data-ttu-id="7a7ec-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7ec-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7ec-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7ec-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a7ec-151">INPUTS</span></span>

### <span data-ttu-id="7a7ec-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7a7ec-152">System.Guid</span></span>

### <span data-ttu-id="7a7ec-153">System. String</span><span class="sxs-lookup"><span data-stu-id="7a7ec-153">System.String</span></span>

## <span data-ttu-id="7a7ec-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a7ec-154">OUTPUTS</span></span>

### <span data-ttu-id="7a7ec-155">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="7a7ec-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="7a7ec-156">Note</span><span class="sxs-lookup"><span data-stu-id="7a7ec-156">NOTES</span></span>

## <span data-ttu-id="7a7ec-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a7ec-157">RELATED LINKS</span></span>

[<span data-ttu-id="7a7ec-158">Registro-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7a7ec-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="7a7ec-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7a7ec-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="7a7ec-160">Annullamento della registrazione-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7a7ec-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)

