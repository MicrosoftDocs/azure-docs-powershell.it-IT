---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199678"
---
# <span data-ttu-id="bb13e-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="bb13e-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="bb13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb13e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb13e-103">Esporta il contenuto non elaborati di un report DSC inviato da un nodo DSC all'automazione.</span><span class="sxs-lookup"><span data-stu-id="bb13e-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="bb13e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb13e-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb13e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb13e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb13e-106">Il cmdlet **Export-AzAutomationDscNodeReportContent** esporta il contenuto non elaborato di un report APS Desired State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="bb13e-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="bb13e-107">Un nodo DSC invia un report DSC all'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb13e-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="bb13e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb13e-108">EXAMPLES</span></span>

### <span data-ttu-id="bb13e-109">Esempio 1: Esportare un report da un nodo DSC</span><span class="sxs-lookup"><span data-stu-id="bb13e-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="bb13e-110">Questo set di comandi esporta il report più recente dal nodo DSC denominato Computer14 al desktop.</span><span class="sxs-lookup"><span data-stu-id="bb13e-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="bb13e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb13e-111">PARAMETERS</span></span>

### <span data-ttu-id="bb13e-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb13e-112">-AutomationAccountName</span></span>
<span data-ttu-id="bb13e-113">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="bb13e-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="bb13e-114">Questo cmdlet esporta il contenuto del report per un nodo DSC che appartiene all'account di automazione specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bb13e-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb13e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb13e-115">-DefaultProfile</span></span>
<span data-ttu-id="bb13e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="bb13e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb13e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bb13e-117">-Force</span></span>
<span data-ttu-id="bb13e-118">Indica che questo cmdlet sostituisce un file locale esistente con un nuovo file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="bb13e-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb13e-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="bb13e-119">-NodeId</span></span>
<span data-ttu-id="bb13e-120">Specifica l'ID univoco del nodo DSC per cui il cmdlet esporta il contenuto del report.</span><span class="sxs-lookup"><span data-stu-id="bb13e-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="bb13e-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="bb13e-121">-OutputFolder</span></span>
<span data-ttu-id="bb13e-122">Specifica la cartella di output in cui il cmdlet esporta il contenuto del report.</span><span class="sxs-lookup"><span data-stu-id="bb13e-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb13e-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="bb13e-123">-ReportId</span></span>
<span data-ttu-id="bb13e-124">Specifica l'ID univoco del report del nodo DSC esportato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb13e-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb13e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb13e-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb13e-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb13e-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bb13e-127">Questo cmdlet esporta il contenuto di un report per il nodo DSC che appartiene al gruppo di risorse specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb13e-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="bb13e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb13e-128">-Confirm</span></span>
<span data-ttu-id="bb13e-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb13e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb13e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb13e-130">-WhatIf</span></span>
<span data-ttu-id="bb13e-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb13e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb13e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb13e-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb13e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb13e-133">CommonParameters</span></span>
<span data-ttu-id="bb13e-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb13e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb13e-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb13e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb13e-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb13e-136">INPUTS</span></span>

### <span data-ttu-id="bb13e-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bb13e-137">System.Guid</span></span>

### <span data-ttu-id="bb13e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bb13e-138">System.String</span></span>

## <span data-ttu-id="bb13e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb13e-139">OUTPUTS</span></span>

### <span data-ttu-id="bb13e-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="bb13e-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="bb13e-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb13e-141">NOTES</span></span>

## <span data-ttu-id="bb13e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb13e-142">RELATED LINKS</span></span>

[<span data-ttu-id="bb13e-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="bb13e-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="bb13e-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="bb13e-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="bb13e-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="bb13e-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


