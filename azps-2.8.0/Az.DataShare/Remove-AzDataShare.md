---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: b16e5a9ff2c6e5a898baf56cf237676665bc12c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674658"
---
# <span data-ttu-id="12fee-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="12fee-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="12fee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12fee-102">SYNOPSIS</span></span>
<span data-ttu-id="12fee-103">Rimuove una condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="12fee-103">Removes a data share.</span></span>

## <span data-ttu-id="12fee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12fee-104">SYNTAX</span></span>

### <span data-ttu-id="12fee-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12fee-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fee-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12fee-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fee-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12fee-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12fee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12fee-108">DESCRIPTION</span></span>
<span data-ttu-id="12fee-109">Il cmdlet **Remove-AzDataShare** rimuove una condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="12fee-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="12fee-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12fee-110">EXAMPLES</span></span>

### <span data-ttu-id="12fee-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12fee-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="12fee-112">Questo comando rimuove la condivisione dati denominata AdsShare dall'account di condivisione dati di Azure WikiAds.</span><span class="sxs-lookup"><span data-stu-id="12fee-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="12fee-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12fee-113">PARAMETERS</span></span>

### <span data-ttu-id="12fee-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12fee-114">-AccountName</span></span>
<span data-ttu-id="12fee-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="12fee-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fee-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12fee-116">-AsJob</span></span>
<span data-ttu-id="12fee-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="12fee-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="12fee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fee-118">-DefaultProfile</span></span>
<span data-ttu-id="12fee-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12fee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12fee-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12fee-120">-InputObject</span></span>
<span data-ttu-id="12fee-121">Oggetto di condivisione dati di Azure ''' tipo YAML: set di parametri PSDataShare: alias ByObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="12fee-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="12fee-122">Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: true (ByValue) accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="12fee-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>


### <span data-ttu-id="12fee-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="12fee-123">-Name</span></span>
<span data-ttu-id="12fee-124">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="12fee-124">Azure data share name</span></span>

<span data-ttu-id="12fee-125">Tipo YAML: set di parametri stringa: alias ByFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="12fee-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="12fee-126">Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="12fee-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="12fee-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12fee-127">-PassThru</span></span>
<span data-ttu-id="12fee-128">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="12fee-128">Return object (if specified).</span></span>

<span data-ttu-id="12fee-129">Tipo YAML: set di parametri SwitchParameter: (tutti) alias:</span><span class="sxs-lookup"><span data-stu-id="12fee-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="12fee-130">Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="12fee-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="12fee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fee-131">-ResourceGroupName</span></span>
<span data-ttu-id="12fee-132">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="12fee-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="12fee-133">Tipo YAML: set di parametri stringa: alias ByFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="12fee-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="12fee-134">Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="12fee-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="12fee-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12fee-135">-ResourceId</span></span>
<span data-ttu-id="12fee-136">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="12fee-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="12fee-137">Tipo YAML: set di parametri stringa: alias ByResourceIdParameterSet:</span><span class="sxs-lookup"><span data-stu-id="12fee-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="12fee-138">Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: true (ByPropertyName) accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="12fee-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>


### <span data-ttu-id="12fee-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12fee-139">-Confirm</span></span>
<span data-ttu-id="12fee-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fee-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="12fee-141">Tipo YAML: set di parametri SwitchParameter: (tutti) alias: CF</span><span class="sxs-lookup"><span data-stu-id="12fee-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="12fee-142">Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="12fee-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="12fee-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fee-143">-WhatIf</span></span>
<span data-ttu-id="12fee-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12fee-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12fee-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12fee-145">The cmdlet is not run.</span></span>

<span data-ttu-id="12fee-146">Tipo YAML: set di parametri SwitchParameter: (tutti) alias: Wi</span><span class="sxs-lookup"><span data-stu-id="12fee-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="12fee-147">Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="12fee-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fee-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="12fee-148">-Name</span></span>
<span data-ttu-id="12fee-149">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="12fee-149">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fee-150">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12fee-150">-PassThru</span></span>
<span data-ttu-id="12fee-151">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="12fee-151">Return object (if specified).</span></span>

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

### <span data-ttu-id="12fee-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fee-152">-ResourceGroupName</span></span>
<span data-ttu-id="12fee-153">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="12fee-153">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fee-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12fee-154">-ResourceId</span></span>
<span data-ttu-id="12fee-155">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="12fee-155">The resource id of the Azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12fee-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12fee-156">-Confirm</span></span>
<span data-ttu-id="12fee-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fee-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fee-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fee-158">-WhatIf</span></span>
<span data-ttu-id="12fee-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12fee-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12fee-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12fee-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fee-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fee-161">CommonParameters</span></span>
<span data-ttu-id="12fee-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fee-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fee-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12fee-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fee-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12fee-164">INPUTS</span></span>

### <span data-ttu-id="12fee-165">System. String</span><span class="sxs-lookup"><span data-stu-id="12fee-165">System.String</span></span>

### <span data-ttu-id="12fee-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="12fee-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="12fee-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12fee-167">OUTPUTS</span></span>

### <span data-ttu-id="12fee-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12fee-168">System.Boolean</span></span>

## <span data-ttu-id="12fee-169">Note</span><span class="sxs-lookup"><span data-stu-id="12fee-169">NOTES</span></span>

## <span data-ttu-id="12fee-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12fee-170">RELATED LINKS</span></span>
