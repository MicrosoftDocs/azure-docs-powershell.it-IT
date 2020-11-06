---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 2a147e00dba480a483b10843b17347145a1dc2a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510139"
---
# <span data-ttu-id="84d5f-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="84d5f-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="84d5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="84d5f-103">Ottiene un file RDP da un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="84d5f-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84d5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84d5f-104">SYNTAX</span></span>

### <span data-ttu-id="84d5f-105">Id_Path (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84d5f-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84d5f-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="84d5f-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84d5f-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="84d5f-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84d5f-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="84d5f-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84d5f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84d5f-109">DESCRIPTION</span></span>
<span data-ttu-id="84d5f-110">Il cmdlet **Get-AzureBatchRemoteDesktopProtocolFile** ottiene un file RDP (Remote Desktop Protocol) da un nodo COMPUTE e lo salva come file o in un flusso fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="84d5f-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="84d5f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84d5f-111">EXAMPLES</span></span>

### <span data-ttu-id="84d5f-112">Esempio 1: recuperare un file RDP da un nodo Compute specificato e salvare il file</span><span class="sxs-lookup"><span data-stu-id="84d5f-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="84d5f-113">Questo comando ottiene un file RDP dal nodo Compute che contiene l'ID ComputeNode01 nel pool che contiene l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="84d5f-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="84d5f-114">Il comando Salva il file con estensione RDP come C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="84d5f-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="84d5f-115">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="84d5f-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="84d5f-116">Esempio 2: ottenere un file RDP da un nodo COMPUTE e salvare il file usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="84d5f-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="84d5f-117">Questo comando ottiene il nodo Compute che contiene l'ID ComputeNode02 nel pool che contiene l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="84d5f-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="84d5f-118">Il comando passa il nodo Compute al cmdlet Current usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="84d5f-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="84d5f-119">Il cmdlet corrente ottiene un file con estensione RPD dal nodo COMPUTE e quindi Salva il contenuto come file denominato C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="84d5f-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="84d5f-120">Esempio 3: ottenere un file RDP da un nodo Compute specificato e indirizzarlo a un flusso</span><span class="sxs-lookup"><span data-stu-id="84d5f-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="84d5f-121">Il primo comando crea un flusso usando il cmdlet New-Object e lo archivia nella variabile $Stream.</span><span class="sxs-lookup"><span data-stu-id="84d5f-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="84d5f-122">Il secondo comando ottiene un file con estensione RDP dal nodo Compute che contiene l'ID ComputeNode03 nel pool che contiene l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="84d5f-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="84d5f-123">Il comando indirizza il contenuto del file al flusso in $Stream.</span><span class="sxs-lookup"><span data-stu-id="84d5f-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="84d5f-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84d5f-124">PARAMETERS</span></span>

### <span data-ttu-id="84d5f-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="84d5f-125">-BatchContext</span></span>
<span data-ttu-id="84d5f-126">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="84d5f-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="84d5f-127">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="84d5f-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="84d5f-128">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="84d5f-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="84d5f-129">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="84d5f-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="84d5f-130">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="84d5f-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84d5f-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="84d5f-131">-ComputeNode</span></span>
<span data-ttu-id="84d5f-132">Specifica un nodo COMPUTE, come oggetto **PSComputeNode** , a cui punta il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="84d5f-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="84d5f-133">Per ottenere un oggetto compute node, usa il cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="84d5f-133">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84d5f-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="84d5f-134">-ComputeNodeId</span></span>
<span data-ttu-id="84d5f-135">Specifica l'ID del nodo Compute a cui punta il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="84d5f-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d5f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d5f-136">-DefaultProfile</span></span>
<span data-ttu-id="84d5f-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84d5f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d5f-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="84d5f-138">-DestinationPath</span></span>
<span data-ttu-id="84d5f-139">Specifica il percorso del file in cui questo cmdlet salva il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="84d5f-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d5f-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="84d5f-140">-DestinationStream</span></span>
<span data-ttu-id="84d5f-141">Specifica il flusso in cui questo cmdlet dirige i dati RDP.</span><span class="sxs-lookup"><span data-stu-id="84d5f-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="84d5f-142">Questo cmdlet non chiude o riavvolge questo flusso.</span><span class="sxs-lookup"><span data-stu-id="84d5f-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d5f-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="84d5f-143">-PoolId</span></span>
<span data-ttu-id="84d5f-144">Specifica l'ID del pool che contiene il nodo Compute da cui questo cmdlet ottiene un file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="84d5f-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d5f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d5f-145">CommonParameters</span></span>
<span data-ttu-id="84d5f-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d5f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d5f-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84d5f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d5f-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84d5f-148">INPUTS</span></span>

### <span data-ttu-id="84d5f-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="84d5f-149">BatchAccountContext</span></span>
<span data-ttu-id="84d5f-150">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="84d5f-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="84d5f-151">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="84d5f-151">PSComputeNode</span></span>
<span data-ttu-id="84d5f-152">Il parametro ' ComputeNode ' accetta il valore di tipo ' PSComputeNode ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="84d5f-152">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="84d5f-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84d5f-153">OUTPUTS</span></span>

## <span data-ttu-id="84d5f-154">Note</span><span class="sxs-lookup"><span data-stu-id="84d5f-154">NOTES</span></span>

## <span data-ttu-id="84d5f-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84d5f-155">RELATED LINKS</span></span>

[<span data-ttu-id="84d5f-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="84d5f-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="84d5f-157">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="84d5f-157">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="84d5f-158">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="84d5f-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


