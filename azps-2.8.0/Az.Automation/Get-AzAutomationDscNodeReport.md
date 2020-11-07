---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: a8d0244b9a26616e796a4e867a193da4ed3888d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675812"
---
# <span data-ttu-id="b9e34-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="b9e34-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="b9e34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9e34-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e34-103">Ottiene i report inviati da un nodo DSC all'automazione.</span><span class="sxs-lookup"><span data-stu-id="b9e34-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="b9e34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9e34-104">SYNTAX</span></span>

### <span data-ttu-id="b9e34-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9e34-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9e34-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="b9e34-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9e34-107">ById</span><span class="sxs-lookup"><span data-stu-id="b9e34-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9e34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9e34-108">DESCRIPTION</span></span>
<span data-ttu-id="b9e34-109">Il cmdlet **Get-AzAutomationDscNodeReport** ottiene i report inviati da un nodo DSC (APS desired state Configuration) a Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b9e34-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="b9e34-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9e34-110">EXAMPLES</span></span>

### <span data-ttu-id="b9e34-111">Esempio 1: ottenere tutti i report per un nodo DSC</span><span class="sxs-lookup"><span data-stu-id="b9e34-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="b9e34-112">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9e34-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b9e34-113">Il comando Archivia l'oggetto nella variabile $Node.</span><span class="sxs-lookup"><span data-stu-id="b9e34-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="b9e34-114">Il secondo comando recupera i metadati per tutti i report inviati dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9e34-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="b9e34-115">Il comando specifica il nodo usando la proprietà **ID** dell'oggetto $node.</span><span class="sxs-lookup"><span data-stu-id="b9e34-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="b9e34-116">Esempio 2: ottenere un report per un nodo DSC tramite ID report</span><span class="sxs-lookup"><span data-stu-id="b9e34-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="b9e34-117">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9e34-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b9e34-118">Il comando Archivia l'oggetto nella variabile $Node.</span><span class="sxs-lookup"><span data-stu-id="b9e34-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="b9e34-119">Il secondo comando recupera i metadati per il report identificato dall'ID specificato inviato dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9e34-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b9e34-120">Esempio 3: ottenere il report più recente per un nodo DSC</span><span class="sxs-lookup"><span data-stu-id="b9e34-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="b9e34-121">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9e34-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b9e34-122">Il comando Archivia l'oggetto nella variabile $Node.</span><span class="sxs-lookup"><span data-stu-id="b9e34-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="b9e34-123">Il secondo comando recupera i metadati per l'ultimo report inviato dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9e34-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b9e34-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9e34-124">PARAMETERS</span></span>

### <span data-ttu-id="b9e34-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b9e34-125">-AutomationAccountName</span></span>
<span data-ttu-id="b9e34-126">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b9e34-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="b9e34-127">Questo cmdlet Esporta i report per un nodo DSC che appartiene all'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b9e34-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9e34-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e34-128">-DefaultProfile</span></span>
<span data-ttu-id="b9e34-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b9e34-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9e34-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b9e34-130">-EndTime</span></span>
<span data-ttu-id="b9e34-131">Specifica un'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="b9e34-131">Specifies an end time.</span></span>
<span data-ttu-id="b9e34-132">Questo cmdlet restituisce i report che l'automazione ha ricevuto prima di questo periodo.</span><span class="sxs-lookup"><span data-stu-id="b9e34-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e34-133">-ID</span><span class="sxs-lookup"><span data-stu-id="b9e34-133">-Id</span></span>
<span data-ttu-id="b9e34-134">Specifica l'ID univoco del report DSC node per il cmdlet da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b9e34-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e34-135">-Ultimi</span><span class="sxs-lookup"><span data-stu-id="b9e34-135">-Latest</span></span>
<span data-ttu-id="b9e34-136">Indica che questo cmdlet ottiene il report DSC più recente per il nodo specificato.</span><span class="sxs-lookup"><span data-stu-id="b9e34-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e34-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="b9e34-137">-NodeId</span></span>
<span data-ttu-id="b9e34-138">Specifica l'ID univoco del nodo DSC per cui questo cmdlet ottiene i report.</span><span class="sxs-lookup"><span data-stu-id="b9e34-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e34-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e34-139">-ResourceGroupName</span></span>
<span data-ttu-id="b9e34-140">Specifica il nome di un gruppo di risorse che contiene il nodo DSC per cui questo cmdlet ottiene i report.</span><span class="sxs-lookup"><span data-stu-id="b9e34-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="b9e34-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b9e34-141">-StartTime</span></span>
<span data-ttu-id="b9e34-142">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="b9e34-142">Specifies a start time.</span></span>
<span data-ttu-id="b9e34-143">Questo cmdlet ottiene i report ricevuti da Automation dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="b9e34-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e34-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e34-144">CommonParameters</span></span>
<span data-ttu-id="b9e34-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e34-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e34-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e34-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e34-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9e34-147">INPUTS</span></span>

### <span data-ttu-id="b9e34-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="b9e34-148">System.Guid</span></span>

### <span data-ttu-id="b9e34-149">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b9e34-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b9e34-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b9e34-150">System.String</span></span>

## <span data-ttu-id="b9e34-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9e34-151">OUTPUTS</span></span>

### <span data-ttu-id="b9e34-152">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="b9e34-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b9e34-153">Note</span><span class="sxs-lookup"><span data-stu-id="b9e34-153">NOTES</span></span>

## <span data-ttu-id="b9e34-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9e34-154">RELATED LINKS</span></span>

[<span data-ttu-id="b9e34-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9e34-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="b9e34-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="b9e34-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


