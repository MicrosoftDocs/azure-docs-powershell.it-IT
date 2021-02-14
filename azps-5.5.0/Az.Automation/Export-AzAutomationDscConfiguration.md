---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197126"
---
# <span data-ttu-id="e3fa1-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3fa1-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="e3fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fa1-103">Esporta una configurazione DSC dall'automazione in un file locale.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="e3fa1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3fa1-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3fa1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3fa1-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fa1-106">Il cmdlet **Export-AzAutomationDscConfiguration** esporta una configurazione DSC (Desired State Configuration) APS dall'automazione di Azure in un file locale.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="e3fa1-107">Il file esportato ha estensione ps1.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="e3fa1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3fa1-108">EXAMPLES</span></span>

### <span data-ttu-id="e3fa1-109">Esempio 1: Esportare la versione pubblicata di una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="e3fa1-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="e3fa1-110">Questo comando esporta la versione pubblicata di una configurazione DSC nell'automazione nella cartella specificata, ovvero il desktop.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="e3fa1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3fa1-111">PARAMETERS</span></span>

### <span data-ttu-id="e3fa1-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e3fa1-112">-AutomationAccountName</span></span>
<span data-ttu-id="e3fa1-113">Specifica il nome dell'account di automazione che contiene il DSC esportato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="e3fa1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fa1-114">-DefaultProfile</span></span>
<span data-ttu-id="e3fa1-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e3fa1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3fa1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e3fa1-116">-Force</span></span>
<span data-ttu-id="e3fa1-117">Indica che questo cmdlet sostituisce un file locale esistente con un nuovo file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="e3fa1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e3fa1-118">-Name</span></span>
<span data-ttu-id="e3fa1-119">Specifica il nome della configurazione DSC esportato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3fa1-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="e3fa1-120">-OutputFolder</span></span>
<span data-ttu-id="e3fa1-121">Specifica la cartella di output in cui il cmdlet esporta la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="e3fa1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fa1-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3fa1-123">Specifica il nome di un gruppo di risorse per cui questo cmdlet esporta una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="e3fa1-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="e3fa1-124">-Slot</span></span>
<span data-ttu-id="e3fa1-125">Specifica la versione della configurazione DSC esportata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="e3fa1-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e3fa1-126">Valid values are:</span></span> 
- <span data-ttu-id="e3fa1-127">Bozza</span><span class="sxs-lookup"><span data-stu-id="e3fa1-127">Draft</span></span>
- <span data-ttu-id="e3fa1-128">Pubblicato Il valore predefinito è Pubblicato.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3fa1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3fa1-129">-Confirm</span></span>
<span data-ttu-id="e3fa1-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3fa1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3fa1-131">-WhatIf</span></span>
<span data-ttu-id="e3fa1-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3fa1-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3fa1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fa1-134">CommonParameters</span></span>
<span data-ttu-id="e3fa1-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fa1-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3fa1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fa1-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3fa1-137">INPUTS</span></span>

### <span data-ttu-id="e3fa1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e3fa1-138">System.String</span></span>

## <span data-ttu-id="e3fa1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3fa1-139">OUTPUTS</span></span>

### <span data-ttu-id="e3fa1-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="e3fa1-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="e3fa1-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3fa1-141">NOTES</span></span>

## <span data-ttu-id="e3fa1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3fa1-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3fa1-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3fa1-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="e3fa1-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3fa1-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


