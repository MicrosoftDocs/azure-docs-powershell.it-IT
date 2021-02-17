---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: cc7beb921e09a2cdf1568e9cb693dd01f059e562
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205563"
---
# <span data-ttu-id="4eb5a-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="4eb5a-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="4eb5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb5a-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb5a-103">Recupera i report inviati da un nodo DSC all'automazione.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="4eb5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4eb5a-104">SYNTAX</span></span>

### <span data-ttu-id="4eb5a-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4eb5a-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb5a-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="4eb5a-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eb5a-107">ById</span><span class="sxs-lookup"><span data-stu-id="4eb5a-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eb5a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4eb5a-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb5a-109">Il cmdlet **Get-AzAutomationDscNodeReport** riceve i report inviati da un nodo APS Desired State Configuration (DSC) all'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="4eb5a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4eb5a-110">EXAMPLES</span></span>

### <span data-ttu-id="4eb5a-111">Esempio 1: Ottenere tutti i report per un nodo DSC</span><span class="sxs-lookup"><span data-stu-id="4eb5a-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="4eb5a-112">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4eb5a-113">Il comando archivia l'oggetto nella $Node variabile.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="4eb5a-114">Il secondo comando recupera i metadati per tutti i report inviati dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="4eb5a-115">Il comando specifica il nodo usando la **proprietà ID** dell'oggetto $Node dati.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="4eb5a-116">Esempio 2: Ottenere un report per un nodo DSC in base all'ID report</span><span class="sxs-lookup"><span data-stu-id="4eb5a-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="4eb5a-117">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4eb5a-118">Il comando archivia l'oggetto nella $Node variabile.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="4eb5a-119">Il secondo comando recupera i metadati per il report identificato dall'ID specificato inviato dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4eb5a-120">Esempio 3: Ottenere il report più recente per un nodo DSC</span><span class="sxs-lookup"><span data-stu-id="4eb5a-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="4eb5a-121">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4eb5a-122">Il comando archivia l'oggetto nella $Node variabile.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="4eb5a-123">Il secondo comando recupera i metadati per il report più recente inviato dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4eb5a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb5a-124">PARAMETERS</span></span>

### <span data-ttu-id="4eb5a-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4eb5a-125">-AutomationAccountName</span></span>
<span data-ttu-id="4eb5a-126">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="4eb5a-127">Questo cmdlet esporta i report per un nodo DSC che appartiene all'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="4eb5a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb5a-128">-DefaultProfile</span></span>
<span data-ttu-id="4eb5a-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4eb5a-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eb5a-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4eb5a-130">-EndTime</span></span>
<span data-ttu-id="4eb5a-131">Specifica un'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-131">Specifies an end time.</span></span>
<span data-ttu-id="4eb5a-132">Questo cmdlet riceve i report ricevuti dall'automazione prima di questo periodo.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="4eb5a-133">-Id</span><span class="sxs-lookup"><span data-stu-id="4eb5a-133">-Id</span></span>
<span data-ttu-id="4eb5a-134">Specifica l'ID univoco del report del nodo DSC per il cmdlet da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="4eb5a-135">-Più recenti</span><span class="sxs-lookup"><span data-stu-id="4eb5a-135">-Latest</span></span>
<span data-ttu-id="4eb5a-136">Indica che questo cmdlet ottiene il report DSC più recente solo per il nodo specificato.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="4eb5a-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="4eb5a-137">-NodeId</span></span>
<span data-ttu-id="4eb5a-138">Specifica l'ID univoco del nodo DSC per cui il cmdlet riceve i report.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="4eb5a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb5a-139">-ResourceGroupName</span></span>
<span data-ttu-id="4eb5a-140">Specifica il nome di un gruppo di risorse che contiene il nodo DSC per cui il cmdlet riceve i report.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="4eb5a-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4eb5a-141">-StartTime</span></span>
<span data-ttu-id="4eb5a-142">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-142">Specifies a start time.</span></span>
<span data-ttu-id="4eb5a-143">Questo cmdlet riceve report che l'automazione ha ricevuto dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="4eb5a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb5a-144">CommonParameters</span></span>
<span data-ttu-id="4eb5a-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb5a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb5a-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb5a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb5a-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="4eb5a-147">INPUTS</span></span>

### <span data-ttu-id="4eb5a-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4eb5a-148">System.Guid</span></span>

### <span data-ttu-id="4eb5a-149">System.Nullable'1[[System.DateTimeToken, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4eb5a-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4eb5a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb5a-150">System.String</span></span>

## <span data-ttu-id="4eb5a-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4eb5a-151">OUTPUTS</span></span>

### <span data-ttu-id="4eb5a-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="4eb5a-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="4eb5a-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="4eb5a-153">NOTES</span></span>

## <span data-ttu-id="4eb5a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4eb5a-154">RELATED LINKS</span></span>

[<span data-ttu-id="4eb5a-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4eb5a-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="4eb5a-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="4eb5a-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


