---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: 51d7df7f6b1e99188e5be31537700f4eef019053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517163"
---
# <span data-ttu-id="cd449-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cd449-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="cd449-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd449-102">SYNOPSIS</span></span>
<span data-ttu-id="cd449-103">Ottiene i nodi DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="cd449-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd449-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd449-104">SYNTAX</span></span>

### <span data-ttu-id="cd449-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd449-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd449-106">ById</span><span class="sxs-lookup"><span data-stu-id="cd449-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd449-107">ByName</span><span class="sxs-lookup"><span data-stu-id="cd449-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd449-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd449-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd449-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd449-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd449-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd449-110">DESCRIPTION</span></span>
<span data-ttu-id="cd449-111">Il cmdlet **Get-AzureRmAutomationDscNode** ottiene i nodi di configurazione di stato (DSC) APS di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cd449-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="cd449-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd449-112">EXAMPLES</span></span>

### <span data-ttu-id="cd449-113">Esempio 1: ottenere tutti i nodi DSC</span><span class="sxs-lookup"><span data-stu-id="cd449-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="cd449-114">Questo comando consente di ottenere metadati per tutti i nodi DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cd449-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cd449-115">Esempio 2: ottenere tutti i nodi DSC per una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="cd449-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="cd449-116">Questo comando consente di ottenere metadati per tutti i nodi DSC nell'account di automazione denominato Contoso17 mappati a una configurazione di nodi DSC generata da ContosoConfiguration di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="cd449-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="cd449-117">Esempio 3: ottenere un nodo DSC in base all'ID</span><span class="sxs-lookup"><span data-stu-id="cd449-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="cd449-118">Questo comando consente di ottenere metadati in un nodo DSC con l'ID specificato nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cd449-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cd449-119">Esempio 4: ottenere un nodo DSC per nome</span><span class="sxs-lookup"><span data-stu-id="cd449-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="cd449-120">Questo comando consente di ottenere metadati in un nodo DSC con il nome Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cd449-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cd449-121">Esempio 5: ottenere tutti i nodi DSC mappati a una configurazione di nodi DSC</span><span class="sxs-lookup"><span data-stu-id="cd449-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="cd449-122">Questo comando consente di ottenere metadati in tutti i nodi DSC nell'account di automazione denominato Contoso17 mappati a una configurazione di nodi DSC denominata ContosoConfiguration. webserver.</span><span class="sxs-lookup"><span data-stu-id="cd449-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="cd449-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd449-123">PARAMETERS</span></span>

### <span data-ttu-id="cd449-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd449-124">-AutomationAccountName</span></span>
<span data-ttu-id="cd449-125">Specifica il nome dell'account di automazione che contiene i nodi DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd449-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cd449-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cd449-126">-ConfigurationName</span></span>
<span data-ttu-id="cd449-127">Specifica il nome di una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="cd449-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="cd449-128">Questo cmdlet ottiene i nodi DSC che corrispondono alle configurazioni di nodi generate dalla configurazione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cd449-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd449-129">-ID</span><span class="sxs-lookup"><span data-stu-id="cd449-129">-Id</span></span>
<span data-ttu-id="cd449-130">Specifica l'ID univoco del nodo DSC ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd449-130">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cd449-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd449-131">-Name</span></span>
<span data-ttu-id="cd449-132">Specifica il nome di un nodo DSC che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd449-132">Specifies the name of a DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cd449-133">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cd449-133">-NodeConfigurationName</span></span>
<span data-ttu-id="cd449-134">Specifica il nome di una configurazione di nodo ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd449-134">Specifies the name of a node configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cd449-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd449-135">-ResourceGroupName</span></span>
<span data-ttu-id="cd449-136">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene i nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="cd449-136">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="cd449-137">-Stato</span><span class="sxs-lookup"><span data-stu-id="cd449-137">-Status</span></span>
<span data-ttu-id="cd449-138">Specifica lo stato dei nodi DSC ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd449-138">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="cd449-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="cd449-139">Valid values are:</span></span> 

- <span data-ttu-id="cd449-140">Conformi</span><span class="sxs-lookup"><span data-stu-id="cd449-140">Compliant</span></span> 
- <span data-ttu-id="cd449-141">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="cd449-141">NotCompliant</span></span>
- <span data-ttu-id="cd449-142">Fallito</span><span class="sxs-lookup"><span data-stu-id="cd449-142">Failed</span></span>
- <span data-ttu-id="cd449-143">In sospeso</span><span class="sxs-lookup"><span data-stu-id="cd449-143">Pending</span></span> 
- <span data-ttu-id="cd449-144">Ricevuto</span><span class="sxs-lookup"><span data-stu-id="cd449-144">Received</span></span>
- <span data-ttu-id="cd449-145">Risponde</span><span class="sxs-lookup"><span data-stu-id="cd449-145">Unresponsive</span></span>

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

### <span data-ttu-id="cd449-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd449-146">-DefaultProfile</span></span>
<span data-ttu-id="cd449-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd449-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd449-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd449-148">CommonParameters</span></span>
<span data-ttu-id="cd449-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd449-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd449-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd449-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd449-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd449-151">INPUTS</span></span>

## <span data-ttu-id="cd449-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd449-152">OUTPUTS</span></span>

### <span data-ttu-id="cd449-153">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="cd449-153">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="cd449-154">Note</span><span class="sxs-lookup"><span data-stu-id="cd449-154">NOTES</span></span>

## <span data-ttu-id="cd449-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd449-155">RELATED LINKS</span></span>

[<span data-ttu-id="cd449-156">Registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cd449-156">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="cd449-157">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cd449-157">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="cd449-158">Annullamento della registrazione-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cd449-158">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


