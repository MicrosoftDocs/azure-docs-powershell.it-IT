---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 4cb023fecb020e37535f47823df6f02ee9f5050e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007965"
---
# <span data-ttu-id="18ada-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="18ada-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="18ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18ada-102">SYNOPSIS</span></span>
<span data-ttu-id="18ada-103">rimuove un abbonamento alla condivisione</span><span class="sxs-lookup"><span data-stu-id="18ada-103">removes a share subscription</span></span>

## <span data-ttu-id="18ada-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18ada-104">SYNTAX</span></span>

### <span data-ttu-id="18ada-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18ada-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18ada-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18ada-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18ada-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18ada-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18ada-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18ada-108">DESCRIPTION</span></span>
<span data-ttu-id="18ada-109">Il cmdlet **Remove-AzDataShareSubscription** rimuove una sottoscrizione di condivisione</span><span class="sxs-lookup"><span data-stu-id="18ada-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="18ada-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18ada-110">EXAMPLES</span></span>

### <span data-ttu-id="18ada-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18ada-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="18ada-112">Questo comando rimuove un abbonamento alla condivisione denominato AdsShareSubscription dall'account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="18ada-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="18ada-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18ada-113">PARAMETERS</span></span>

### <span data-ttu-id="18ada-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18ada-114">-AccountName</span></span>
<span data-ttu-id="18ada-115">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ada-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="18ada-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18ada-116">-AsJob</span></span>
<span data-ttu-id="18ada-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="18ada-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="18ada-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ada-118">-DefaultProfile</span></span>
<span data-ttu-id="18ada-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18ada-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18ada-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18ada-120">-InputObject</span></span>
<span data-ttu-id="18ada-121">Oggetto sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="18ada-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="18ada-122">-Name</span><span class="sxs-lookup"><span data-stu-id="18ada-122">-Name</span></span>
<span data-ttu-id="18ada-123">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="18ada-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="18ada-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18ada-124">-PassThru</span></span>
<span data-ttu-id="18ada-125">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="18ada-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="18ada-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ada-126">-ResourceGroupName</span></span>
<span data-ttu-id="18ada-127">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="18ada-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="18ada-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18ada-128">-ResourceId</span></span>
<span data-ttu-id="18ada-129">ID risorsa della sottoscrizione della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="18ada-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="18ada-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18ada-130">-Confirm</span></span>
<span data-ttu-id="18ada-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ada-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18ada-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ada-132">-WhatIf</span></span>
<span data-ttu-id="18ada-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18ada-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18ada-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18ada-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18ada-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ada-135">CommonParameters</span></span>
<span data-ttu-id="18ada-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ada-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ada-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18ada-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ada-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="18ada-138">INPUTS</span></span>

### <span data-ttu-id="18ada-139">System.String</span><span class="sxs-lookup"><span data-stu-id="18ada-139">System.String</span></span>

### <span data-ttu-id="18ada-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="18ada-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="18ada-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18ada-141">OUTPUTS</span></span>

### <span data-ttu-id="18ada-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18ada-142">System.Boolean</span></span>

## <span data-ttu-id="18ada-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="18ada-143">NOTES</span></span>

## <span data-ttu-id="18ada-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18ada-144">RELATED LINKS</span></span>
