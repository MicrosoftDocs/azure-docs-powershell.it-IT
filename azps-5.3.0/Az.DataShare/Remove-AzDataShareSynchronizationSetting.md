---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377100"
---
# <span data-ttu-id="3d5bf-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="3d5bf-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="3d5bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5bf-103">rimuove un'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="3d5bf-103">removes a synchronization setting</span></span>

## <span data-ttu-id="3d5bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d5bf-104">SYNTAX</span></span>

### <span data-ttu-id="3d5bf-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d5bf-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d5bf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d5bf-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d5bf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d5bf-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d5bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d5bf-108">DESCRIPTION</span></span>
<span data-ttu-id="3d5bf-109">Il cmdlet **Remove-AzDataShareSynchronizationSetting** rimuove un'impostazione di sincronizzazione DataShare</span><span class="sxs-lookup"><span data-stu-id="3d5bf-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="3d5bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d5bf-110">EXAMPLES</span></span>

### <span data-ttu-id="3d5bf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d5bf-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3d5bf-112">Questo comando rimuove un'impostazione di sincronizzazione denominata AdsShareSynchronizationSetting da Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="3d5bf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d5bf-113">PARAMETERS</span></span>

### <span data-ttu-id="3d5bf-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3d5bf-114">-AccountName</span></span>
<span data-ttu-id="3d5bf-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="3d5bf-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="3d5bf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d5bf-116">-AsJob</span></span>
<span data-ttu-id="3d5bf-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="3d5bf-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="3d5bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5bf-118">-DefaultProfile</span></span>
<span data-ttu-id="3d5bf-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d5bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d5bf-120">-InputObject</span></span>
<span data-ttu-id="3d5bf-121">Impostazione di sincronizzazione della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="3d5bf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d5bf-122">-Name</span></span>
<span data-ttu-id="3d5bf-123">Nome impostazione sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="3d5bf-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="3d5bf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d5bf-124">-PassThru</span></span>
<span data-ttu-id="3d5bf-125">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="3d5bf-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="3d5bf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d5bf-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d5bf-127">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="3d5bf-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3d5bf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d5bf-128">-ResourceId</span></span>
<span data-ttu-id="3d5bf-129">ID risorsa dell'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="3d5bf-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="3d5bf-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3d5bf-130">-ShareName</span></span>
<span data-ttu-id="3d5bf-131">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="3d5bf-131">Azure data share name</span></span>

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

### <span data-ttu-id="3d5bf-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3d5bf-132">-Confirm</span></span>
<span data-ttu-id="3d5bf-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d5bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d5bf-134">-WhatIf</span></span>
<span data-ttu-id="3d5bf-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d5bf-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d5bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5bf-137">CommonParameters</span></span>
<span data-ttu-id="3d5bf-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5bf-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d5bf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5bf-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d5bf-140">INPUTS</span></span>

### <span data-ttu-id="3d5bf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3d5bf-141">System.String</span></span>

### <span data-ttu-id="3d5bf-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="3d5bf-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="3d5bf-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d5bf-143">OUTPUTS</span></span>

### <span data-ttu-id="3d5bf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d5bf-144">System.Boolean</span></span>

## <span data-ttu-id="3d5bf-145">Note</span><span class="sxs-lookup"><span data-stu-id="3d5bf-145">NOTES</span></span>

## <span data-ttu-id="3d5bf-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d5bf-146">RELATED LINKS</span></span>
