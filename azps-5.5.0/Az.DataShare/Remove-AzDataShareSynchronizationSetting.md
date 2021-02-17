---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194558"
---
# <span data-ttu-id="de0ef-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="de0ef-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="de0ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de0ef-102">SYNOPSIS</span></span>
<span data-ttu-id="de0ef-103">rimuove un'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="de0ef-103">removes a synchronization setting</span></span>

## <span data-ttu-id="de0ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de0ef-104">SYNTAX</span></span>

### <span data-ttu-id="de0ef-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de0ef-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de0ef-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de0ef-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de0ef-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de0ef-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de0ef-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de0ef-108">DESCRIPTION</span></span>
<span data-ttu-id="de0ef-109">Il cmdlet **Remove-AzDataShareSynchronizationSetting** rimuove un'impostazione di sincronizzazione della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="de0ef-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="de0ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de0ef-110">EXAMPLES</span></span>

### <span data-ttu-id="de0ef-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de0ef-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="de0ef-112">Questo comando rimuove un'impostazione di sincronizzazione denominata AdsShareSynchronizationSetting dalla condivisione AdsShare.</span><span class="sxs-lookup"><span data-stu-id="de0ef-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="de0ef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de0ef-113">PARAMETERS</span></span>

### <span data-ttu-id="de0ef-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de0ef-114">-AccountName</span></span>
<span data-ttu-id="de0ef-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="de0ef-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="de0ef-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de0ef-116">-AsJob</span></span>
<span data-ttu-id="de0ef-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="de0ef-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="de0ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0ef-118">-DefaultProfile</span></span>
<span data-ttu-id="de0ef-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de0ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de0ef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de0ef-120">-InputObject</span></span>
<span data-ttu-id="de0ef-121">Impostazione Sincronizzazione condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="de0ef-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="de0ef-122">-Name</span><span class="sxs-lookup"><span data-stu-id="de0ef-122">-Name</span></span>
<span data-ttu-id="de0ef-123">Nome dell'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="de0ef-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="de0ef-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de0ef-124">-PassThru</span></span>
<span data-ttu-id="de0ef-125">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="de0ef-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="de0ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="de0ef-127">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="de0ef-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="de0ef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de0ef-128">-ResourceId</span></span>
<span data-ttu-id="de0ef-129">ID risorsa dell'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="de0ef-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="de0ef-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="de0ef-130">-ShareName</span></span>
<span data-ttu-id="de0ef-131">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="de0ef-131">Azure data share name</span></span>

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

### <span data-ttu-id="de0ef-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de0ef-132">-Confirm</span></span>
<span data-ttu-id="de0ef-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de0ef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de0ef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de0ef-134">-WhatIf</span></span>
<span data-ttu-id="de0ef-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de0ef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de0ef-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de0ef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de0ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0ef-137">CommonParameters</span></span>
<span data-ttu-id="de0ef-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de0ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0ef-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de0ef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0ef-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="de0ef-140">INPUTS</span></span>

### <span data-ttu-id="de0ef-141">System.String</span><span class="sxs-lookup"><span data-stu-id="de0ef-141">System.String</span></span>

### <span data-ttu-id="de0ef-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="de0ef-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="de0ef-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de0ef-143">OUTPUTS</span></span>

### <span data-ttu-id="de0ef-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de0ef-144">System.Boolean</span></span>

## <span data-ttu-id="de0ef-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="de0ef-145">NOTES</span></span>

## <span data-ttu-id="de0ef-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de0ef-146">RELATED LINKS</span></span>
