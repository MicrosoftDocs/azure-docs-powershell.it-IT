---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: c27f878d2dbb0e52a16216a2158c737bc523c932
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959037"
---
# <span data-ttu-id="742a8-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="742a8-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="742a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742a8-102">SYNOPSIS</span></span>
<span data-ttu-id="742a8-103">Esporta una configurazione DSC dall'automazione in un file locale.</span><span class="sxs-lookup"><span data-stu-id="742a8-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="742a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="742a8-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="742a8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="742a8-105">DESCRIPTION</span></span>
<span data-ttu-id="742a8-106">Il cmdlet **Export-AzAutomationDscConfiguration** esporta una configurazione DSC (Desired State Configuration) APS dall'automazione di Azure in un file locale.</span><span class="sxs-lookup"><span data-stu-id="742a8-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="742a8-107">Il file esportato ha estensione ps1.</span><span class="sxs-lookup"><span data-stu-id="742a8-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="742a8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="742a8-108">EXAMPLES</span></span>

### <span data-ttu-id="742a8-109">Esempio 1: Esportare la versione pubblicata di una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="742a8-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="742a8-110">Questo comando esporta la versione pubblicata di una configurazione DSC nell'automazione nella cartella specificata, ovvero il desktop.</span><span class="sxs-lookup"><span data-stu-id="742a8-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="742a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="742a8-111">PARAMETERS</span></span>

### <span data-ttu-id="742a8-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="742a8-112">-AutomationAccountName</span></span>
<span data-ttu-id="742a8-113">Specifica il nome dell'account di automazione che contiene il DSC esportato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="742a8-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="742a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742a8-114">-DefaultProfile</span></span>
<span data-ttu-id="742a8-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="742a8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="742a8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="742a8-116">-Force</span></span>
<span data-ttu-id="742a8-117">Indica che questo cmdlet sostituisce un file locale esistente con un nuovo file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="742a8-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="742a8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="742a8-118">-Name</span></span>
<span data-ttu-id="742a8-119">Specifica il nome della configurazione DSC esportato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="742a8-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="742a8-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="742a8-120">-OutputFolder</span></span>
<span data-ttu-id="742a8-121">Specifica la cartella di output in cui il cmdlet esporta la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="742a8-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="742a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="742a8-123">Specifica il nome di un gruppo di risorse per cui questo cmdlet esporta una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="742a8-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="742a8-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="742a8-124">-Slot</span></span>
<span data-ttu-id="742a8-125">Specifica la versione della configurazione DSC esportata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="742a8-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="742a8-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="742a8-126">Valid values are:</span></span> 
- <span data-ttu-id="742a8-127">Bozza</span><span class="sxs-lookup"><span data-stu-id="742a8-127">Draft</span></span>
- <span data-ttu-id="742a8-128">Pubblicato Il valore predefinito è Pubblicato.</span><span class="sxs-lookup"><span data-stu-id="742a8-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="742a8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="742a8-129">-Confirm</span></span>
<span data-ttu-id="742a8-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="742a8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="742a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="742a8-131">-WhatIf</span></span>
<span data-ttu-id="742a8-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="742a8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="742a8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="742a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="742a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742a8-134">CommonParameters</span></span>
<span data-ttu-id="742a8-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742a8-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742a8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742a8-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="742a8-137">INPUTS</span></span>

### <span data-ttu-id="742a8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="742a8-138">System.String</span></span>

## <span data-ttu-id="742a8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="742a8-139">OUTPUTS</span></span>

### <span data-ttu-id="742a8-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="742a8-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="742a8-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="742a8-141">NOTES</span></span>

## <span data-ttu-id="742a8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="742a8-142">RELATED LINKS</span></span>

[<span data-ttu-id="742a8-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="742a8-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="742a8-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="742a8-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


