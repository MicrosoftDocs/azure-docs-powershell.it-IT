---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200535"
---
# <span data-ttu-id="c81ea-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c81ea-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="c81ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c81ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c81ea-103">rimuove un abbonamento alla condivisione</span><span class="sxs-lookup"><span data-stu-id="c81ea-103">removes a share subscription</span></span>

## <span data-ttu-id="c81ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c81ea-104">SYNTAX</span></span>

### <span data-ttu-id="c81ea-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c81ea-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c81ea-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c81ea-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c81ea-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c81ea-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c81ea-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c81ea-108">DESCRIPTION</span></span>
<span data-ttu-id="c81ea-109">Il cmdlet **Remove-AzDataShareSubscription** rimuove una sottoscrizione di condivisione</span><span class="sxs-lookup"><span data-stu-id="c81ea-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="c81ea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c81ea-110">EXAMPLES</span></span>

### <span data-ttu-id="c81ea-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c81ea-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c81ea-112">Questo comando rimuove un abbonamento alla condivisione denominato AdsShareSubscription dall'account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="c81ea-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="c81ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c81ea-113">PARAMETERS</span></span>

### <span data-ttu-id="c81ea-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c81ea-114">-AccountName</span></span>
<span data-ttu-id="c81ea-115">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="c81ea-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="c81ea-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c81ea-116">-AsJob</span></span>
<span data-ttu-id="c81ea-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="c81ea-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="c81ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81ea-118">-DefaultProfile</span></span>
<span data-ttu-id="c81ea-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c81ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c81ea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c81ea-120">-InputObject</span></span>
<span data-ttu-id="c81ea-121">Oggetto sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c81ea-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81ea-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c81ea-122">-Name</span></span>
<span data-ttu-id="c81ea-123">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c81ea-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="c81ea-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c81ea-124">-PassThru</span></span>
<span data-ttu-id="c81ea-125">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="c81ea-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="c81ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="c81ea-127">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c81ea-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c81ea-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c81ea-128">-ResourceId</span></span>
<span data-ttu-id="c81ea-129">ID risorsa della sottoscrizione della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c81ea-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="c81ea-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c81ea-130">-Confirm</span></span>
<span data-ttu-id="c81ea-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c81ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81ea-132">-WhatIf</span></span>
<span data-ttu-id="c81ea-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c81ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81ea-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c81ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81ea-135">CommonParameters</span></span>
<span data-ttu-id="c81ea-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81ea-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c81ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81ea-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="c81ea-138">INPUTS</span></span>

### <span data-ttu-id="c81ea-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c81ea-139">System.String</span></span>

### <span data-ttu-id="c81ea-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c81ea-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="c81ea-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c81ea-141">OUTPUTS</span></span>

### <span data-ttu-id="c81ea-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c81ea-142">System.Boolean</span></span>

## <span data-ttu-id="c81ea-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="c81ea-143">NOTES</span></span>

## <span data-ttu-id="c81ea-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c81ea-144">RELATED LINKS</span></span>
