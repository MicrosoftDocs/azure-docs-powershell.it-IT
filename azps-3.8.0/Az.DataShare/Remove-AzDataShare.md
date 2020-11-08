---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: a9e9f5fdc71250acb2496c8eaaf1677461e9cd07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020832"
---
# <span data-ttu-id="90d6d-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="90d6d-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="90d6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="90d6d-103">Rimuove una condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="90d6d-103">Removes a data share.</span></span>

## <span data-ttu-id="90d6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90d6d-104">SYNTAX</span></span>

### <span data-ttu-id="90d6d-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90d6d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d6d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90d6d-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d6d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90d6d-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d6d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90d6d-108">DESCRIPTION</span></span>
<span data-ttu-id="90d6d-109">Il cmdlet **Remove-AzDataShare** rimuove una condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="90d6d-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="90d6d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90d6d-110">EXAMPLES</span></span>

### <span data-ttu-id="90d6d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="90d6d-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="90d6d-112">Questo comando rimuove la condivisione dati denominata AdsShare dall'account di condivisione dati di Azure WikiAds.</span><span class="sxs-lookup"><span data-stu-id="90d6d-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="90d6d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90d6d-113">PARAMETERS</span></span>

### <span data-ttu-id="90d6d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="90d6d-114">-AccountName</span></span>
<span data-ttu-id="90d6d-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="90d6d-115">Azure data share account name</span></span>

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

### <span data-ttu-id="90d6d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90d6d-116">-AsJob</span></span>
<span data-ttu-id="90d6d-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="90d6d-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="90d6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d6d-118">-DefaultProfile</span></span>
<span data-ttu-id="90d6d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90d6d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90d6d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90d6d-120">-InputObject</span></span>
<span data-ttu-id="90d6d-121">Oggetto di condivisione dati di Azure ''' tipo YAML: set di parametri PSDataShare: alias ByObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="90d6d-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="90d6d-122">Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: true (ByValue) accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="90d6d-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>


### <span data-ttu-id="90d6d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="90d6d-123">-Name</span></span>
<span data-ttu-id="90d6d-124">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="90d6d-124">Azure data share name</span></span>

<span data-ttu-id="90d6d-125">Tipo YAML: set di parametri stringa: alias ByFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="90d6d-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="90d6d-126">Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="90d6d-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="90d6d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90d6d-127">-PassThru</span></span>
<span data-ttu-id="90d6d-128">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="90d6d-128">Return object (if specified).</span></span>

<span data-ttu-id="90d6d-129">Tipo YAML: set di parametri SwitchParameter: (tutti) alias:</span><span class="sxs-lookup"><span data-stu-id="90d6d-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="90d6d-130">Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="90d6d-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="90d6d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d6d-131">-ResourceGroupName</span></span>
<span data-ttu-id="90d6d-132">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="90d6d-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="90d6d-133">Tipo YAML: set di parametri stringa: alias ByFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="90d6d-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="90d6d-134">Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="90d6d-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="90d6d-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90d6d-135">-ResourceId</span></span>
<span data-ttu-id="90d6d-136">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="90d6d-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="90d6d-137">Tipo YAML: set di parametri stringa: alias ByResourceIdParameterSet:</span><span class="sxs-lookup"><span data-stu-id="90d6d-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="90d6d-138">Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: true (ByPropertyName) accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="90d6d-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>


### <span data-ttu-id="90d6d-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90d6d-139">-Confirm</span></span>
<span data-ttu-id="90d6d-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d6d-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="90d6d-141">Tipo YAML: set di parametri SwitchParameter: (tutti) alias: CF</span><span class="sxs-lookup"><span data-stu-id="90d6d-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="90d6d-142">Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="90d6d-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="90d6d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d6d-143">-WhatIf</span></span>
<span data-ttu-id="90d6d-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90d6d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90d6d-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90d6d-145">The cmdlet is not run.</span></span>

<span data-ttu-id="90d6d-146">Tipo YAML: set di parametri SwitchParameter: (tutti) alias: Wi</span><span class="sxs-lookup"><span data-stu-id="90d6d-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="90d6d-147">Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false</span><span class="sxs-lookup"><span data-stu-id="90d6d-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>
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

### <span data-ttu-id="90d6d-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="90d6d-148">-Name</span></span>
<span data-ttu-id="90d6d-149">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="90d6d-149">Azure data share name</span></span>

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

### <span data-ttu-id="90d6d-150">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90d6d-150">-PassThru</span></span>
<span data-ttu-id="90d6d-151">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="90d6d-151">Return object (if specified).</span></span>

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

### <span data-ttu-id="90d6d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d6d-152">-ResourceGroupName</span></span>
<span data-ttu-id="90d6d-153">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="90d6d-153">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="90d6d-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90d6d-154">-ResourceId</span></span>
<span data-ttu-id="90d6d-155">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="90d6d-155">The resource id of the Azure data share</span></span>

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

### <span data-ttu-id="90d6d-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90d6d-156">-Confirm</span></span>
<span data-ttu-id="90d6d-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d6d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d6d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d6d-158">-WhatIf</span></span>
<span data-ttu-id="90d6d-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90d6d-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90d6d-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90d6d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d6d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d6d-161">CommonParameters</span></span>
<span data-ttu-id="90d6d-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d6d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d6d-163">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d6d-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d6d-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90d6d-164">INPUTS</span></span>

### <span data-ttu-id="90d6d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="90d6d-165">System.String</span></span>

### <span data-ttu-id="90d6d-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="90d6d-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="90d6d-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90d6d-167">OUTPUTS</span></span>

### <span data-ttu-id="90d6d-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90d6d-168">System.Boolean</span></span>

## <span data-ttu-id="90d6d-169">Note</span><span class="sxs-lookup"><span data-stu-id="90d6d-169">NOTES</span></span>

## <span data-ttu-id="90d6d-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90d6d-170">RELATED LINKS</span></span>
