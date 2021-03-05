---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: 38c6d45c4e49f86d3aacc2774942d15ddd50941e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974045"
---
# <span data-ttu-id="c918b-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c918b-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="c918b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c918b-102">SYNOPSIS</span></span>
<span data-ttu-id="c918b-103">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c918b-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="c918b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c918b-104">SYNTAX</span></span>

### <span data-ttu-id="c918b-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c918b-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c918b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c918b-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c918b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c918b-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c918b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c918b-108">DESCRIPTION</span></span>
<span data-ttu-id="c918b-109">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c918b-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="c918b-110">Un gruppo di sincronizzazione può essere rimosso solo quando tutti gli endpoint contenuti vengono eliminati per primi.</span><span class="sxs-lookup"><span data-stu-id="c918b-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="c918b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c918b-111">EXAMPLES</span></span>

### <span data-ttu-id="c918b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c918b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="c918b-113">Questo comando rimuove il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c918b-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="c918b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c918b-114">PARAMETERS</span></span>

### <span data-ttu-id="c918b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c918b-115">-AsJob</span></span>
<span data-ttu-id="c918b-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c918b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c918b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c918b-117">-DefaultProfile</span></span>
<span data-ttu-id="c918b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c918b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c918b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c918b-119">-Force</span></span>
<span data-ttu-id="c918b-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="c918b-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c918b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c918b-121">-InputObject</span></span>
<span data-ttu-id="c918b-122">Oggetto di input SyncGroup</span><span class="sxs-lookup"><span data-stu-id="c918b-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c918b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c918b-123">-Name</span></span>
<span data-ttu-id="c918b-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c918b-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c918b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c918b-125">-PassThru</span></span>
<span data-ttu-id="c918b-126">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c918b-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="c918b-127">Se si fornisce il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="c918b-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="c918b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c918b-128">-ResourceGroupName</span></span>
<span data-ttu-id="c918b-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c918b-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c918b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c918b-130">-ResourceId</span></span>
<span data-ttu-id="c918b-131">ID risorsa SyncGroup</span><span class="sxs-lookup"><span data-stu-id="c918b-131">SyncGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c918b-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c918b-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="c918b-133">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="c918b-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c918b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c918b-134">-Confirm</span></span>
<span data-ttu-id="c918b-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c918b-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c918b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c918b-136">-WhatIf</span></span>
<span data-ttu-id="c918b-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c918b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c918b-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c918b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c918b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c918b-139">CommonParameters</span></span>
<span data-ttu-id="c918b-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c918b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c918b-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c918b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c918b-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="c918b-142">INPUTS</span></span>

### <span data-ttu-id="c918b-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c918b-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="c918b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c918b-144">System.String</span></span>

### <span data-ttu-id="c918b-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c918b-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c918b-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c918b-146">OUTPUTS</span></span>

### <span data-ttu-id="c918b-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="c918b-147">System.Object</span></span>
## <span data-ttu-id="c918b-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="c918b-148">NOTES</span></span>

## <span data-ttu-id="c918b-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c918b-149">RELATED LINKS</span></span>
