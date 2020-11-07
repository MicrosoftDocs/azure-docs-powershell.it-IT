---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2f739c9471e2a6144c12033ade885a445bade12e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687654"
---
# <span data-ttu-id="8f67d-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f67d-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="8f67d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f67d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f67d-103">Esporta una configurazione DSC dall'automazione in un file locale.</span><span class="sxs-lookup"><span data-stu-id="8f67d-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f67d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f67d-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f67d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f67d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f67d-106">Il cmdlet **Export-AzureRmAutomationDscConfiguration** esporta una configurazione DSC (APS desired state Configuration) da Azure Automation in un file locale.</span><span class="sxs-lookup"><span data-stu-id="8f67d-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="8f67d-107">Il file esportato ha un nome di file con estensione ps1.</span><span class="sxs-lookup"><span data-stu-id="8f67d-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="8f67d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f67d-108">EXAMPLES</span></span>

### <span data-ttu-id="8f67d-109">Esempio 1: esportare la versione pubblicata di una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="8f67d-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="8f67d-110">Questo comando Esporta la versione pubblicata di una configurazione DSC in Automation nella cartella specificata, ovvero il desktop.</span><span class="sxs-lookup"><span data-stu-id="8f67d-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="8f67d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f67d-111">PARAMETERS</span></span>

### <span data-ttu-id="8f67d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f67d-112">-AutomationAccountName</span></span>
<span data-ttu-id="8f67d-113">Specifica il nome dell'account di automazione che contiene il DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="8f67d-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="8f67d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f67d-114">-DefaultProfile</span></span>
<span data-ttu-id="8f67d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8f67d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f67d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8f67d-116">-Force</span></span>
<span data-ttu-id="8f67d-117">Indica che questo cmdlet sostituisce un file locale esistente con un nuovo file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="8f67d-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f67d-118">-Name</span></span>
<span data-ttu-id="8f67d-119">Specifica il nome della configurazione DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="8f67d-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f67d-120">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="8f67d-120">-OutputFolder</span></span>
<span data-ttu-id="8f67d-121">Specifica la cartella di output in cui questo cmdlet Esporta la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="8f67d-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f67d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f67d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f67d-123">Specifica il nome di un gruppo di risorse per cui questo cmdlet esporta una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="8f67d-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="8f67d-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="8f67d-124">-Slot</span></span>
<span data-ttu-id="8f67d-125">Specifica la versione della configurazione DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="8f67d-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="8f67d-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="8f67d-126">Valid values are:</span></span> 

- <span data-ttu-id="8f67d-127">Progetto</span><span class="sxs-lookup"><span data-stu-id="8f67d-127">Draft</span></span>
- <span data-ttu-id="8f67d-128">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="8f67d-128">Published</span></span> 

<span data-ttu-id="8f67d-129">Il valore predefinito viene pubblicato.</span><span class="sxs-lookup"><span data-stu-id="8f67d-129">The default value is Published.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f67d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f67d-130">-Confirm</span></span>
<span data-ttu-id="8f67d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f67d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f67d-132">-WhatIf</span></span>
<span data-ttu-id="8f67d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f67d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f67d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f67d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f67d-135">CommonParameters</span></span>
<span data-ttu-id="8f67d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f67d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f67d-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f67d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f67d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f67d-138">INPUTS</span></span>

### <span data-ttu-id="8f67d-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8f67d-139">None</span></span>
<span data-ttu-id="8f67d-140">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8f67d-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f67d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f67d-141">OUTPUTS</span></span>

### <span data-ttu-id="8f67d-142">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="8f67d-142">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="8f67d-143">Note</span><span class="sxs-lookup"><span data-stu-id="8f67d-143">NOTES</span></span>

## <span data-ttu-id="8f67d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f67d-144">RELATED LINKS</span></span>

[<span data-ttu-id="8f67d-145">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f67d-145">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="8f67d-146">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f67d-146">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


