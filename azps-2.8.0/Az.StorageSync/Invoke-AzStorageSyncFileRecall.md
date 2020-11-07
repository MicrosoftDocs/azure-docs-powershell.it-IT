---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 06eb3942a5320ff7c5c8bb3d089ecad2da912edb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858302"
---
# <span data-ttu-id="ba787-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="ba787-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="ba787-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba787-102">SYNOPSIS</span></span>
<span data-ttu-id="ba787-103">Questo comando richiama tutti i file di livello sul disco locale.</span><span class="sxs-lookup"><span data-stu-id="ba787-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="ba787-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba787-104">SYNTAX</span></span>

### <span data-ttu-id="ba787-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba787-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba787-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba787-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba787-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba787-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba787-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba787-108">DESCRIPTION</span></span>
<span data-ttu-id="ba787-109">Quando il livello cloud è abilitato in un endpoint server (una posizione specifica in un server registrato), questo comando può essere usato per richiamare tutti i file a più livelli nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="ba787-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="ba787-110">È consigliabile disabilitare il livello cloud nell'endpoint del server prima di iniziare il richiamo.</span><span class="sxs-lookup"><span data-stu-id="ba787-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="ba787-111">Se il livello di livelli è ancora attivo, il richiamo potrebbe portare ad altri file che ottengono livelli che non riescono a raggiungere l'obiettivo desiderato di tutto il contenuto che risiede nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="ba787-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="ba787-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba787-112">EXAMPLES</span></span>

### <span data-ttu-id="ba787-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba787-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="ba787-114">Questo comando richiama ricorsivamente tutti i file a più livelli che si trovano sotto il percorso radice dell'endpoint del server specificato.</span><span class="sxs-lookup"><span data-stu-id="ba787-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="ba787-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba787-115">PARAMETERS</span></span>

### <span data-ttu-id="ba787-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba787-116">-AsJob</span></span>
<span data-ttu-id="ba787-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ba787-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba787-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba787-118">-DefaultProfile</span></span>
<span data-ttu-id="ba787-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba787-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba787-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba787-120">-InputObject</span></span>
<span data-ttu-id="ba787-121">Oggetto SyncGroup, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="ba787-121">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ba787-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba787-122">-Name</span></span>
<span data-ttu-id="ba787-123">Nome della ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ba787-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="ba787-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba787-124">-PassThru</span></span>
<span data-ttu-id="ba787-125">In esecuzione normale, questo cmdlet non restituisce alcun valore per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ba787-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="ba787-126">Se fornisci il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="ba787-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="ba787-127">-Pattern</span><span class="sxs-lookup"><span data-stu-id="ba787-127">-Pattern</span></span>
<span data-ttu-id="ba787-128">Modello del nome file</span><span class="sxs-lookup"><span data-stu-id="ba787-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="ba787-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="ba787-129">-RecallPath</span></span>
<span data-ttu-id="ba787-130">Richiamare il percorso di richiamo che è necessario richiamare.</span><span class="sxs-lookup"><span data-stu-id="ba787-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="ba787-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba787-131">-ResourceGroupName</span></span>
<span data-ttu-id="ba787-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba787-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba787-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba787-133">-ResourceId</span></span>
<span data-ttu-id="ba787-134">ID risorsa ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba787-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="ba787-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ba787-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="ba787-136">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ba787-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ba787-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ba787-137">-SyncGroupName</span></span>
<span data-ttu-id="ba787-138">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="ba787-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ba787-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba787-139">-Confirm</span></span>
<span data-ttu-id="ba787-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba787-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba787-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba787-141">-WhatIf</span></span>
<span data-ttu-id="ba787-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba787-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba787-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba787-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba787-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba787-144">CommonParameters</span></span>
<span data-ttu-id="ba787-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba787-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba787-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba787-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba787-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba787-147">INPUTS</span></span>

### <span data-ttu-id="ba787-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ba787-148">System.String</span></span>

### <span data-ttu-id="ba787-149">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba787-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="ba787-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba787-150">OUTPUTS</span></span>

### <span data-ttu-id="ba787-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba787-151">System.Boolean</span></span>

## <span data-ttu-id="ba787-152">Note</span><span class="sxs-lookup"><span data-stu-id="ba787-152">NOTES</span></span>

## <span data-ttu-id="ba787-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba787-153">RELATED LINKS</span></span>
