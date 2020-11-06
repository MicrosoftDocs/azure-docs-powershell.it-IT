---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: c6a89a5c42daea7991711dfa0c96953856949aed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509320"
---
# <span data-ttu-id="49dd8-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="49dd8-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="49dd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="49dd8-103">Modifica le proprietà di un account in un nodo di calcolo batch.</span><span class="sxs-lookup"><span data-stu-id="49dd8-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49dd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49dd8-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49dd8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49dd8-105">DESCRIPTION</span></span>
<span data-ttu-id="49dd8-106">Il cmdlet **set-AzureBatchComputeNodeUser** modifica le proprietà di un account utente in un nodo di calcolo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="49dd8-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="49dd8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49dd8-107">EXAMPLES</span></span>

### <span data-ttu-id="49dd8-108">Esempio 1: aggiornare un account utente</span><span class="sxs-lookup"><span data-stu-id="49dd8-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="49dd8-109">Questo comando modifica l'account utente denominato PFuller nel nodo Compute che contiene l'ID specificato nel pool denominato ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="49dd8-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="49dd8-110">Il comando cambia la password dell'account e il tempo di scadenza.</span><span class="sxs-lookup"><span data-stu-id="49dd8-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="49dd8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49dd8-111">PARAMETERS</span></span>

### <span data-ttu-id="49dd8-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="49dd8-112">-BatchContext</span></span>
<span data-ttu-id="49dd8-113">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="49dd8-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="49dd8-114">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="49dd8-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="49dd8-115">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="49dd8-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="49dd8-116">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="49dd8-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="49dd8-117">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="49dd8-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="49dd8-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="49dd8-118">-ComputeNodeId</span></span>
<span data-ttu-id="49dd8-119">Specifica l'ID del nodo COMPUTE in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49dd8-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dd8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49dd8-120">-DefaultProfile</span></span>
<span data-ttu-id="49dd8-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49dd8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dd8-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="49dd8-122">-ExpiryTime</span></span>
<span data-ttu-id="49dd8-123">Specifica il tempo di scadenza per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="49dd8-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dd8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="49dd8-124">-Name</span></span>
<span data-ttu-id="49dd8-125">Specifica il nome dell'account utente che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="49dd8-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dd8-126">-Password</span><span class="sxs-lookup"><span data-stu-id="49dd8-126">-Password</span></span>
<span data-ttu-id="49dd8-127">Specifica la password per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="49dd8-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dd8-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="49dd8-128">-PoolId</span></span>
<span data-ttu-id="49dd8-129">Specifica l'ID del pool che contiene il nodo COMPUTE in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49dd8-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dd8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49dd8-130">CommonParameters</span></span>
<span data-ttu-id="49dd8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49dd8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49dd8-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49dd8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49dd8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49dd8-133">INPUTS</span></span>

### <span data-ttu-id="49dd8-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="49dd8-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="49dd8-135">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49dd8-135">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="49dd8-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49dd8-136">OUTPUTS</span></span>

### <span data-ttu-id="49dd8-137">System. void</span><span class="sxs-lookup"><span data-stu-id="49dd8-137">System.Void</span></span>

## <span data-ttu-id="49dd8-138">Note</span><span class="sxs-lookup"><span data-stu-id="49dd8-138">NOTES</span></span>

## <span data-ttu-id="49dd8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49dd8-139">RELATED LINKS</span></span>

[<span data-ttu-id="49dd8-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="49dd8-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="49dd8-141">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="49dd8-141">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="49dd8-142">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="49dd8-142">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="49dd8-143">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="49dd8-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

