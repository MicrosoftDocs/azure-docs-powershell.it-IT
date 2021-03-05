---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: aaf020d61941057dd0dabac849adb37197e02882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987011"
---
# <span data-ttu-id="55cbb-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="55cbb-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="55cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="55cbb-103">Crea un account utente in un nodo di elaborazione batch.</span><span class="sxs-lookup"><span data-stu-id="55cbb-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="55cbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55cbb-104">SYNTAX</span></span>

### <span data-ttu-id="55cbb-105">ID</span><span class="sxs-lookup"><span data-stu-id="55cbb-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55cbb-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="55cbb-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55cbb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="55cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="55cbb-108">Il cmdlet **New-AzBatchComputeNodeUser** crea un account utente in un nodo di elaborazione batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="55cbb-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="55cbb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55cbb-109">EXAMPLES</span></span>

### <span data-ttu-id="55cbb-110">Esempio 1: Creare un account utente con credenziali di amministratore</span><span class="sxs-lookup"><span data-stu-id="55cbb-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="55cbb-111">Questo comando crea un account utente nel nodo di elaborazione con ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="55cbb-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="55cbb-112">Il nodo si trova nel pool con ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="55cbb-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="55cbb-113">Il nome utente è TestUser, la password è Password, l'account scade tra sette giorni e l'account ha credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="55cbb-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="55cbb-114">Esempio 2: Creare un account utente in un nodo di calcolo usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="55cbb-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="55cbb-115">Questo comando recupera il nodo di elaborazione denominato ComputeNode01 usando il cmdlet **Get-AzBatchComputeNode.**</span><span class="sxs-lookup"><span data-stu-id="55cbb-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="55cbb-116">Il nodo si trova nel pool con ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="55cbb-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="55cbb-117">Il comando passa il nodo di calcolo al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="55cbb-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="55cbb-118">Il comando crea un account utente con il nome utente TestUser e la password Password.</span><span class="sxs-lookup"><span data-stu-id="55cbb-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="55cbb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55cbb-119">PARAMETERS</span></span>

### <span data-ttu-id="55cbb-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="55cbb-120">-BatchContext</span></span>
<span data-ttu-id="55cbb-121">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="55cbb-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="55cbb-122">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="55cbb-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="55cbb-123">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="55cbb-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="55cbb-124">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="55cbb-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="55cbb-125">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="55cbb-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="55cbb-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="55cbb-126">-ComputeNode</span></span>
<span data-ttu-id="55cbb-127">Specifica il nodo di calcolo, come oggetto **PSComputeNode,** in cui questo cmdlet crea un account utente.</span><span class="sxs-lookup"><span data-stu-id="55cbb-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="55cbb-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="55cbb-128">-ComputeNodeId</span></span>
<span data-ttu-id="55cbb-129">Specifica l'ID del nodo di calcolo in cui questo cmdlet crea un account utente.</span><span class="sxs-lookup"><span data-stu-id="55cbb-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="55cbb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55cbb-130">-DefaultProfile</span></span>
<span data-ttu-id="55cbb-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55cbb-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55cbb-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="55cbb-132">-ExpiryTime</span></span>
<span data-ttu-id="55cbb-133">Specifica la scadenza del nuovo account utente.</span><span class="sxs-lookup"><span data-stu-id="55cbb-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="55cbb-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="55cbb-134">-IsAdmin</span></span>
<span data-ttu-id="55cbb-135">Indica che il cmdlet crea un account utente con credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="55cbb-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="55cbb-136">-Name</span><span class="sxs-lookup"><span data-stu-id="55cbb-136">-Name</span></span>
<span data-ttu-id="55cbb-137">Specifica il nome del nuovo account di Windows locale.</span><span class="sxs-lookup"><span data-stu-id="55cbb-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="55cbb-138">-Password</span><span class="sxs-lookup"><span data-stu-id="55cbb-138">-Password</span></span>
<span data-ttu-id="55cbb-139">Specifica la password dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="55cbb-139">Specifies the user account password.</span></span>

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

### <span data-ttu-id="55cbb-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="55cbb-140">-PoolId</span></span>
<span data-ttu-id="55cbb-141">Specifica l'ID del pool che contiene il nodo di calcolo in cui creare l'account utente.</span><span class="sxs-lookup"><span data-stu-id="55cbb-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="55cbb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55cbb-142">CommonParameters</span></span>
<span data-ttu-id="55cbb-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55cbb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55cbb-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="55cbb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55cbb-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="55cbb-145">INPUTS</span></span>

### <span data-ttu-id="55cbb-146">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="55cbb-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="55cbb-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="55cbb-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="55cbb-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55cbb-148">OUTPUTS</span></span>

### <span data-ttu-id="55cbb-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="55cbb-149">System.Void</span></span>

## <span data-ttu-id="55cbb-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="55cbb-150">NOTES</span></span>

## <span data-ttu-id="55cbb-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55cbb-151">RELATED LINKS</span></span>

[<span data-ttu-id="55cbb-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="55cbb-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="55cbb-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="55cbb-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="55cbb-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="55cbb-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="55cbb-155">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="55cbb-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
