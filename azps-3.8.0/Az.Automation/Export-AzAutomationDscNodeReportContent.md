---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020681"
---
# <span data-ttu-id="0506f-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="0506f-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="0506f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0506f-102">SYNOPSIS</span></span>
<span data-ttu-id="0506f-103">Esporta il contenuto non elaborato di un report DSC inviato da un nodo DSC all'automazione.</span><span class="sxs-lookup"><span data-stu-id="0506f-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="0506f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0506f-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0506f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0506f-105">DESCRIPTION</span></span>
<span data-ttu-id="0506f-106">Il cmdlet **Export-AzAutomationDscNodeReportContent** Esporta il contenuto non elaborato di un report di configurazione di stato desiderato APS (DSC).</span><span class="sxs-lookup"><span data-stu-id="0506f-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="0506f-107">Un nodo DSC Invia un report DSC ad Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0506f-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="0506f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0506f-108">EXAMPLES</span></span>

### <span data-ttu-id="0506f-109">Esempio 1: esportare un report da un nodo DSC</span><span class="sxs-lookup"><span data-stu-id="0506f-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="0506f-110">Questo set di comandi Esporta il report più recente dal nodo DSC denominato Computer14 sul desktop.</span><span class="sxs-lookup"><span data-stu-id="0506f-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="0506f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0506f-111">PARAMETERS</span></span>

### <span data-ttu-id="0506f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0506f-112">-AutomationAccountName</span></span>
<span data-ttu-id="0506f-113">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="0506f-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="0506f-114">Questo cmdlet Esporta il contenuto del report per un nodo DSC che appartiene all'account di automazione specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0506f-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="0506f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0506f-115">-DefaultProfile</span></span>
<span data-ttu-id="0506f-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0506f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0506f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0506f-117">-Force</span></span>
<span data-ttu-id="0506f-118">Indica che questo cmdlet sostituisce un file locale esistente con un nuovo file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="0506f-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="0506f-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="0506f-119">-NodeId</span></span>
<span data-ttu-id="0506f-120">Specifica l'ID univoco del nodo DSC per cui questo cmdlet Esporta il contenuto del report.</span><span class="sxs-lookup"><span data-stu-id="0506f-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="0506f-121">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="0506f-121">-OutputFolder</span></span>
<span data-ttu-id="0506f-122">Specifica la cartella di output in cui questo cmdlet Esporta il contenuto del report.</span><span class="sxs-lookup"><span data-stu-id="0506f-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="0506f-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="0506f-123">-ReportId</span></span>
<span data-ttu-id="0506f-124">Specifica l'ID univoco del report DSC node che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="0506f-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="0506f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0506f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0506f-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0506f-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0506f-127">Questo cmdlet Esporta il contenuto di un report per il nodo DSC che appartiene al gruppo di risorse specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0506f-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="0506f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0506f-128">-Confirm</span></span>
<span data-ttu-id="0506f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0506f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0506f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0506f-130">-WhatIf</span></span>
<span data-ttu-id="0506f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0506f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0506f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0506f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0506f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0506f-133">CommonParameters</span></span>
<span data-ttu-id="0506f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0506f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0506f-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0506f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0506f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0506f-136">INPUTS</span></span>

### <span data-ttu-id="0506f-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="0506f-137">System.Guid</span></span>

### <span data-ttu-id="0506f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0506f-138">System.String</span></span>

## <span data-ttu-id="0506f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0506f-139">OUTPUTS</span></span>

### <span data-ttu-id="0506f-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="0506f-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="0506f-141">Note</span><span class="sxs-lookup"><span data-stu-id="0506f-141">NOTES</span></span>

## <span data-ttu-id="0506f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0506f-142">RELATED LINKS</span></span>

[<span data-ttu-id="0506f-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="0506f-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="0506f-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0506f-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="0506f-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="0506f-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


