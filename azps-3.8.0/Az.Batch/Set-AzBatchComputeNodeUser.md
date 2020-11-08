---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: ddf0632be8ea7749b733d21beecfdb539272d6c3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030711"
---
# <span data-ttu-id="3947d-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3947d-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="3947d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3947d-102">SYNOPSIS</span></span>
<span data-ttu-id="3947d-103">Modifica le proprietà di un account in un nodo di calcolo batch.</span><span class="sxs-lookup"><span data-stu-id="3947d-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="3947d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3947d-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3947d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3947d-105">DESCRIPTION</span></span>
<span data-ttu-id="3947d-106">Il cmdlet **set-AzBatchComputeNodeUser** modifica le proprietà di un account utente in un nodo di calcolo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="3947d-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="3947d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3947d-107">EXAMPLES</span></span>

### <span data-ttu-id="3947d-108">Esempio 1: aggiornare un account utente</span><span class="sxs-lookup"><span data-stu-id="3947d-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="3947d-109">Questo comando modifica l'account utente denominato PFuller nel nodo Compute che contiene l'ID specificato nel pool denominato ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="3947d-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="3947d-110">Il comando cambia la password dell'account e il tempo di scadenza.</span><span class="sxs-lookup"><span data-stu-id="3947d-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="3947d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3947d-111">PARAMETERS</span></span>

### <span data-ttu-id="3947d-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3947d-112">-BatchContext</span></span>
<span data-ttu-id="3947d-113">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="3947d-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3947d-114">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="3947d-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3947d-115">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="3947d-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3947d-116">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3947d-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3947d-117">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3947d-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3947d-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="3947d-118">-ComputeNodeId</span></span>
<span data-ttu-id="3947d-119">Specifica l'ID del nodo COMPUTE in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3947d-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3947d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3947d-120">-DefaultProfile</span></span>
<span data-ttu-id="3947d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3947d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3947d-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3947d-122">-ExpiryTime</span></span>
<span data-ttu-id="3947d-123">Specifica il tempo di scadenza per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="3947d-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="3947d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3947d-124">-Name</span></span>
<span data-ttu-id="3947d-125">Specifica il nome dell'account utente che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3947d-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3947d-126">-Password</span><span class="sxs-lookup"><span data-stu-id="3947d-126">-Password</span></span>
<span data-ttu-id="3947d-127">Specifica la password per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="3947d-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="3947d-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3947d-128">-PoolId</span></span>
<span data-ttu-id="3947d-129">Specifica l'ID del pool che contiene il nodo COMPUTE in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3947d-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3947d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3947d-130">CommonParameters</span></span>
<span data-ttu-id="3947d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3947d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3947d-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3947d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3947d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3947d-133">INPUTS</span></span>

### <span data-ttu-id="3947d-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3947d-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3947d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3947d-135">OUTPUTS</span></span>

### <span data-ttu-id="3947d-136">System. void</span><span class="sxs-lookup"><span data-stu-id="3947d-136">System.Void</span></span>

## <span data-ttu-id="3947d-137">Note</span><span class="sxs-lookup"><span data-stu-id="3947d-137">NOTES</span></span>

## <span data-ttu-id="3947d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3947d-138">RELATED LINKS</span></span>

[<span data-ttu-id="3947d-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3947d-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3947d-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3947d-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="3947d-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3947d-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="3947d-142">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="3947d-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


