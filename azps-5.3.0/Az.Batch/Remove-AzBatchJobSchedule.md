---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488780"
---
# <span data-ttu-id="f655e-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f655e-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f655e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f655e-102">SYNOPSIS</span></span>
<span data-ttu-id="f655e-103">Rimuove la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="f655e-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="f655e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f655e-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f655e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f655e-105">DESCRIPTION</span></span>
<span data-ttu-id="f655e-106">Il cmdlet **Remove-AzBatchJobSchedule** rimuove una pianificazione dei processi batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="f655e-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="f655e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f655e-107">EXAMPLES</span></span>

### <span data-ttu-id="f655e-108">Esempio 1: eliminare una pianificazione processo batch</span><span class="sxs-lookup"><span data-stu-id="f655e-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="f655e-109">Questo comando Elimina la pianificazione del processo con ID MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="f655e-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="f655e-110">Il comando richiede conferma prima di eliminare il processo.</span><span class="sxs-lookup"><span data-stu-id="f655e-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="f655e-111">Usa il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="f655e-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f655e-112">Esempio 2: eliminare una procedura batch senza conferma tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="f655e-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="f655e-113">Questo comando consente di ottenere la pianificazione del processo che contiene l'ID MyJobSchedule usando il cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="f655e-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="f655e-114">Il comando passa la pianificazione del processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f655e-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f655e-115">Il comando Elimina la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="f655e-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="f655e-116">Poiché il comando include il parametro *Force* , non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="f655e-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f655e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f655e-117">PARAMETERS</span></span>

### <span data-ttu-id="f655e-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f655e-118">-BatchContext</span></span>
<span data-ttu-id="f655e-119">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f655e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f655e-120">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f655e-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f655e-121">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="f655e-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f655e-122">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f655e-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f655e-123">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f655e-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f655e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f655e-124">-DefaultProfile</span></span>
<span data-ttu-id="f655e-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f655e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f655e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f655e-126">-Force</span></span>
<span data-ttu-id="f655e-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f655e-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f655e-128">-ID</span><span class="sxs-lookup"><span data-stu-id="f655e-128">-Id</span></span>
<span data-ttu-id="f655e-129">Specifica l'ID della pianificazione del processo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f655e-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="f655e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f655e-130">-Confirm</span></span>
<span data-ttu-id="f655e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f655e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f655e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f655e-132">-WhatIf</span></span>
<span data-ttu-id="f655e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f655e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f655e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f655e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f655e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f655e-135">CommonParameters</span></span>
<span data-ttu-id="f655e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f655e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f655e-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f655e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f655e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f655e-138">INPUTS</span></span>

### <span data-ttu-id="f655e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f655e-139">System.String</span></span>

### <span data-ttu-id="f655e-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f655e-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f655e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f655e-141">OUTPUTS</span></span>

### <span data-ttu-id="f655e-142">System. void</span><span class="sxs-lookup"><span data-stu-id="f655e-142">System.Void</span></span>

## <span data-ttu-id="f655e-143">Note</span><span class="sxs-lookup"><span data-stu-id="f655e-143">NOTES</span></span>

## <span data-ttu-id="f655e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f655e-144">RELATED LINKS</span></span>

[<span data-ttu-id="f655e-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f655e-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="f655e-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f655e-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="f655e-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f655e-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="f655e-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f655e-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="f655e-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f655e-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="f655e-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f655e-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


