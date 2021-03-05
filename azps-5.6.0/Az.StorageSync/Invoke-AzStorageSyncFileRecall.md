---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 4da44d6ecff7dbf6de9c0fb20f74988688e9826d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002190"
---
# <span data-ttu-id="24795-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="24795-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="24795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24795-102">SYNOPSIS</span></span>
<span data-ttu-id="24795-103">Questo comando richiama tutti i file a più livelli nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="24795-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="24795-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24795-104">SYNTAX</span></span>

### <span data-ttu-id="24795-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="24795-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24795-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24795-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24795-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24795-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24795-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="24795-108">DESCRIPTION</span></span>
<span data-ttu-id="24795-109">Quando il livello del cloud è abilitato su un endpoint del server (una posizione specifica su un server registrato), questo comando può essere usato per richiamare tutti i file a più livelli sul disco locale.</span><span class="sxs-lookup"><span data-stu-id="24795-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="24795-110">È consigliabile disabilitare il livelli del cloud nell'endpoint del server prima di iniziare il richiamo.</span><span class="sxs-lookup"><span data-stu-id="24795-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="24795-111">Se il tiering è ancora in corso, il richiamo potrebbe comportare la visualizzazione a più livelli di altri file, che non vengono visualizzati per raggiungere l'obiettivo desiderato di tutto il contenuto che si trova sul disco locale.</span><span class="sxs-lookup"><span data-stu-id="24795-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="24795-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24795-112">EXAMPLES</span></span>

### <span data-ttu-id="24795-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="24795-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="24795-114">Questo comando richiama in modo ricorsivo tutti i file a più livelli che si trovano nel percorso radice dell'endpoint del server specificato.</span><span class="sxs-lookup"><span data-stu-id="24795-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="24795-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24795-115">PARAMETERS</span></span>

### <span data-ttu-id="24795-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24795-116">-AsJob</span></span>
<span data-ttu-id="24795-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="24795-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24795-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24795-118">-DefaultProfile</span></span>
<span data-ttu-id="24795-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24795-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24795-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24795-120">-InputObject</span></span>
<span data-ttu-id="24795-121">Oggetto SyncGroup, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="24795-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24795-122">-Name</span><span class="sxs-lookup"><span data-stu-id="24795-122">-Name</span></span>
<span data-ttu-id="24795-123">Nome di ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="24795-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24795-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24795-124">-PassThru</span></span>
<span data-ttu-id="24795-125">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="24795-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="24795-126">Se si fornisce il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="24795-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="24795-127">-Pattern</span><span class="sxs-lookup"><span data-stu-id="24795-127">-Pattern</span></span>
<span data-ttu-id="24795-128">Schema del nome file</span><span class="sxs-lookup"><span data-stu-id="24795-128">Pattern of the file name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24795-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="24795-129">-RecallPath</span></span>
<span data-ttu-id="24795-130">Richiama il percorso che deve essere richiamato.</span><span class="sxs-lookup"><span data-stu-id="24795-130">Recall path which need to be recalled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24795-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24795-131">-ResourceGroupName</span></span>
<span data-ttu-id="24795-132">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="24795-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="24795-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24795-133">-ResourceId</span></span>
<span data-ttu-id="24795-134">ID risorsa ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="24795-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="24795-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="24795-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="24795-136">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="24795-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="24795-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="24795-137">-SyncGroupName</span></span>
<span data-ttu-id="24795-138">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="24795-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24795-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24795-139">-Confirm</span></span>
<span data-ttu-id="24795-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24795-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24795-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24795-141">-WhatIf</span></span>
<span data-ttu-id="24795-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24795-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24795-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24795-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24795-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24795-144">CommonParameters</span></span>
<span data-ttu-id="24795-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24795-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24795-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24795-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24795-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="24795-147">INPUTS</span></span>

### <span data-ttu-id="24795-148">System.String</span><span class="sxs-lookup"><span data-stu-id="24795-148">System.String</span></span>

### <span data-ttu-id="24795-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="24795-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="24795-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24795-150">OUTPUTS</span></span>

### <span data-ttu-id="24795-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24795-151">System.Boolean</span></span>

## <span data-ttu-id="24795-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="24795-152">NOTES</span></span>

## <span data-ttu-id="24795-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24795-153">RELATED LINKS</span></span>
