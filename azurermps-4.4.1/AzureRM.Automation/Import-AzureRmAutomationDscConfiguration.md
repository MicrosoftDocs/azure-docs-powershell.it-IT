---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517124"
---
# <span data-ttu-id="c2b34-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2b34-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="c2b34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2b34-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b34-103">Importa una configurazione DSC in automazione.</span><span class="sxs-lookup"><span data-stu-id="c2b34-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2b34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2b34-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2b34-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b34-106">Il cmdlet **Import-AzureRmAutomationDscConfiguration** importa una configurazione DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c2b34-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="c2b34-107">Specifica il percorso di uno script APS che contiene una singola configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="c2b34-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="c2b34-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2b34-108">EXAMPLES</span></span>

### <span data-ttu-id="c2b34-109">Esempio 1: importare una configurazione DSC in automazione</span><span class="sxs-lookup"><span data-stu-id="c2b34-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="c2b34-110">Questo comando importa la configurazione DSC nel file denominato client.ps1 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c2b34-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="c2b34-111">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="c2b34-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="c2b34-112">Se esiste una configurazione DSC esistente, questo comando lo sostituisce.</span><span class="sxs-lookup"><span data-stu-id="c2b34-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="c2b34-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2b34-113">PARAMETERS</span></span>

### <span data-ttu-id="c2b34-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c2b34-114">-AutomationAccountName</span></span>
<span data-ttu-id="c2b34-115">Specifica il nome dell'account di automazione in cui questo cmdlet importa una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="c2b34-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="c2b34-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2b34-116">-Description</span></span>
<span data-ttu-id="c2b34-117">Specifica una descrizione della configurazione importata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b34-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="c2b34-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c2b34-118">-Force</span></span>
<span data-ttu-id="c2b34-119">Indica che questo cmdlet sostituisce una configurazione DSC esistente nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="c2b34-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="c2b34-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="c2b34-120">-LogVerbose</span></span>
<span data-ttu-id="c2b34-121">Specifica se questo cmdlet attiva o disattiva la registrazione dettagliata per i processi di compilazione della configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="c2b34-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="c2b34-122">Specificare un valore di $True per attivare la registrazione dettagliata o $False per disattivarla.</span><span class="sxs-lookup"><span data-stu-id="c2b34-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b34-123">-Pubblicato</span><span class="sxs-lookup"><span data-stu-id="c2b34-123">-Published</span></span>
<span data-ttu-id="c2b34-124">Indica che questo cmdlet importa la configurazione DSC nello stato Published.</span><span class="sxs-lookup"><span data-stu-id="c2b34-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="c2b34-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b34-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2b34-126">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="c2b34-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="c2b34-127">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="c2b34-127">-SourcePath</span></span>
<span data-ttu-id="c2b34-128">Specifica il percorso dello script wps_2 che contiene la configurazione DSC importata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b34-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b34-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2b34-129">-Tags</span></span>
<span data-ttu-id="c2b34-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c2b34-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c2b34-131">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="c2b34-131">For example:</span></span>

<span data-ttu-id="c2b34-132">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c2b34-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b34-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2b34-133">-Confirm</span></span>
<span data-ttu-id="c2b34-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b34-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b34-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b34-135">-WhatIf</span></span>
<span data-ttu-id="c2b34-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2b34-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b34-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2b34-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b34-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b34-138">-DefaultProfile</span></span>
<span data-ttu-id="c2b34-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b34-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b34-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b34-140">CommonParameters</span></span>
<span data-ttu-id="c2b34-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b34-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b34-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b34-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b34-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2b34-143">INPUTS</span></span>

## <span data-ttu-id="c2b34-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2b34-144">OUTPUTS</span></span>

### <span data-ttu-id="c2b34-145">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2b34-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="c2b34-146">Note</span><span class="sxs-lookup"><span data-stu-id="c2b34-146">NOTES</span></span>

## <span data-ttu-id="c2b34-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2b34-147">RELATED LINKS</span></span>

[<span data-ttu-id="c2b34-148">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2b34-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="c2b34-149">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2b34-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
