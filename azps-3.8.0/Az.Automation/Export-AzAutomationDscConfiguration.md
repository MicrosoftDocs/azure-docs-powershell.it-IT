---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020678"
---
# <span data-ttu-id="6c98a-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c98a-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="6c98a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c98a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c98a-103">Esporta una configurazione DSC dall'automazione in un file locale.</span><span class="sxs-lookup"><span data-stu-id="6c98a-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="6c98a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c98a-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c98a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c98a-105">DESCRIPTION</span></span>
<span data-ttu-id="6c98a-106">Il cmdlet **Export-AzAutomationDscConfiguration** esporta una configurazione DSC (APS desired state Configuration) da Azure Automation in un file locale.</span><span class="sxs-lookup"><span data-stu-id="6c98a-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="6c98a-107">Il file esportato ha un nome di file con estensione ps1.</span><span class="sxs-lookup"><span data-stu-id="6c98a-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="6c98a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c98a-108">EXAMPLES</span></span>

### <span data-ttu-id="6c98a-109">Esempio 1: esportare la versione pubblicata di una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="6c98a-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="6c98a-110">Questo comando Esporta la versione pubblicata di una configurazione DSC in Automation nella cartella specificata, ovvero il desktop.</span><span class="sxs-lookup"><span data-stu-id="6c98a-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="6c98a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c98a-111">PARAMETERS</span></span>

### <span data-ttu-id="6c98a-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6c98a-112">-AutomationAccountName</span></span>
<span data-ttu-id="6c98a-113">Specifica il nome dell'account di automazione che contiene il DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="6c98a-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="6c98a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c98a-114">-DefaultProfile</span></span>
<span data-ttu-id="6c98a-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6c98a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c98a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6c98a-116">-Force</span></span>
<span data-ttu-id="6c98a-117">Indica che questo cmdlet sostituisce un file locale esistente con un nuovo file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="6c98a-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="6c98a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c98a-118">-Name</span></span>
<span data-ttu-id="6c98a-119">Specifica il nome della configurazione DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="6c98a-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="6c98a-120">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="6c98a-120">-OutputFolder</span></span>
<span data-ttu-id="6c98a-121">Specifica la cartella di output in cui questo cmdlet Esporta la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="6c98a-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="6c98a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c98a-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c98a-123">Specifica il nome di un gruppo di risorse per cui questo cmdlet esporta una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="6c98a-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="6c98a-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="6c98a-124">-Slot</span></span>
<span data-ttu-id="6c98a-125">Specifica la versione della configurazione DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="6c98a-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="6c98a-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6c98a-126">Valid values are:</span></span> 
- <span data-ttu-id="6c98a-127">Progetto</span><span class="sxs-lookup"><span data-stu-id="6c98a-127">Draft</span></span>
- <span data-ttu-id="6c98a-128">Pubblicato il valore predefinito viene pubblicato.</span><span class="sxs-lookup"><span data-stu-id="6c98a-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="6c98a-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c98a-129">-Confirm</span></span>
<span data-ttu-id="6c98a-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c98a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c98a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c98a-131">-WhatIf</span></span>
<span data-ttu-id="6c98a-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c98a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c98a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c98a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c98a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c98a-134">CommonParameters</span></span>
<span data-ttu-id="6c98a-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c98a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c98a-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c98a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c98a-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c98a-137">INPUTS</span></span>

### <span data-ttu-id="6c98a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6c98a-138">System.String</span></span>

## <span data-ttu-id="6c98a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c98a-139">OUTPUTS</span></span>

### <span data-ttu-id="6c98a-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="6c98a-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="6c98a-141">Note</span><span class="sxs-lookup"><span data-stu-id="6c98a-141">NOTES</span></span>

## <span data-ttu-id="6c98a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c98a-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c98a-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c98a-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="6c98a-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c98a-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


