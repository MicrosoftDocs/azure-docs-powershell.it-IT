---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 21e1848266f13fd44513ea0bce8c540b0387320a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985360"
---
# <span data-ttu-id="825f7-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="825f7-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="825f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="825f7-102">SYNOPSIS</span></span>
<span data-ttu-id="825f7-103">Ottiene un file RDP da un nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="825f7-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="825f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="825f7-104">SYNTAX</span></span>

### <span data-ttu-id="825f7-105">Id_Path (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="825f7-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="825f7-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="825f7-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="825f7-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="825f7-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="825f7-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="825f7-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="825f7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="825f7-109">DESCRIPTION</span></span>
<span data-ttu-id="825f7-110">Il cmdlet **Get-AzBatchRemoteDesktopProtocolFile** ottiene un file RDP (Remote Desktop Protocol) da un nodo di elaborazione e lo salva come file o in uno stream fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="825f7-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="825f7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="825f7-111">EXAMPLES</span></span>

### <span data-ttu-id="825f7-112">Esempio 1: Ottenere un file RDP da un nodo di elaborazione specificato e salvare il file</span><span class="sxs-lookup"><span data-stu-id="825f7-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="825f7-113">Questo comando recupera un file RDP dal nodo di elaborazione con ID ComputeNode01 nel pool che contiene l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="825f7-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="825f7-114">Il comando salva il file con estensione rdp come C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="825f7-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="825f7-115">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="825f7-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="825f7-116">Esempio 2: Ottenere un file RDP da un nodo di calcolo e salvare il file usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="825f7-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="825f7-117">Questo comando recupera il nodo di calcolo con ID ComputeNode02 nel pool con l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="825f7-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="825f7-118">Il comando passa il nodo di calcolo al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="825f7-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="825f7-119">Il cmdlet corrente recupera un file con estensione rpd dal nodo di calcolo e quindi salva il contenuto come file denominato C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="825f7-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="825f7-120">Esempio 3: Ottenere un file RDP da un nodo di elaborazione specificato e indirizzarlo a uno stream</span><span class="sxs-lookup"><span data-stu-id="825f7-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="825f7-121">Il primo comando crea uno stream usando il cmdlet New-Object, quindi lo archivia nella $Stream variabile.</span><span class="sxs-lookup"><span data-stu-id="825f7-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="825f7-122">Il secondo comando ottiene un file con estensione rdp dal nodo di elaborazione con ID ComputeNode03 nel pool con ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="825f7-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="825f7-123">Il comando indirizza il contenuto del file al flusso in $Stream.</span><span class="sxs-lookup"><span data-stu-id="825f7-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="825f7-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="825f7-124">PARAMETERS</span></span>

### <span data-ttu-id="825f7-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="825f7-125">-BatchContext</span></span>
<span data-ttu-id="825f7-126">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="825f7-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="825f7-127">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="825f7-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="825f7-128">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="825f7-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="825f7-129">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="825f7-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="825f7-130">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="825f7-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="825f7-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="825f7-131">-ComputeNode</span></span>
<span data-ttu-id="825f7-132">Specifica un nodo di calcolo, come oggetto **PSComputeNode,** a cui punta il file rdp.</span><span class="sxs-lookup"><span data-stu-id="825f7-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="825f7-133">Per ottenere un oggetto nodo di calcolo, usare il cmdlet Get-AzBatchComputeNode di calcolo.</span><span class="sxs-lookup"><span data-stu-id="825f7-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="825f7-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="825f7-134">-ComputeNodeId</span></span>
<span data-ttu-id="825f7-135">Specifica l'ID del nodo di calcolo a cui punta il file rdp.</span><span class="sxs-lookup"><span data-stu-id="825f7-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="825f7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825f7-136">-DefaultProfile</span></span>
<span data-ttu-id="825f7-137">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="825f7-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="825f7-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="825f7-138">-DestinationPath</span></span>
<span data-ttu-id="825f7-139">Specifica il percorso del file in cui questo cmdlet salva il file con estensione rdp.</span><span class="sxs-lookup"><span data-stu-id="825f7-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825f7-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="825f7-140">-DestinationStream</span></span>
<span data-ttu-id="825f7-141">Specifica lo stream in cui questo cmdlet indirizza i dati RDP.</span><span class="sxs-lookup"><span data-stu-id="825f7-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="825f7-142">Questo cmdlet non chiude o riavvolge questo flusso.</span><span class="sxs-lookup"><span data-stu-id="825f7-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825f7-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="825f7-143">-PoolId</span></span>
<span data-ttu-id="825f7-144">Specifica l'ID del pool che contiene il nodo di calcolo da cui questo cmdlet ottiene un file con estensione rdp.</span><span class="sxs-lookup"><span data-stu-id="825f7-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="825f7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825f7-145">CommonParameters</span></span>
<span data-ttu-id="825f7-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="825f7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825f7-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="825f7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825f7-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="825f7-148">INPUTS</span></span>

### <span data-ttu-id="825f7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="825f7-149">System.String</span></span>

### <span data-ttu-id="825f7-150">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="825f7-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="825f7-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="825f7-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="825f7-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="825f7-152">OUTPUTS</span></span>

### <span data-ttu-id="825f7-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="825f7-153">System.Void</span></span>

## <span data-ttu-id="825f7-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="825f7-154">NOTES</span></span>

## <span data-ttu-id="825f7-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="825f7-155">RELATED LINKS</span></span>

[<span data-ttu-id="825f7-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="825f7-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="825f7-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="825f7-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="825f7-158">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="825f7-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
