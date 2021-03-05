---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964733"
---
# <span data-ttu-id="f4c92-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="f4c92-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="f4c92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4c92-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c92-103">Rimuove una condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="f4c92-103">Removes a data share.</span></span>

## <span data-ttu-id="f4c92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4c92-104">SYNTAX</span></span>

### <span data-ttu-id="f4c92-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4c92-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c92-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4c92-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c92-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4c92-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c92-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4c92-108">DESCRIPTION</span></span>
<span data-ttu-id="f4c92-109">Il cmdlet **Remove-AzDataShare** rimuove una condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="f4c92-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="f4c92-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4c92-110">EXAMPLES</span></span>

### <span data-ttu-id="f4c92-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4c92-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="f4c92-112">Questo comando rimuove la condivisione dati denominata AdsShare dall'account di condivisione dati Di Azure WikiAds.</span><span class="sxs-lookup"><span data-stu-id="f4c92-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="f4c92-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4c92-113">PARAMETERS</span></span>

### <span data-ttu-id="f4c92-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4c92-114">-AccountName</span></span>
<span data-ttu-id="f4c92-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="f4c92-115">Azure data share account name</span></span>

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

### <span data-ttu-id="f4c92-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4c92-116">-AsJob</span></span>
<span data-ttu-id="f4c92-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="f4c92-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="f4c92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c92-118">-DefaultProfile</span></span>
<span data-ttu-id="f4c92-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4c92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4c92-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4c92-120">-InputObject</span></span>
<span data-ttu-id="f4c92-121">Oggetto di condivisione dati di Azure ' ''yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="f4c92-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="f4c92-122">Obbligatorio: Posizione True: Valore predefinito denominato: Nessuna accetta input pipeline: True (ByValue) Accetta caratteri jolly: False</span><span class="sxs-lookup"><span data-stu-id="f4c92-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="f4c92-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f4c92-123">-Name</span></span>
<span data-ttu-id="f4c92-124">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="f4c92-124">Azure data share name</span></span>

<span data-ttu-id="f4c92-125">Tipo yaml: Set di parametri stringa: Alias byFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="f4c92-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="f4c92-126">Obbligatorio: Posizione True: Valore predefinito denominato: Input pipeline None Accept: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="f4c92-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="f4c92-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4c92-127">-PassThru</span></span>
<span data-ttu-id="f4c92-128">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="f4c92-128">Return object (if specified).</span></span>

<span data-ttu-id="f4c92-129">Tipo yaml: Set di parametri SwitchParameter: (Tutti) Alias:</span><span class="sxs-lookup"><span data-stu-id="f4c92-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="f4c92-130">Obbligatorio: Posizione Falso: Valore predefinito denominato: Input pipeline None Accept: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="f4c92-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="f4c92-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c92-131">-ResourceGroupName</span></span>
<span data-ttu-id="f4c92-132">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="f4c92-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="f4c92-133">Tipo yaml: Set di parametri stringa: Alias byFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="f4c92-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="f4c92-134">Obbligatorio: Posizione True: Valore predefinito denominato: Input pipeline None Accept: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="f4c92-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="f4c92-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4c92-135">-ResourceId</span></span>
<span data-ttu-id="f4c92-136">ID risorsa della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="f4c92-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="f4c92-137">Tipo yaml: Set di parametri stringa: Alias byResourceIdParameterSet:</span><span class="sxs-lookup"><span data-stu-id="f4c92-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="f4c92-138">Obbligatorio: Posizione True: Valore predefinito denominato: Nessuna accetta input pipeline: True (ByPropertyName) Accetta caratteri jolly: False</span><span class="sxs-lookup"><span data-stu-id="f4c92-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="f4c92-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4c92-139">-Confirm</span></span>
<span data-ttu-id="f4c92-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c92-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="f4c92-141">Tipo yaml: Set di parametri SwitchParameter: (All) Alias: cf</span><span class="sxs-lookup"><span data-stu-id="f4c92-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="f4c92-142">Obbligatorio: Posizione Falso: Valore predefinito denominato: Input pipeline None Accept: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="f4c92-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="f4c92-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c92-143">-WhatIf</span></span>
<span data-ttu-id="f4c92-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4c92-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4c92-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4c92-145">The cmdlet is not run.</span></span>

<span data-ttu-id="f4c92-146">Tipo yaml: Set di parametri SwitchParameter: (All) Alias: wi</span><span class="sxs-lookup"><span data-stu-id="f4c92-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="f4c92-147">Obbligatorio: Posizione Falso: Valore predefinito denominato: Input pipeline None Accept: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="f4c92-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="f4c92-148">Tipo yaml: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDset di parametri ataShare: Alias byObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="f4c92-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="f4c92-149">Obbligatorio: Posizione True: Valore predefinito denominato: Nessuna accetta input pipeline: True (ByValue) Accetta caratteri jolly: False</span><span class="sxs-lookup"><span data-stu-id="f4c92-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="f4c92-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c92-150">CommonParameters</span></span>
<span data-ttu-id="f4c92-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4c92-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c92-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4c92-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c92-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4c92-153">INPUTS</span></span>

### <span data-ttu-id="f4c92-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f4c92-154">System.String</span></span>

### <span data-ttu-id="f4c92-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="f4c92-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="f4c92-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4c92-156">OUTPUTS</span></span>

### <span data-ttu-id="f4c92-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4c92-157">System.Boolean</span></span>

## <span data-ttu-id="f4c92-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4c92-158">NOTES</span></span>

## <span data-ttu-id="f4c92-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4c92-159">RELATED LINKS</span></span>
