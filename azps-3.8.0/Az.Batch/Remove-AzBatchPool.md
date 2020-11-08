---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: ce2a7c6d01af33de585d4ac8adef83d03dbd33bc
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030667"
---
# <span data-ttu-id="ea819-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ea819-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="ea819-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea819-102">SYNOPSIS</span></span>
<span data-ttu-id="ea819-103">Elimina il pool di batch specificato.</span><span class="sxs-lookup"><span data-stu-id="ea819-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="ea819-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea819-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea819-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea819-105">DESCRIPTION</span></span>
<span data-ttu-id="ea819-106">Il cmdlet **Remove-AzBatchPool** Elimina il pool di batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="ea819-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="ea819-107">Viene richiesto di confermare a meno che non si usi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="ea819-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="ea819-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea819-108">EXAMPLES</span></span>

### <span data-ttu-id="ea819-109">Esempio 1: eliminare un pool di batch per ID pool</span><span class="sxs-lookup"><span data-stu-id="ea819-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="ea819-110">Questo comando Elimina il pool con ID pool.</span><span class="sxs-lookup"><span data-stu-id="ea819-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="ea819-111">All'utente viene richiesta la conferma prima che venga applicata l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="ea819-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="ea819-112">Esempio 2: eliminare tutti i pool di batch per forza</span><span class="sxs-lookup"><span data-stu-id="ea819-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="ea819-113">Questo comando Elimina tutti i pool di batch.</span><span class="sxs-lookup"><span data-stu-id="ea819-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="ea819-114">Dato che il parametro *Force* è presente, il messaggio di conferma viene soppresso.</span><span class="sxs-lookup"><span data-stu-id="ea819-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="ea819-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea819-115">PARAMETERS</span></span>

### <span data-ttu-id="ea819-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ea819-116">-BatchContext</span></span>
<span data-ttu-id="ea819-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="ea819-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ea819-118">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="ea819-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ea819-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="ea819-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ea819-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ea819-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ea819-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ea819-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ea819-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea819-122">-DefaultProfile</span></span>
<span data-ttu-id="ea819-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea819-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea819-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ea819-124">-Force</span></span>
<span data-ttu-id="ea819-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ea819-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea819-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ea819-126">-Id</span></span>
<span data-ttu-id="ea819-127">Specifica l'ID del pool da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ea819-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="ea819-128">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="ea819-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea819-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea819-129">-Confirm</span></span>
<span data-ttu-id="ea819-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea819-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea819-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea819-131">-WhatIf</span></span>
<span data-ttu-id="ea819-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea819-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea819-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea819-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea819-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea819-134">CommonParameters</span></span>
<span data-ttu-id="ea819-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea819-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea819-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea819-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea819-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea819-137">INPUTS</span></span>

### <span data-ttu-id="ea819-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ea819-138">System.String</span></span>

### <span data-ttu-id="ea819-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ea819-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ea819-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea819-140">OUTPUTS</span></span>

### <span data-ttu-id="ea819-141">System. void</span><span class="sxs-lookup"><span data-stu-id="ea819-141">System.Void</span></span>

## <span data-ttu-id="ea819-142">Note</span><span class="sxs-lookup"><span data-stu-id="ea819-142">NOTES</span></span>

## <span data-ttu-id="ea819-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea819-143">RELATED LINKS</span></span>

[<span data-ttu-id="ea819-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ea819-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ea819-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ea819-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="ea819-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ea819-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="ea819-147">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="ea819-147">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


