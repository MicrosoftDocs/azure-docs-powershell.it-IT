---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 69b1ef139569a4a89c5c0f11d54ddbf5407fa653
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685320"
---
# <span data-ttu-id="ad769-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ad769-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="ad769-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad769-102">SYNOPSIS</span></span>
<span data-ttu-id="ad769-103">Crea un account utente in un nodo di calcolo batch.</span><span class="sxs-lookup"><span data-stu-id="ad769-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="ad769-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad769-104">SYNTAX</span></span>

### <span data-ttu-id="ad769-105">ID</span><span class="sxs-lookup"><span data-stu-id="ad769-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad769-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ad769-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad769-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad769-107">DESCRIPTION</span></span>
<span data-ttu-id="ad769-108">Il cmdlet **New-AzBatchComputeNodeUser** crea un account utente in un nodo di calcolo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="ad769-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="ad769-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad769-109">EXAMPLES</span></span>

### <span data-ttu-id="ad769-110">Esempio 1: creare un account utente con credenziali amministrative</span><span class="sxs-lookup"><span data-stu-id="ad769-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="ad769-111">Questo comando crea un account utente nel nodo Compute che contiene l'ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="ad769-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="ad769-112">Il nodo è nel pool che contiene l'ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="ad769-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="ad769-113">Il nome utente è TestUser, la password è la password, l'account scade in sette giorni e l'account ha le credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="ad769-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="ad769-114">Esempio 2: creare un account utente in un nodo Compute tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="ad769-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="ad769-115">Questo comando ottiene il nodo Compute denominato ComputeNode01 usando il cmdlet **Get-AzBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="ad769-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="ad769-116">Il nodo è nel pool che contiene l'ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="ad769-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="ad769-117">Il comando passa il nodo Compute al cmdlet Current usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad769-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ad769-118">Il comando crea un account utente con il nome utente TestUserand password.</span><span class="sxs-lookup"><span data-stu-id="ad769-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="ad769-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad769-119">PARAMETERS</span></span>

### <span data-ttu-id="ad769-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ad769-120">-BatchContext</span></span>
<span data-ttu-id="ad769-121">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="ad769-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ad769-122">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="ad769-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ad769-123">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="ad769-123">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ad769-124">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ad769-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ad769-125">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ad769-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ad769-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad769-126">-ComputeNode</span></span>
<span data-ttu-id="ad769-127">Specifica il nodo COMPUTE, come oggetto **PSComputeNode** , in cui questo cmdlet crea un account utente.</span><span class="sxs-lookup"><span data-stu-id="ad769-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="ad769-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ad769-128">-ComputeNodeId</span></span>
<span data-ttu-id="ad769-129">Specifica l'ID del nodo COMPUTE in cui questo cmdlet crea un account utente.</span><span class="sxs-lookup"><span data-stu-id="ad769-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="ad769-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad769-130">-DefaultProfile</span></span>
<span data-ttu-id="ad769-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad769-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad769-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ad769-132">-ExpiryTime</span></span>
<span data-ttu-id="ad769-133">Specifica l'ora di scadenza per il nuovo account utente.</span><span class="sxs-lookup"><span data-stu-id="ad769-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="ad769-134">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="ad769-134">-IsAdmin</span></span>
<span data-ttu-id="ad769-135">Indica che il cmdlet crea un account utente con credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="ad769-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="ad769-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad769-136">-Name</span></span>
<span data-ttu-id="ad769-137">Specifica il nome del nuovo account di Windows locale.</span><span class="sxs-lookup"><span data-stu-id="ad769-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="ad769-138">-Password</span><span class="sxs-lookup"><span data-stu-id="ad769-138">-Password</span></span>
<span data-ttu-id="ad769-139">Specifica la password dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="ad769-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad769-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ad769-140">-PoolId</span></span>
<span data-ttu-id="ad769-141">Specifica l'ID del pool che contiene il nodo COMPUTE in cui creare l'account utente.</span><span class="sxs-lookup"><span data-stu-id="ad769-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="ad769-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad769-142">CommonParameters</span></span>
<span data-ttu-id="ad769-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad769-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad769-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad769-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad769-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad769-145">INPUTS</span></span>

### <span data-ttu-id="ad769-146">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad769-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ad769-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ad769-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ad769-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad769-148">OUTPUTS</span></span>

### <span data-ttu-id="ad769-149">System. void</span><span class="sxs-lookup"><span data-stu-id="ad769-149">System.Void</span></span>

## <span data-ttu-id="ad769-150">Note</span><span class="sxs-lookup"><span data-stu-id="ad769-150">NOTES</span></span>

## <span data-ttu-id="ad769-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad769-151">RELATED LINKS</span></span>

[<span data-ttu-id="ad769-152">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ad769-152">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ad769-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad769-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ad769-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ad769-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="ad769-155">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="ad769-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

