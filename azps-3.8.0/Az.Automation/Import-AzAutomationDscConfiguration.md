---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
ms.openlocfilehash: 21b3e8c29d9d74f548ca9d212a72d4b70520aa82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022941"
---
# <span data-ttu-id="c17e2-101">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c17e2-101">Import-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="c17e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c17e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c17e2-103">Importa una configurazione DSC in automazione.</span><span class="sxs-lookup"><span data-stu-id="c17e2-103">Imports a DSC configuration into Automation.</span></span>

## <span data-ttu-id="c17e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c17e2-104">SYNTAX</span></span>

```
Import-AzAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c17e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c17e2-105">DESCRIPTION</span></span>
<span data-ttu-id="c17e2-106">Il cmdlet **Import-AzAutomationDscConfiguration** importa una configurazione DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c17e2-106">The **Import-AzAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="c17e2-107">Specifica il percorso di uno script APS che contiene una singola configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="c17e2-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="c17e2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c17e2-108">EXAMPLES</span></span>

### <span data-ttu-id="c17e2-109">Esempio 1: importare una configurazione DSC in automazione</span><span class="sxs-lookup"><span data-stu-id="c17e2-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="c17e2-110">Questo comando importa la configurazione DSC nel file denominato client.ps1 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c17e2-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="c17e2-111">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="c17e2-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="c17e2-112">Se esiste una configurazione DSC esistente, questo comando lo sostituisce.</span><span class="sxs-lookup"><span data-stu-id="c17e2-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="c17e2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c17e2-113">PARAMETERS</span></span>

### <span data-ttu-id="c17e2-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c17e2-114">-AutomationAccountName</span></span>
<span data-ttu-id="c17e2-115">Specifica il nome dell'account di automazione in cui questo cmdlet importa una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="c17e2-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="c17e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17e2-116">-DefaultProfile</span></span>
<span data-ttu-id="c17e2-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c17e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c17e2-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c17e2-118">-Description</span></span>
<span data-ttu-id="c17e2-119">Specifica una descrizione della configurazione importata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c17e2-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="c17e2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c17e2-120">-Force</span></span>
<span data-ttu-id="c17e2-121">Indica che questo cmdlet sostituisce una configurazione DSC esistente nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="c17e2-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="c17e2-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="c17e2-122">-LogVerbose</span></span>
<span data-ttu-id="c17e2-123">Specifica se questo cmdlet attiva o disattiva la registrazione dettagliata per i processi di compilazione della configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="c17e2-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="c17e2-124">Specificare un valore di $True per attivare la registrazione dettagliata o $False per disattivarla.</span><span class="sxs-lookup"><span data-stu-id="c17e2-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="c17e2-125">-Pubblicato</span><span class="sxs-lookup"><span data-stu-id="c17e2-125">-Published</span></span>
<span data-ttu-id="c17e2-126">Indica che questo cmdlet importa la configurazione DSC nello stato Published.</span><span class="sxs-lookup"><span data-stu-id="c17e2-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="c17e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c17e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="c17e2-128">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa una configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="c17e2-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="c17e2-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="c17e2-129">-SourcePath</span></span>
<span data-ttu-id="c17e2-130">Specifica il percorso dello script wps_2 che contiene la configurazione DSC importata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c17e2-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="c17e2-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="c17e2-131">-Tags</span></span>
<span data-ttu-id="c17e2-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c17e2-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c17e2-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c17e2-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c17e2-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c17e2-134">-Confirm</span></span>
<span data-ttu-id="c17e2-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c17e2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c17e2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c17e2-136">-WhatIf</span></span>
<span data-ttu-id="c17e2-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c17e2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c17e2-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c17e2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c17e2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17e2-139">CommonParameters</span></span>
<span data-ttu-id="c17e2-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c17e2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17e2-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c17e2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17e2-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c17e2-142">INPUTS</span></span>

### <span data-ttu-id="c17e2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c17e2-143">System.String</span></span>

### <span data-ttu-id="c17e2-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="c17e2-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="c17e2-145">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c17e2-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c17e2-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c17e2-146">OUTPUTS</span></span>

### <span data-ttu-id="c17e2-147">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c17e2-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="c17e2-148">Note</span><span class="sxs-lookup"><span data-stu-id="c17e2-148">NOTES</span></span>

## <span data-ttu-id="c17e2-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c17e2-149">RELATED LINKS</span></span>

[<span data-ttu-id="c17e2-150">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c17e2-150">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="c17e2-151">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c17e2-151">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)
