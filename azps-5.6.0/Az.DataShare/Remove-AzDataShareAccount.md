---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 74651ea4a9a108db9cc3f666ad6f78f494fcd676
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971118"
---
# <span data-ttu-id="b5c75-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="b5c75-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="b5c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c75-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c75-103">Rimuove un account di condivisione dati</span><span class="sxs-lookup"><span data-stu-id="b5c75-103">Removes a datashare account</span></span>

## <span data-ttu-id="b5c75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5c75-104">SYNTAX</span></span>

### <span data-ttu-id="b5c75-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5c75-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c75-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c75-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c75-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c75-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c75-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5c75-108">DESCRIPTION</span></span>
<span data-ttu-id="b5c75-109">Il cmdlet **Remove-AzDataShareAccount** rimuove un account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="b5c75-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="b5c75-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5c75-110">EXAMPLES</span></span>

### <span data-ttu-id="b5c75-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5c75-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="b5c75-112">Questo comando rimuove l'account di condivisione dati denominato WikiADS dal gruppo di risorse denominato ADS.</span><span class="sxs-lookup"><span data-stu-id="b5c75-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="b5c75-113">Questo comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="b5c75-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="b5c75-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5c75-114">PARAMETERS</span></span>

### <span data-ttu-id="b5c75-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5c75-115">-AsJob</span></span>
<span data-ttu-id="b5c75-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="b5c75-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b5c75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c75-117">-DefaultProfile</span></span>
<span data-ttu-id="b5c75-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c75-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b5c75-119">-Force</span></span>
<span data-ttu-id="b5c75-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="b5c75-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="b5c75-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5c75-121">-InputObject</span></span>
<span data-ttu-id="b5c75-122">Oggetto account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c75-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c75-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b5c75-123">-Name</span></span>
<span data-ttu-id="b5c75-124">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c75-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="b5c75-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5c75-125">-PassThru</span></span>
<span data-ttu-id="b5c75-126">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="b5c75-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="b5c75-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c75-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5c75-128">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c75-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="b5c75-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c75-129">-ResourceId</span></span>
<span data-ttu-id="b5c75-130">ID risorsa dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c75-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="b5c75-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5c75-131">-Confirm</span></span>
<span data-ttu-id="b5c75-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5c75-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c75-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c75-133">-WhatIf</span></span>
<span data-ttu-id="b5c75-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5c75-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5c75-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5c75-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c75-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c75-136">CommonParameters</span></span>
<span data-ttu-id="b5c75-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c75-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c75-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5c75-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c75-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5c75-139">INPUTS</span></span>

### <span data-ttu-id="b5c75-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b5c75-140">System.String</span></span>

### <span data-ttu-id="b5c75-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="b5c75-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="b5c75-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5c75-142">OUTPUTS</span></span>

### <span data-ttu-id="b5c75-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5c75-143">System.Boolean</span></span>

## <span data-ttu-id="b5c75-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5c75-144">NOTES</span></span>

## <span data-ttu-id="b5c75-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5c75-145">RELATED LINKS</span></span>
