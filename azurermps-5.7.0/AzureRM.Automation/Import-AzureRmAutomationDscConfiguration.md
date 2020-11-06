---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e8d7cfcf595d7dd445d66865d922676c96b7e6d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508412"
---
# <span data-ttu-id="871dd-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="871dd-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="871dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="871dd-102">SYNOPSIS</span></span>
<span data-ttu-id="871dd-103">Importa una configurazione DSC in automazione.</span><span class="sxs-lookup"><span data-stu-id="871dd-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="871dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="871dd-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="871dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="871dd-105">DESCRIPTION</span></span>
<span data-ttu-id="871dd-106">Il cmdlet **Import-AzureRmAutomationDscConfiguration** importa una configurazione DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="871dd-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="871dd-107">Specifica il percorso di uno script APS che contiene una singola configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="871dd-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="871dd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="871dd-108">EXAMPLES</span></span>

### <span data-ttu-id="871dd-109">Esempio 1: importare una configurazione DSC in automazione</span><span class="sxs-lookup"><span data-stu-id="871dd-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="871dd-110">Questo comando importa la configurazione DSC nel file denominato client.ps1 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="871dd-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="871dd-111">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="871dd-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="871dd-112">Se esiste una configurazione DSC esistente, questo comando lo sostituisce.</span><span class="sxs-lookup"><span data-stu-id="871dd-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="871dd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="871dd-113">PARAMETERS</span></span>

### <span data-ttu-id="871dd-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="871dd-114">-AutomationAccountName</span></span>
<span data-ttu-id="871dd-115">Specifica il nome dell'account di automazione in cui questo cmdlet importa una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="871dd-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="871dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871dd-116">-DefaultProfile</span></span>
<span data-ttu-id="871dd-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="871dd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="871dd-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="871dd-118">-Description</span></span>
<span data-ttu-id="871dd-119">Specifica una descrizione della configurazione importata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="871dd-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="871dd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="871dd-120">-Force</span></span>
<span data-ttu-id="871dd-121">Indica che questo cmdlet sostituisce una configurazione DSC esistente nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="871dd-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="871dd-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="871dd-122">-LogVerbose</span></span>
<span data-ttu-id="871dd-123">Specifica se questo cmdlet attiva o disattiva la registrazione dettagliata per i processi di compilazione della configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="871dd-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="871dd-124">Specificare un valore di $True per attivare la registrazione dettagliata o $False per disattivarla.</span><span class="sxs-lookup"><span data-stu-id="871dd-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871dd-125">-Pubblicato</span><span class="sxs-lookup"><span data-stu-id="871dd-125">-Published</span></span>
<span data-ttu-id="871dd-126">Indica che questo cmdlet importa la configurazione DSC nello stato Published.</span><span class="sxs-lookup"><span data-stu-id="871dd-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="871dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="871dd-128">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="871dd-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="871dd-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="871dd-129">-SourcePath</span></span>
<span data-ttu-id="871dd-130">Specifica il percorso dello script wps_2 che contiene la configurazione DSC importata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="871dd-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871dd-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="871dd-131">-Tags</span></span>
<span data-ttu-id="871dd-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="871dd-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="871dd-133">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="871dd-133">For example:</span></span>

<span data-ttu-id="871dd-134">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="871dd-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871dd-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="871dd-135">-Confirm</span></span>
<span data-ttu-id="871dd-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="871dd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="871dd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="871dd-137">-WhatIf</span></span>
<span data-ttu-id="871dd-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="871dd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="871dd-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="871dd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="871dd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871dd-140">CommonParameters</span></span>
<span data-ttu-id="871dd-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871dd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871dd-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="871dd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871dd-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="871dd-143">INPUTS</span></span>

### <span data-ttu-id="871dd-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="871dd-144">None</span></span>
<span data-ttu-id="871dd-145">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="871dd-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="871dd-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="871dd-146">OUTPUTS</span></span>

### <span data-ttu-id="871dd-147">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="871dd-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="871dd-148">Note</span><span class="sxs-lookup"><span data-stu-id="871dd-148">NOTES</span></span>

## <span data-ttu-id="871dd-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="871dd-149">RELATED LINKS</span></span>

[<span data-ttu-id="871dd-150">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="871dd-150">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="871dd-151">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="871dd-151">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
