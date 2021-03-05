---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: c96df19d110a795177d138b7ec34faefb72c0970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966557"
---
# <span data-ttu-id="9355c-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="9355c-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="9355c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9355c-102">SYNOPSIS</span></span>
<span data-ttu-id="9355c-103">rimuove un'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="9355c-103">removes a synchronization setting</span></span>

## <span data-ttu-id="9355c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9355c-104">SYNTAX</span></span>

### <span data-ttu-id="9355c-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9355c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9355c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9355c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9355c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9355c-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9355c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9355c-108">DESCRIPTION</span></span>
<span data-ttu-id="9355c-109">Il cmdlet **Remove-AzDataShareSynchronizationSetting** rimuove un'impostazione di sincronizzazione della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="9355c-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="9355c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9355c-110">EXAMPLES</span></span>

### <span data-ttu-id="9355c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9355c-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="9355c-112">Questo comando rimuove un'impostazione di sincronizzazione denominata AdsShareSynchronizationSetting dalla condivisione AdsShare.</span><span class="sxs-lookup"><span data-stu-id="9355c-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="9355c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9355c-113">PARAMETERS</span></span>

### <span data-ttu-id="9355c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9355c-114">-AccountName</span></span>
<span data-ttu-id="9355c-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="9355c-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="9355c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9355c-116">-AsJob</span></span>
<span data-ttu-id="9355c-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="9355c-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="9355c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9355c-118">-DefaultProfile</span></span>
<span data-ttu-id="9355c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9355c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9355c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9355c-120">-InputObject</span></span>
<span data-ttu-id="9355c-121">Impostazione Sincronizzazione condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="9355c-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9355c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9355c-122">-Name</span></span>
<span data-ttu-id="9355c-123">Nome dell'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="9355c-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="9355c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9355c-124">-PassThru</span></span>
<span data-ttu-id="9355c-125">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="9355c-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="9355c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9355c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9355c-127">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="9355c-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9355c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9355c-128">-ResourceId</span></span>
<span data-ttu-id="9355c-129">ID risorsa dell'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="9355c-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="9355c-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9355c-130">-ShareName</span></span>
<span data-ttu-id="9355c-131">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="9355c-131">Azure data share name</span></span>

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

### <span data-ttu-id="9355c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9355c-132">-Confirm</span></span>
<span data-ttu-id="9355c-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9355c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9355c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9355c-134">-WhatIf</span></span>
<span data-ttu-id="9355c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9355c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9355c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9355c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9355c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9355c-137">CommonParameters</span></span>
<span data-ttu-id="9355c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9355c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9355c-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9355c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9355c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="9355c-140">INPUTS</span></span>

### <span data-ttu-id="9355c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9355c-141">System.String</span></span>

### <span data-ttu-id="9355c-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="9355c-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="9355c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9355c-143">OUTPUTS</span></span>

### <span data-ttu-id="9355c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9355c-144">System.Boolean</span></span>

## <span data-ttu-id="9355c-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="9355c-145">NOTES</span></span>

## <span data-ttu-id="9355c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9355c-146">RELATED LINKS</span></span>
