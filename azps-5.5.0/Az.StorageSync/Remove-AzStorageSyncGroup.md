---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188830"
---
# <span data-ttu-id="75c38-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="75c38-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="75c38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c38-102">SYNOPSIS</span></span>
<span data-ttu-id="75c38-103">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="75c38-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="75c38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75c38-104">SYNTAX</span></span>

### <span data-ttu-id="75c38-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="75c38-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75c38-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c38-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75c38-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c38-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c38-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75c38-108">DESCRIPTION</span></span>
<span data-ttu-id="75c38-109">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="75c38-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="75c38-110">Un gruppo di sincronizzazione può essere rimosso solo quando tutti gli endpoint contenuti vengono eliminati per primi.</span><span class="sxs-lookup"><span data-stu-id="75c38-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="75c38-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75c38-111">EXAMPLES</span></span>

### <span data-ttu-id="75c38-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75c38-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="75c38-113">Questo comando rimuove il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="75c38-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="75c38-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75c38-114">PARAMETERS</span></span>

### <span data-ttu-id="75c38-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75c38-115">-AsJob</span></span>
<span data-ttu-id="75c38-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="75c38-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75c38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c38-117">-DefaultProfile</span></span>
<span data-ttu-id="75c38-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75c38-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75c38-119">-Force</span><span class="sxs-lookup"><span data-stu-id="75c38-119">-Force</span></span>
<span data-ttu-id="75c38-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="75c38-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="75c38-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75c38-121">-InputObject</span></span>
<span data-ttu-id="75c38-122">Oggetto di input SyncGroup</span><span class="sxs-lookup"><span data-stu-id="75c38-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="75c38-123">-Name</span><span class="sxs-lookup"><span data-stu-id="75c38-123">-Name</span></span>
<span data-ttu-id="75c38-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="75c38-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="75c38-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75c38-125">-PassThru</span></span>
<span data-ttu-id="75c38-126">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="75c38-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="75c38-127">Se si fornisce il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="75c38-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="75c38-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c38-128">-ResourceGroupName</span></span>
<span data-ttu-id="75c38-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="75c38-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="75c38-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75c38-130">-ResourceId</span></span>
<span data-ttu-id="75c38-131">ID risorsa SyncGroup</span><span class="sxs-lookup"><span data-stu-id="75c38-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="75c38-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="75c38-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="75c38-133">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="75c38-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="75c38-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75c38-134">-Confirm</span></span>
<span data-ttu-id="75c38-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75c38-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c38-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c38-136">-WhatIf</span></span>
<span data-ttu-id="75c38-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75c38-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75c38-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75c38-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c38-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c38-139">CommonParameters</span></span>
<span data-ttu-id="75c38-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c38-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c38-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c38-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c38-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="75c38-142">INPUTS</span></span>

### <span data-ttu-id="75c38-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="75c38-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="75c38-144">System.String</span><span class="sxs-lookup"><span data-stu-id="75c38-144">System.String</span></span>

### <span data-ttu-id="75c38-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="75c38-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="75c38-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75c38-146">OUTPUTS</span></span>

### <span data-ttu-id="75c38-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="75c38-147">System.Object</span></span>
## <span data-ttu-id="75c38-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="75c38-148">NOTES</span></span>

## <span data-ttu-id="75c38-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75c38-149">RELATED LINKS</span></span>
