---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517060"
---
# <span data-ttu-id="45260-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="45260-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="45260-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45260-102">SYNOPSIS</span></span>
<span data-ttu-id="45260-103">Crea un account utente in un nodo di calcolo batch.</span><span class="sxs-lookup"><span data-stu-id="45260-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45260-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45260-104">SYNTAX</span></span>

### <span data-ttu-id="45260-105">ID</span><span class="sxs-lookup"><span data-stu-id="45260-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45260-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="45260-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45260-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45260-107">DESCRIPTION</span></span>
<span data-ttu-id="45260-108">Il cmdlet **New-AzureBatchComputeNodeUser** crea un account utente in un nodo di calcolo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="45260-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="45260-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45260-109">EXAMPLES</span></span>

### <span data-ttu-id="45260-110">Esempio 1: creare un account utente con credenziali amministrative</span><span class="sxs-lookup"><span data-stu-id="45260-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="45260-111">Questo comando crea un account utente nel nodo Compute che contiene l'ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="45260-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="45260-112">Il nodo è nel pool che contiene l'ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="45260-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="45260-113">Il nome utente è TestUser, la password è la password, l'account scade in sette giorni e l'account ha le credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="45260-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="45260-114">Esempio 2: creare un account utente in un nodo Compute tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="45260-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="45260-115">Questo comando ottiene il nodo Compute denominato ComputeNode01 usando il cmdlet **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="45260-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="45260-116">Il nodo è nel pool che contiene l'ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="45260-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="45260-117">Il comando passa il nodo Compute al cmdlet Current usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="45260-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="45260-118">Il comando crea un account utente con il nome utente TestUserand password.</span><span class="sxs-lookup"><span data-stu-id="45260-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="45260-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45260-119">PARAMETERS</span></span>

### <span data-ttu-id="45260-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="45260-120">-BatchContext</span></span>
<span data-ttu-id="45260-121">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="45260-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="45260-122">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="45260-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="45260-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="45260-123">-ComputeNode</span></span>
<span data-ttu-id="45260-124">Specifica il nodo COMPUTE, come oggetto **PSComputeNode** , in cui questo cmdlet crea un account utente.</span><span class="sxs-lookup"><span data-stu-id="45260-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45260-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="45260-125">-ComputeNodeId</span></span>
<span data-ttu-id="45260-126">Specifica l'ID del nodo COMPUTE in cui questo cmdlet crea un account utente.</span><span class="sxs-lookup"><span data-stu-id="45260-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45260-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="45260-127">-ExpiryTime</span></span>
<span data-ttu-id="45260-128">Specifica l'ora di scadenza per il nuovo account utente.</span><span class="sxs-lookup"><span data-stu-id="45260-128">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="45260-129">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="45260-129">-IsAdmin</span></span>
<span data-ttu-id="45260-130">Indica che il cmdlet crea un account utente con credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="45260-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="45260-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="45260-131">-Name</span></span>
<span data-ttu-id="45260-132">Specifica il nome del nuovo account di Windows locale.</span><span class="sxs-lookup"><span data-stu-id="45260-132">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45260-133">-Password</span><span class="sxs-lookup"><span data-stu-id="45260-133">-Password</span></span>
<span data-ttu-id="45260-134">Specifica la password dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="45260-134">Specifies the user account password.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45260-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="45260-135">-PoolId</span></span>
<span data-ttu-id="45260-136">Specifica l'ID del pool che contiene il nodo COMPUTE in cui creare l'account utente.</span><span class="sxs-lookup"><span data-stu-id="45260-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45260-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45260-137">-DefaultProfile</span></span>
<span data-ttu-id="45260-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45260-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45260-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45260-139">CommonParameters</span></span>
<span data-ttu-id="45260-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45260-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45260-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45260-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45260-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45260-142">INPUTS</span></span>

### <span data-ttu-id="45260-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="45260-143">BatchAccountContext</span></span>
<span data-ttu-id="45260-144">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="45260-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="45260-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="45260-145">PSComputeNode</span></span>
<span data-ttu-id="45260-146">Il parametro ' ComputeNode ' accetta il valore di tipo ' PSComputeNode ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="45260-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="45260-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45260-147">OUTPUTS</span></span>

## <span data-ttu-id="45260-148">Note</span><span class="sxs-lookup"><span data-stu-id="45260-148">NOTES</span></span>

## <span data-ttu-id="45260-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45260-149">RELATED LINKS</span></span>

[<span data-ttu-id="45260-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="45260-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="45260-151">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="45260-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="45260-152">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="45260-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="45260-153">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="45260-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


