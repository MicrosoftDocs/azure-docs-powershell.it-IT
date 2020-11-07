---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688575"
---
# <span data-ttu-id="df37a-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="df37a-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="df37a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df37a-102">SYNOPSIS</span></span>
<span data-ttu-id="df37a-103">Ottiene i report inviati da un nodo DSC all'automazione.</span><span class="sxs-lookup"><span data-stu-id="df37a-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df37a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df37a-104">SYNTAX</span></span>

### <span data-ttu-id="df37a-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df37a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df37a-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="df37a-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df37a-107">ById</span><span class="sxs-lookup"><span data-stu-id="df37a-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df37a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df37a-108">DESCRIPTION</span></span>
<span data-ttu-id="df37a-109">Il cmdlet **Get-AzureRmAutomationDscNodeReport** ottiene i report inviati da un nodo DSC (APS desired state Configuration) a Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="df37a-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="df37a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df37a-110">EXAMPLES</span></span>

### <span data-ttu-id="df37a-111">Esempio 1: ottenere tutti i report per un nodo DSC</span><span class="sxs-lookup"><span data-stu-id="df37a-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="df37a-112">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df37a-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="df37a-113">Il comando Archivia l'oggetto nella variabile $Node.</span><span class="sxs-lookup"><span data-stu-id="df37a-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="df37a-114">Il secondo comando recupera i metadati per tutti i report inviati dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df37a-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="df37a-115">Il comando specifica il nodo usando la proprietà **ID** dell'oggetto $node.</span><span class="sxs-lookup"><span data-stu-id="df37a-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="df37a-116">Esempio 2: ottenere un report per un nodo DSC tramite ID report</span><span class="sxs-lookup"><span data-stu-id="df37a-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="df37a-117">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df37a-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="df37a-118">Il comando Archivia l'oggetto nella variabile $Node.</span><span class="sxs-lookup"><span data-stu-id="df37a-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="df37a-119">Il secondo comando recupera i metadati per il report identificato dall'ID specificato inviato dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df37a-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="df37a-120">Esempio 3: ottenere il report più recente per un nodo DSC</span><span class="sxs-lookup"><span data-stu-id="df37a-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="df37a-121">Il primo comando ottiene il nodo DSC per il computer denominato Computer14 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df37a-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="df37a-122">Il comando Archivia l'oggetto nella variabile $Node.</span><span class="sxs-lookup"><span data-stu-id="df37a-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="df37a-123">Il secondo comando recupera i metadati per l'ultimo report inviato dal nodo DSC denominato Computer14 all'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df37a-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="df37a-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df37a-124">PARAMETERS</span></span>

### <span data-ttu-id="df37a-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df37a-125">-AutomationAccountName</span></span>
<span data-ttu-id="df37a-126">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="df37a-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="df37a-127">Questo cmdlet Esporta i report per un nodo DSC che appartiene all'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="df37a-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df37a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df37a-128">-DefaultProfile</span></span>
<span data-ttu-id="df37a-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="df37a-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df37a-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="df37a-130">-EndTime</span></span>
<span data-ttu-id="df37a-131">Specifica un'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="df37a-131">Specifies an end time.</span></span>
<span data-ttu-id="df37a-132">Questo cmdlet restituisce i report che l'automazione ha ricevuto prima di questo periodo.</span><span class="sxs-lookup"><span data-stu-id="df37a-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df37a-133">-ID</span><span class="sxs-lookup"><span data-stu-id="df37a-133">-Id</span></span>
<span data-ttu-id="df37a-134">Specifica l'ID univoco del report DSC node per il cmdlet da ottenere.</span><span class="sxs-lookup"><span data-stu-id="df37a-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df37a-135">-Ultimi</span><span class="sxs-lookup"><span data-stu-id="df37a-135">-Latest</span></span>
<span data-ttu-id="df37a-136">Indica che questo cmdlet ottiene il report DSC più recente per il nodo specificato.</span><span class="sxs-lookup"><span data-stu-id="df37a-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByLatest
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df37a-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="df37a-137">-NodeId</span></span>
<span data-ttu-id="df37a-138">Specifica l'ID univoco del nodo DSC per cui questo cmdlet ottiene i report.</span><span class="sxs-lookup"><span data-stu-id="df37a-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df37a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df37a-139">-ResourceGroupName</span></span>
<span data-ttu-id="df37a-140">Specifica il nome di un gruppo di risorse che contiene il nodo DSC per cui questo cmdlet ottiene i report.</span><span class="sxs-lookup"><span data-stu-id="df37a-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df37a-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="df37a-141">-StartTime</span></span>
<span data-ttu-id="df37a-142">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="df37a-142">Specifies a start time.</span></span>
<span data-ttu-id="df37a-143">Questo cmdlet ottiene i report ricevuti da Automation dopo questo periodo.</span><span class="sxs-lookup"><span data-stu-id="df37a-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df37a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df37a-144">CommonParameters</span></span>
<span data-ttu-id="df37a-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df37a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df37a-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df37a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df37a-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df37a-147">INPUTS</span></span>

### <span data-ttu-id="df37a-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="df37a-148">None</span></span>
<span data-ttu-id="df37a-149">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="df37a-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df37a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df37a-150">OUTPUTS</span></span>

### <span data-ttu-id="df37a-151">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="df37a-151">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="df37a-152">Note</span><span class="sxs-lookup"><span data-stu-id="df37a-152">NOTES</span></span>

## <span data-ttu-id="df37a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df37a-153">RELATED LINKS</span></span>

[<span data-ttu-id="df37a-154">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="df37a-154">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="df37a-155">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="df37a-155">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


