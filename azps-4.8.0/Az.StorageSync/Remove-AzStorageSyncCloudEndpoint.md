---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: ae3d75b90e6e095072b8e6e6543e2f122fe4cb50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189995"
---
# <span data-ttu-id="85533-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="85533-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="85533-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85533-102">SYNOPSIS</span></span>
<span data-ttu-id="85533-103">Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="85533-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="85533-104">Senza almeno un endpoint nuvola, non è possibile sincronizzare altri endpoint del server in questo gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="85533-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="85533-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85533-105">SYNTAX</span></span>

### <span data-ttu-id="85533-106">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85533-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85533-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85533-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85533-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85533-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85533-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85533-109">DESCRIPTION</span></span>
<span data-ttu-id="85533-110">Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="85533-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="85533-111">Il file di Azure condivide i riferimenti all'endpoint cloud rimane intatto da questo processo.</span><span class="sxs-lookup"><span data-stu-id="85533-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="85533-112">Questo comando è previsto solo per la disattivazione.</span><span class="sxs-lookup"><span data-stu-id="85533-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="85533-113">La rimozione di un endpoint cloud è un'operazione distruttiva.</span><span class="sxs-lookup"><span data-stu-id="85533-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="85533-114">Gli endpoint del server non possono essere sincronizzati senza almeno un endpoint cloud presente.</span><span class="sxs-lookup"><span data-stu-id="85533-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="85533-115">Questa operazione non deve essere eseguita per risolvere i problemi di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="85533-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="85533-116">Se questa condivisione di file Azure viene aggiunta di nuovo allo stesso gruppo di sincronizzazione, come endpoint cloud, può portare a file di conflitto e ad altre conseguenze impreviste.</span><span class="sxs-lookup"><span data-stu-id="85533-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="85533-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85533-117">EXAMPLES</span></span>

### <span data-ttu-id="85533-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85533-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="85533-119">Questo comando rimuoverà l'endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="85533-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="85533-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85533-120">PARAMETERS</span></span>

### <span data-ttu-id="85533-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85533-121">-AsJob</span></span>
<span data-ttu-id="85533-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="85533-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85533-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85533-123">-DefaultProfile</span></span>
<span data-ttu-id="85533-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85533-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85533-125">-Force</span><span class="sxs-lookup"><span data-stu-id="85533-125">-Force</span></span>
<span data-ttu-id="85533-126">Forza di fornitura per ignorare la conferma di questo comando.</span><span class="sxs-lookup"><span data-stu-id="85533-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="85533-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85533-127">-InputObject</span></span>
<span data-ttu-id="85533-128">Oggetto di input CloudEndpoint, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="85533-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="85533-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="85533-129">-Name</span></span>
<span data-ttu-id="85533-130">Nome della CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="85533-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="85533-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85533-131">-PassThru</span></span>
<span data-ttu-id="85533-132">In esecuzione normale, questo cmdlet non restituisce alcun valore per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="85533-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="85533-133">Se fornisci il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="85533-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="85533-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85533-134">-ResourceGroupName</span></span>
<span data-ttu-id="85533-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85533-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="85533-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85533-136">-ResourceId</span></span>
<span data-ttu-id="85533-137">ID risorsa CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="85533-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="85533-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="85533-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="85533-139">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="85533-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="85533-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="85533-140">-SyncGroupName</span></span>
<span data-ttu-id="85533-141">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="85533-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="85533-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85533-142">-Confirm</span></span>
<span data-ttu-id="85533-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85533-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85533-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85533-144">-WhatIf</span></span>
<span data-ttu-id="85533-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85533-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85533-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85533-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85533-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85533-147">CommonParameters</span></span>
<span data-ttu-id="85533-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85533-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85533-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85533-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85533-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85533-150">INPUTS</span></span>

### <span data-ttu-id="85533-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="85533-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="85533-152">System. String</span><span class="sxs-lookup"><span data-stu-id="85533-152">System.String</span></span>

## <span data-ttu-id="85533-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85533-153">OUTPUTS</span></span>

### <span data-ttu-id="85533-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="85533-154">System.Object</span></span>
## <span data-ttu-id="85533-155">Note</span><span class="sxs-lookup"><span data-stu-id="85533-155">NOTES</span></span>

## <span data-ttu-id="85533-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85533-156">RELATED LINKS</span></span>
