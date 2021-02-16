---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 636ceb216c7bb6aec2016bdd047a26f707108c9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177966"
---
# <span data-ttu-id="c3cf0-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c3cf0-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="c3cf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cf0-103">Modifica le proprietà di un account in un nodo di elaborazione batch.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="c3cf0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3cf0-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3cf0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3cf0-105">DESCRIPTION</span></span>
<span data-ttu-id="c3cf0-106">Il cmdlet **Set-AzBatchComputeNodeUser** modifica le proprietà di un account utente in un nodo di elaborazione batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="c3cf0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3cf0-107">EXAMPLES</span></span>

### <span data-ttu-id="c3cf0-108">Esempio 1: Aggiornare un account utente</span><span class="sxs-lookup"><span data-stu-id="c3cf0-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="c3cf0-109">Questo comando modifica l'account utente denominato PFuller nel nodo di elaborazione che ha l'ID specificato nel pool denominato ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="c3cf0-110">Il comando modifica la password e la scadenza dell'account.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="c3cf0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3cf0-111">PARAMETERS</span></span>

### <span data-ttu-id="c3cf0-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3cf0-112">-BatchContext</span></span>
<span data-ttu-id="c3cf0-113">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3cf0-114">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c3cf0-115">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c3cf0-116">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c3cf0-117">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c3cf0-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c3cf0-118">-ComputeNodeId</span></span>
<span data-ttu-id="c3cf0-119">Specifica l'ID del nodo di calcolo su cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c3cf0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cf0-120">-DefaultProfile</span></span>
<span data-ttu-id="c3cf0-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3cf0-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c3cf0-122">-ExpiryTime</span></span>
<span data-ttu-id="c3cf0-123">Specifica la scadenza per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="c3cf0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c3cf0-124">-Name</span></span>
<span data-ttu-id="c3cf0-125">Specifica il nome dell'account utente modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c3cf0-126">-Password</span><span class="sxs-lookup"><span data-stu-id="c3cf0-126">-Password</span></span>
<span data-ttu-id="c3cf0-127">Specifica la password dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="c3cf0-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c3cf0-128">-PoolId</span></span>
<span data-ttu-id="c3cf0-129">Specifica l'ID del pool che contiene il nodo di calcolo in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c3cf0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cf0-130">CommonParameters</span></span>
<span data-ttu-id="c3cf0-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cf0-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cf0-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3cf0-133">INPUTS</span></span>

### <span data-ttu-id="c3cf0-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3cf0-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c3cf0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3cf0-135">OUTPUTS</span></span>

### <span data-ttu-id="c3cf0-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="c3cf0-136">System.Void</span></span>

## <span data-ttu-id="c3cf0-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3cf0-137">NOTES</span></span>

## <span data-ttu-id="c3cf0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3cf0-138">RELATED LINKS</span></span>

[<span data-ttu-id="c3cf0-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c3cf0-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c3cf0-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c3cf0-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="c3cf0-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c3cf0-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="c3cf0-142">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="c3cf0-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
