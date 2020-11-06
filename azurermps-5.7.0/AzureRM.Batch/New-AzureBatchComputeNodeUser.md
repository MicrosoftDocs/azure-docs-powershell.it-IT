---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 3e52b2f3c9bddb2039b87b373d0963d51827f293
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516919"
---
# <span data-ttu-id="7a047-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7a047-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="7a047-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a047-102">SYNOPSIS</span></span>
<span data-ttu-id="7a047-103">Crea un account utente in un nodo di calcolo batch.</span><span class="sxs-lookup"><span data-stu-id="7a047-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a047-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a047-104">SYNTAX</span></span>

### <span data-ttu-id="7a047-105">ID</span><span class="sxs-lookup"><span data-stu-id="7a047-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String>
 -Password <SecureString> [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a047-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="7a047-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a047-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a047-107">DESCRIPTION</span></span>
<span data-ttu-id="7a047-108">Il cmdlet **New-AzureBatchComputeNodeUser** crea un account utente in un nodo di calcolo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="7a047-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="7a047-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a047-109">EXAMPLES</span></span>

### <span data-ttu-id="7a047-110">Esempio 1: creare un account utente con credenziali amministrative</span><span class="sxs-lookup"><span data-stu-id="7a047-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="7a047-111">Questo comando crea un account utente nel nodo Compute che contiene l'ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="7a047-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="7a047-112">Il nodo è nel pool che contiene l'ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="7a047-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="7a047-113">Il nome utente è TestUser, la password è la password, l'account scade in sette giorni e l'account ha le credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="7a047-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="7a047-114">Esempio 2: creare un account utente in un nodo Compute tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="7a047-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="7a047-115">Questo comando ottiene il nodo Compute denominato ComputeNode01 usando il cmdlet **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="7a047-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="7a047-116">Il nodo è nel pool che contiene l'ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="7a047-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="7a047-117">Il comando passa il nodo Compute al cmdlet Current usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a047-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7a047-118">Il comando crea un account utente con il nome utente TestUserand password.</span><span class="sxs-lookup"><span data-stu-id="7a047-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="7a047-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a047-119">PARAMETERS</span></span>

### <span data-ttu-id="7a047-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7a047-120">-BatchContext</span></span>
<span data-ttu-id="7a047-121">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7a047-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7a047-122">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7a047-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7a047-123">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="7a047-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7a047-124">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7a047-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7a047-125">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7a047-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7a047-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a047-126">-ComputeNode</span></span>
<span data-ttu-id="7a047-127">Specifica il nodo COMPUTE, come oggetto **PSComputeNode** , in cui questo cmdlet crea un account utente.</span><span class="sxs-lookup"><span data-stu-id="7a047-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a047-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="7a047-128">-ComputeNodeId</span></span>
<span data-ttu-id="7a047-129">Specifica l'ID del nodo COMPUTE in cui questo cmdlet crea un account utente.</span><span class="sxs-lookup"><span data-stu-id="7a047-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a047-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a047-130">-DefaultProfile</span></span>
<span data-ttu-id="7a047-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a047-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a047-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7a047-132">-ExpiryTime</span></span>
<span data-ttu-id="7a047-133">Specifica l'ora di scadenza per il nuovo account utente.</span><span class="sxs-lookup"><span data-stu-id="7a047-133">Specifies the expiry time for the new user account.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a047-134">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="7a047-134">-IsAdmin</span></span>
<span data-ttu-id="7a047-135">Indica che il cmdlet crea un account utente con credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="7a047-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a047-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a047-136">-Name</span></span>
<span data-ttu-id="7a047-137">Specifica il nome del nuovo account di Windows locale.</span><span class="sxs-lookup"><span data-stu-id="7a047-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a047-138">-Password</span><span class="sxs-lookup"><span data-stu-id="7a047-138">-Password</span></span>
<span data-ttu-id="7a047-139">Specifica la password dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="7a047-139">Specifies the user account password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a047-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7a047-140">-PoolId</span></span>
<span data-ttu-id="7a047-141">Specifica l'ID del pool che contiene il nodo COMPUTE in cui creare l'account utente.</span><span class="sxs-lookup"><span data-stu-id="7a047-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a047-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a047-142">CommonParameters</span></span>
<span data-ttu-id="7a047-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a047-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a047-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a047-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a047-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a047-145">INPUTS</span></span>

### <span data-ttu-id="7a047-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7a047-146">BatchAccountContext</span></span>
<span data-ttu-id="7a047-147">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7a047-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="7a047-148">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a047-148">PSComputeNode</span></span>
<span data-ttu-id="7a047-149">Il parametro ' ComputeNode ' accetta il valore di tipo ' PSComputeNode ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7a047-149">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="7a047-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a047-150">OUTPUTS</span></span>

## <span data-ttu-id="7a047-151">Note</span><span class="sxs-lookup"><span data-stu-id="7a047-151">NOTES</span></span>

## <span data-ttu-id="7a047-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a047-152">RELATED LINKS</span></span>

[<span data-ttu-id="7a047-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7a047-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7a047-154">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a047-154">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="7a047-155">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7a047-155">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="7a047-156">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="7a047-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


