---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: f690e5d7e35b819b727e2ea3f12c8f5e0b2a375f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507712"
---
# <span data-ttu-id="78d7d-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="78d7d-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="78d7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="78d7d-103">Esporta una configurazione DSC dall'automazione in un file locale.</span><span class="sxs-lookup"><span data-stu-id="78d7d-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78d7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78d7d-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="78d7d-106">Il cmdlet **Export-AzureRmAutomationDscConfiguration** esporta una configurazione DSC (APS desired state Configuration) da Azure Automation in un file locale.</span><span class="sxs-lookup"><span data-stu-id="78d7d-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="78d7d-107">Il file esportato ha un nome di file con estensione ps1.</span><span class="sxs-lookup"><span data-stu-id="78d7d-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="78d7d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78d7d-108">EXAMPLES</span></span>

### <span data-ttu-id="78d7d-109">Esempio 1: esportare la versione pubblicata di una configurazione DSC</span><span class="sxs-lookup"><span data-stu-id="78d7d-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="78d7d-110">Questo comando Esporta la versione pubblicata di una configurazione DSC in Automation nella cartella specificata, ovvero il desktop.</span><span class="sxs-lookup"><span data-stu-id="78d7d-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="78d7d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78d7d-111">PARAMETERS</span></span>

### <span data-ttu-id="78d7d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78d7d-112">-AutomationAccountName</span></span>
<span data-ttu-id="78d7d-113">Specifica il nome dell'account di automazione che contiene il DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="78d7d-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="78d7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d7d-114">-DefaultProfile</span></span>
<span data-ttu-id="78d7d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="78d7d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78d7d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="78d7d-116">-Force</span></span>
<span data-ttu-id="78d7d-117">Indica che questo cmdlet sostituisce un file locale esistente con un nuovo file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="78d7d-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="78d7d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="78d7d-118">-Name</span></span>
<span data-ttu-id="78d7d-119">Specifica il nome della configurazione DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="78d7d-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="78d7d-120">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="78d7d-120">-OutputFolder</span></span>
<span data-ttu-id="78d7d-121">Specifica la cartella di output in cui questo cmdlet Esporta la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="78d7d-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="78d7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="78d7d-123">Specifica il nome di un gruppo di risorse per cui questo cmdlet esporta una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="78d7d-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="78d7d-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="78d7d-124">-Slot</span></span>
<span data-ttu-id="78d7d-125">Specifica la versione della configurazione DSC che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="78d7d-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="78d7d-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="78d7d-126">Valid values are:</span></span> 
- <span data-ttu-id="78d7d-127">Progetto</span><span class="sxs-lookup"><span data-stu-id="78d7d-127">Draft</span></span>
- <span data-ttu-id="78d7d-128">Pubblicato il valore predefinito viene pubblicato.</span><span class="sxs-lookup"><span data-stu-id="78d7d-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="78d7d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="78d7d-129">-Confirm</span></span>
<span data-ttu-id="78d7d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d7d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d7d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d7d-131">-WhatIf</span></span>
<span data-ttu-id="78d7d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78d7d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d7d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78d7d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d7d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d7d-134">CommonParameters</span></span>
<span data-ttu-id="78d7d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d7d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d7d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d7d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d7d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78d7d-137">INPUTS</span></span>

### <span data-ttu-id="78d7d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="78d7d-138">System.String</span></span>

## <span data-ttu-id="78d7d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78d7d-139">OUTPUTS</span></span>

### <span data-ttu-id="78d7d-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="78d7d-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="78d7d-141">Note</span><span class="sxs-lookup"><span data-stu-id="78d7d-141">NOTES</span></span>

## <span data-ttu-id="78d7d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78d7d-142">RELATED LINKS</span></span>

[<span data-ttu-id="78d7d-143">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="78d7d-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="78d7d-144">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="78d7d-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


