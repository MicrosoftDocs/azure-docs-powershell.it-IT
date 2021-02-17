---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205274"
---
# <span data-ttu-id="0eccc-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="0eccc-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="0eccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eccc-102">SYNOPSIS</span></span>
<span data-ttu-id="0eccc-103">Ottiene un file di nodo batch.</span><span class="sxs-lookup"><span data-stu-id="0eccc-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="0eccc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0eccc-104">SYNTAX</span></span>

### <span data-ttu-id="0eccc-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="0eccc-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccc-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="0eccc-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccc-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="0eccc-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccc-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="0eccc-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccc-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="0eccc-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0eccc-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="0eccc-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0eccc-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0eccc-111">DESCRIPTION</span></span>
<span data-ttu-id="0eccc-112">Il cmdlet **Get-AzBatchNodeFileContent** ottiene un file nodo di Azure Batch e lo salva come file o in uno stream.</span><span class="sxs-lookup"><span data-stu-id="0eccc-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="0eccc-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0eccc-113">EXAMPLES</span></span>

### <span data-ttu-id="0eccc-114">Esempio 1: Ottenere un file batch nodo associato a un'attività e salvare il file</span><span class="sxs-lookup"><span data-stu-id="0eccc-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="0eccc-115">Questo comando recupera il file nodo denominato StdOut.txt e lo salva nel percorso E:\PowerShell\StdOut.txt file nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="0eccc-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="0eccc-116">Il StdOut.txt nodo di attività è associato all'attività con ID Attività01 per il processo con ID Processo01.</span><span class="sxs-lookup"><span data-stu-id="0eccc-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="0eccc-117">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="0eccc-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0eccc-118">Esempio 2: Ottenere un file batch nodo e salvarlo in un percorso file specificato usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="0eccc-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="0eccc-119">Questo comando recupera il file nodo denominato StdErr.txt tramite il cmdlet Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="0eccc-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="0eccc-120">Il comando passa il file al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="0eccc-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0eccc-121">Il cmdlet corrente salva il file nel percorso E:\PowerShell\StdOut.txt file nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="0eccc-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="0eccc-122">Il StdOut.txt nodo di attività è associato all'attività con ID Attività02 per il processo con ID Processo02.</span><span class="sxs-lookup"><span data-stu-id="0eccc-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="0eccc-123">Esempio 3: Ottenere un file batch nodo associato a un'attività e indirizzarlo a uno stream</span><span class="sxs-lookup"><span data-stu-id="0eccc-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="0eccc-124">Il primo comando crea uno stream usando il cmdlet New-Object, quindi lo archivia nella $Stream variabile.</span><span class="sxs-lookup"><span data-stu-id="0eccc-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="0eccc-125">Il secondo comando recupera il file nodo denominato StdOut.txt'attività con ID Attività11 per il processo con ID Processo03.</span><span class="sxs-lookup"><span data-stu-id="0eccc-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="0eccc-126">Il comando indirizza il contenuto del file al flusso in $Stream.</span><span class="sxs-lookup"><span data-stu-id="0eccc-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="0eccc-127">Esempio 4: Ottenere un file nodo da un nodo di calcolo e salvarlo</span><span class="sxs-lookup"><span data-stu-id="0eccc-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="0eccc-128">Questo comando recupera il file Startup\StdOut.txt nodo dal nodo di elaborazione che contiene l'ID ComputeNode01 nel pool che contiene l'ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="0eccc-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="0eccc-129">Il comando salva il file nel percorso E:\PowerShell\StdOut.txt file nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="0eccc-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="0eccc-130">Esempio 5: Ottenere un file nodo da un nodo di calcolo e salvarlo usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="0eccc-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="0eccc-131">Questo comando recupera il file Startup\StdOut.txt nodo usando Get-AzBatchNodeFile dal nodo di calcolo che contiene l'ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="0eccc-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="0eccc-132">Il nodo di calcolo si trova nel pool con l'ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="0eccc-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="0eccc-133">Il comando passa il file nodo al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="0eccc-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="0eccc-134">Questo cmdlet salva il file nel percorso E:\PowerShell\StdOut.txt file nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="0eccc-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="0eccc-135">Esempio 6: Ottenere un file nodo da un nodo di calcolo e indirizzarlo a uno stream</span><span class="sxs-lookup"><span data-stu-id="0eccc-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="0eccc-136">Il primo comando crea uno stream usando il cmdlet New-Object, quindi lo archivia nella $Stream variabile.</span><span class="sxs-lookup"><span data-stu-id="0eccc-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="0eccc-137">Il secondo comando recupera il file del nodo denominato StdOut.txt dal nodo di calcolo con ID ComputeNode01 nel pool con l'ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="0eccc-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="0eccc-138">Il comando indirizza il contenuto del file al flusso in $Stream.</span><span class="sxs-lookup"><span data-stu-id="0eccc-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="0eccc-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eccc-139">PARAMETERS</span></span>

### <span data-ttu-id="0eccc-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0eccc-140">-BatchContext</span></span>
<span data-ttu-id="0eccc-141">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0eccc-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0eccc-142">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0eccc-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0eccc-143">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="0eccc-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0eccc-144">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="0eccc-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0eccc-145">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0eccc-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="0eccc-146">-ByteRangeEnd</span></span>
<span data-ttu-id="0eccc-147">La fine dell'intervallo di byte da scaricare.</span><span class="sxs-lookup"><span data-stu-id="0eccc-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="0eccc-148">-ByteRangeStart</span></span>
<span data-ttu-id="0eccc-149">Inizio dell'intervallo di byte da scaricare.</span><span class="sxs-lookup"><span data-stu-id="0eccc-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="0eccc-150">-ComputeNodeId</span></span>
<span data-ttu-id="0eccc-151">Specifica l'ID del nodo di calcolo che contiene il file nodo restituito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eccc-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eccc-152">-DefaultProfile</span></span>
<span data-ttu-id="0eccc-153">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0eccc-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eccc-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="0eccc-154">-DestinationPath</span></span>
<span data-ttu-id="0eccc-155">Specifica il percorso del file in cui questo cmdlet salva il file nodo.</span><span class="sxs-lookup"><span data-stu-id="0eccc-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="0eccc-156">-DestinationStream</span></span>
<span data-ttu-id="0eccc-157">Specifica lo stream in cui questo cmdlet scrive il contenuto del file nodo.</span><span class="sxs-lookup"><span data-stu-id="0eccc-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="0eccc-158">Questo cmdlet non chiude o riavvolge questo flusso.</span><span class="sxs-lookup"><span data-stu-id="0eccc-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eccc-159">-InputObject</span></span>
<span data-ttu-id="0eccc-160">Specifica il file che riceve questo cmdlet come **oggetto PSNodeFile.**</span><span class="sxs-lookup"><span data-stu-id="0eccc-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="0eccc-161">Per ottenere un oggetto file nodo, usare il cmdlet Get-AzBatchNodeFile node.</span><span class="sxs-lookup"><span data-stu-id="0eccc-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="0eccc-162">-JobId</span></span>
<span data-ttu-id="0eccc-163">Specifica l'ID del processo che contiene l'attività di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0eccc-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-164">-Path</span><span class="sxs-lookup"><span data-stu-id="0eccc-164">-Path</span></span>
<span data-ttu-id="0eccc-165">Il percorso del file nodo da scaricare.</span><span class="sxs-lookup"><span data-stu-id="0eccc-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="0eccc-166">-PoolId</span></span>
<span data-ttu-id="0eccc-167">Specifica l'ID del pool che contiene il nodo di elaborazione che contiene il file del nodo che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eccc-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="0eccc-168">-TaskId</span></span>
<span data-ttu-id="0eccc-169">Specifica l'ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0eccc-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccc-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eccc-170">CommonParameters</span></span>
<span data-ttu-id="0eccc-171">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eccc-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eccc-172">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0eccc-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eccc-173">INPUT</span><span class="sxs-lookup"><span data-stu-id="0eccc-173">INPUTS</span></span>

### <span data-ttu-id="0eccc-174">System.String</span><span class="sxs-lookup"><span data-stu-id="0eccc-174">System.String</span></span>

### <span data-ttu-id="0eccc-175">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="0eccc-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="0eccc-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0eccc-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0eccc-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0eccc-177">OUTPUTS</span></span>

### <span data-ttu-id="0eccc-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="0eccc-178">System.Void</span></span>

## <span data-ttu-id="0eccc-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="0eccc-179">NOTES</span></span>

## <span data-ttu-id="0eccc-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0eccc-180">RELATED LINKS</span></span>

[<span data-ttu-id="0eccc-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0eccc-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0eccc-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="0eccc-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="0eccc-183">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="0eccc-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
