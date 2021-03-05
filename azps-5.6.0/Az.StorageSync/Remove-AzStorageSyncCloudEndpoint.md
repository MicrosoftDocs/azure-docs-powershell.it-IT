---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 451df6b0608ece9888b1525388784dcee1aac334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974077"
---
# <span data-ttu-id="f69fc-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="f69fc-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="f69fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f69fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f69fc-103">Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f69fc-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="f69fc-104">Senza almeno un endpoint cloud, nessun altro endpoint server di questo gruppo di sincronizzazione può eseguire la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f69fc-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="f69fc-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f69fc-105">SYNTAX</span></span>

### <span data-ttu-id="f69fc-106">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="f69fc-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f69fc-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f69fc-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f69fc-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f69fc-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f69fc-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f69fc-109">DESCRIPTION</span></span>
<span data-ttu-id="f69fc-110">Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f69fc-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="f69fc-111">I riferimenti all'endpoint cloud condivisi da file di Azure rimangono invariati da questo processo.</span><span class="sxs-lookup"><span data-stu-id="f69fc-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="f69fc-112">Questo comando è destinato solo alla rimozione.</span><span class="sxs-lookup"><span data-stu-id="f69fc-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="f69fc-113">La rimozione di un endpoint cloud è un'operazione dannosa.</span><span class="sxs-lookup"><span data-stu-id="f69fc-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="f69fc-114">Gli endpoint server non possono eseguire la sincronizzazione senza almeno un endpoint cloud presente.</span><span class="sxs-lookup"><span data-stu-id="f69fc-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="f69fc-115">Questa operazione non deve essere eseguita per risolvere i problemi di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f69fc-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="f69fc-116">Se questa condivisione file di Azure viene aggiunta di nuovo allo stesso gruppo di sincronizzazione, come endpoint cloud, può causare file in conflitto e altre conseguenze indesiderate.</span><span class="sxs-lookup"><span data-stu-id="f69fc-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="f69fc-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f69fc-117">EXAMPLES</span></span>

### <span data-ttu-id="f69fc-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f69fc-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="f69fc-119">Questo comando rimuove l'endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="f69fc-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="f69fc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f69fc-120">PARAMETERS</span></span>

### <span data-ttu-id="f69fc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f69fc-121">-AsJob</span></span>
<span data-ttu-id="f69fc-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f69fc-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f69fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69fc-123">-DefaultProfile</span></span>
<span data-ttu-id="f69fc-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f69fc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f69fc-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f69fc-125">-Force</span></span>
<span data-ttu-id="f69fc-126">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="f69fc-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="f69fc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f69fc-127">-InputObject</span></span>
<span data-ttu-id="f69fc-128">Oggetto di input CloudEndpoint, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="f69fc-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f69fc-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f69fc-129">-Name</span></span>
<span data-ttu-id="f69fc-130">Nome di CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f69fc-130">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69fc-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f69fc-131">-PassThru</span></span>
<span data-ttu-id="f69fc-132">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f69fc-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f69fc-133">Se si fornisce il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="f69fc-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f69fc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69fc-134">-ResourceGroupName</span></span>
<span data-ttu-id="f69fc-135">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f69fc-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="f69fc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f69fc-136">-ResourceId</span></span>
<span data-ttu-id="f69fc-137">ID risorsa CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="f69fc-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="f69fc-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f69fc-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="f69fc-139">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f69fc-139">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69fc-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f69fc-140">-SyncGroupName</span></span>
<span data-ttu-id="f69fc-141">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f69fc-141">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69fc-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f69fc-142">-Confirm</span></span>
<span data-ttu-id="f69fc-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f69fc-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f69fc-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f69fc-144">-WhatIf</span></span>
<span data-ttu-id="f69fc-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f69fc-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f69fc-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f69fc-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f69fc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69fc-147">CommonParameters</span></span>
<span data-ttu-id="f69fc-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69fc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69fc-149">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69fc-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69fc-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="f69fc-150">INPUTS</span></span>

### <span data-ttu-id="f69fc-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="f69fc-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="f69fc-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f69fc-152">System.String</span></span>

## <span data-ttu-id="f69fc-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f69fc-153">OUTPUTS</span></span>

### <span data-ttu-id="f69fc-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="f69fc-154">System.Object</span></span>
## <span data-ttu-id="f69fc-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="f69fc-155">NOTES</span></span>

## <span data-ttu-id="f69fc-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f69fc-156">RELATED LINKS</span></span>
