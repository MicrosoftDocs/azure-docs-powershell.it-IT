---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: ed0f21c7a3ad2105073cb81a8dff174d201f96ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974029"
---
# <span data-ttu-id="4e423-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e423-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="4e423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e423-102">SYNOPSIS</span></span>
<span data-ttu-id="4e423-103">Questo comando eliminerà l'endpoint server specificato.</span><span class="sxs-lookup"><span data-stu-id="4e423-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="4e423-104">La sincronizzazione con questa posizione verrà interrotta immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4e423-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="4e423-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e423-105">SYNTAX</span></span>

### <span data-ttu-id="4e423-106">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="4e423-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e423-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e423-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e423-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e423-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e423-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4e423-109">DESCRIPTION</span></span>
<span data-ttu-id="4e423-110">La rimozione di un endpoint server è un'operazione dannosa.</span><span class="sxs-lookup"><span data-stu-id="4e423-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="4e423-111">La sincronizzazione di questo percorso server verrà interrotta.</span><span class="sxs-lookup"><span data-stu-id="4e423-111">This server location will stop syncing.</span></span> <span data-ttu-id="4e423-112">Questa operazione non deve essere eseguita per risolvere i problemi di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4e423-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="4e423-113">Se il percorso del server (incl. i file) viene aggiunto di nuovo allo stesso gruppo di sincronizzazione di un endpoint server, possono verificarsi file in conflitto e altre conseguenze indesiderate.</span><span class="sxs-lookup"><span data-stu-id="4e423-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="4e423-114">Questo comando è destinato solo alla rimozione.</span><span class="sxs-lookup"><span data-stu-id="4e423-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="4e423-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e423-115">EXAMPLES</span></span>

### <span data-ttu-id="4e423-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e423-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="4e423-117">Questo comando rimuove l'endpoint del server.</span><span class="sxs-lookup"><span data-stu-id="4e423-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="4e423-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e423-118">PARAMETERS</span></span>

### <span data-ttu-id="4e423-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e423-119">-AsJob</span></span>
<span data-ttu-id="4e423-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4e423-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e423-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e423-121">-DefaultProfile</span></span>
<span data-ttu-id="4e423-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e423-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e423-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4e423-123">-Force</span></span>
<span data-ttu-id="4e423-124">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="4e423-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="4e423-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e423-125">-InputObject</span></span>
<span data-ttu-id="4e423-126">Oggetto di input ServerEndpoint, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="4e423-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e423-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4e423-127">-Name</span></span>
<span data-ttu-id="4e423-128">Nome di ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e423-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="4e423-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e423-129">-PassThru</span></span>
<span data-ttu-id="4e423-130">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4e423-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="4e423-131">Se si specifica il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="4e423-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="4e423-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e423-132">-ResourceGroupName</span></span>
<span data-ttu-id="4e423-133">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e423-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e423-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e423-134">-ResourceId</span></span>
<span data-ttu-id="4e423-135">ID risorsa ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e423-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4e423-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4e423-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="4e423-137">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4e423-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4e423-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4e423-138">-SyncGroupName</span></span>
<span data-ttu-id="4e423-139">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4e423-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4e423-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e423-140">-Confirm</span></span>
<span data-ttu-id="4e423-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e423-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e423-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e423-142">-WhatIf</span></span>
<span data-ttu-id="4e423-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e423-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e423-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e423-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e423-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e423-145">CommonParameters</span></span>
<span data-ttu-id="4e423-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e423-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e423-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e423-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e423-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="4e423-148">INPUTS</span></span>

### <span data-ttu-id="4e423-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e423-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="4e423-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4e423-150">System.String</span></span>

## <span data-ttu-id="4e423-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e423-151">OUTPUTS</span></span>

### <span data-ttu-id="4e423-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="4e423-152">System.Object</span></span>
## <span data-ttu-id="4e423-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="4e423-153">NOTES</span></span>

## <span data-ttu-id="4e423-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e423-154">RELATED LINKS</span></span>
