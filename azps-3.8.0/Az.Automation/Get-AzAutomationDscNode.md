---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: f1328b71564b0fd839d3481a87b23a2a8b24ab55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020662"
---
# <span data-ttu-id="542d2-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="542d2-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="542d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="542d2-102">SYNOPSIS</span></span>
<span data-ttu-id="542d2-103">Ottiene i nodi DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="542d2-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="542d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="542d2-104">SYNTAX</span></span>

### <span data-ttu-id="542d2-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="542d2-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542d2-106">ById</span><span class="sxs-lookup"><span data-stu-id="542d2-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542d2-107">ByName</span><span class="sxs-lookup"><span data-stu-id="542d2-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542d2-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="542d2-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542d2-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="542d2-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="542d2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="542d2-110">DESCRIPTION</span></span>
<span data-ttu-id="542d2-111">Il cmdlet **Get-AzAutomationDscNode** ottiene i nodi di configurazione di stato (DSC) APS di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="542d2-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="542d2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="542d2-112">EXAMPLES</span></span>

### <span data-ttu-id="542d2-113">Esempio 1: ottenere tutti i nodi DSC</span><span class="sxs-lookup"><span data-stu-id="542d2-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="542d2-114">Questo comando consente di ottenere metadati per tutti i nodi DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="542d2-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="542d2-115">Esempio 2: ottenere tutti i nodi DSC per una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="542d2-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="542d2-116">Questo comando consente di ottenere metadati per tutti i nodi DSC nell'account di automazione denominato Contoso17 mappati a una configurazione di nodi DSC generata da ContosoConfiguration di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="542d2-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="542d2-117">Esempio 3: ottenere un nodo DSC in base all'ID</span><span class="sxs-lookup"><span data-stu-id="542d2-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="542d2-118">Questo comando consente di ottenere metadati in un nodo DSC con l'ID specificato nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="542d2-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="542d2-119">Esempio 4: ottenere un nodo DSC per nome</span><span class="sxs-lookup"><span data-stu-id="542d2-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="542d2-120">Questo comando consente di ottenere metadati in un nodo DSC con il nome Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="542d2-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="542d2-121">Esempio 5: ottenere tutti i nodi DSC mappati a una configurazione di nodi DSC</span><span class="sxs-lookup"><span data-stu-id="542d2-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="542d2-122">Questo comando consente di ottenere metadati in tutti i nodi DSC nell'account di automazione denominato Contoso17 mappati a una configurazione di nodi DSC denominata ContosoConfiguration. webserver.</span><span class="sxs-lookup"><span data-stu-id="542d2-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="542d2-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="542d2-123">PARAMETERS</span></span>

### <span data-ttu-id="542d2-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="542d2-124">-AutomationAccountName</span></span>
<span data-ttu-id="542d2-125">Specifica il nome dell'account di automazione che contiene i nodi DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="542d2-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="542d2-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="542d2-126">-ConfigurationName</span></span>
<span data-ttu-id="542d2-127">Specifica il nome di una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="542d2-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="542d2-128">Questo cmdlet ottiene i nodi DSC che corrispondono alle configurazioni di nodi generate dalla configurazione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="542d2-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

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

### <span data-ttu-id="542d2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542d2-129">-DefaultProfile</span></span>
<span data-ttu-id="542d2-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="542d2-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="542d2-131">-ID</span><span class="sxs-lookup"><span data-stu-id="542d2-131">-Id</span></span>
<span data-ttu-id="542d2-132">Specifica l'ID univoco del nodo DSC ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="542d2-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="542d2-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="542d2-133">-Name</span></span>
<span data-ttu-id="542d2-134">Specifica il nome di un nodo DSC che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="542d2-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="542d2-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="542d2-135">-NodeConfigurationName</span></span>
<span data-ttu-id="542d2-136">Specifica il nome di una configurazione di nodo ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="542d2-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="542d2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="542d2-137">-ResourceGroupName</span></span>
<span data-ttu-id="542d2-138">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene i nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="542d2-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="542d2-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="542d2-139">-Status</span></span>
<span data-ttu-id="542d2-140">Specifica lo stato dei nodi DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="542d2-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="542d2-141">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="542d2-141">Valid values are:</span></span> 
- <span data-ttu-id="542d2-142">Conformi</span><span class="sxs-lookup"><span data-stu-id="542d2-142">Compliant</span></span> 
- <span data-ttu-id="542d2-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="542d2-143">NotCompliant</span></span>
- <span data-ttu-id="542d2-144">Fallito</span><span class="sxs-lookup"><span data-stu-id="542d2-144">Failed</span></span>
- <span data-ttu-id="542d2-145">In sospeso</span><span class="sxs-lookup"><span data-stu-id="542d2-145">Pending</span></span> 
- <span data-ttu-id="542d2-146">Ricevuto</span><span class="sxs-lookup"><span data-stu-id="542d2-146">Received</span></span>
- <span data-ttu-id="542d2-147">Risponde</span><span class="sxs-lookup"><span data-stu-id="542d2-147">Unresponsive</span></span>

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

### <span data-ttu-id="542d2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542d2-148">CommonParameters</span></span>
<span data-ttu-id="542d2-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542d2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542d2-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542d2-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542d2-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="542d2-151">INPUTS</span></span>

### <span data-ttu-id="542d2-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="542d2-152">System.Guid</span></span>

### <span data-ttu-id="542d2-153">System. String</span><span class="sxs-lookup"><span data-stu-id="542d2-153">System.String</span></span>

## <span data-ttu-id="542d2-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="542d2-154">OUTPUTS</span></span>

### <span data-ttu-id="542d2-155">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="542d2-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="542d2-156">Note</span><span class="sxs-lookup"><span data-stu-id="542d2-156">NOTES</span></span>

## <span data-ttu-id="542d2-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="542d2-157">RELATED LINKS</span></span>

[<span data-ttu-id="542d2-158">Registro-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="542d2-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="542d2-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="542d2-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="542d2-160">Annullamento della registrazione-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="542d2-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


