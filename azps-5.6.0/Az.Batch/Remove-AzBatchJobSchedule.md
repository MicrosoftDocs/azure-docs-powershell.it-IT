---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 5e227662e8c0ce1011172eded7b218f627efbbbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009358"
---
# <span data-ttu-id="cd30b-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cd30b-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="cd30b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd30b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd30b-103">Rimuove la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="cd30b-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="cd30b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd30b-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd30b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd30b-105">DESCRIPTION</span></span>
<span data-ttu-id="cd30b-106">Il cmdlet **Remove-AzBatchJobSchedule** rimuove la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd30b-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="cd30b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd30b-107">EXAMPLES</span></span>

### <span data-ttu-id="cd30b-108">Esempio 1: Eliminare una pianificazione di un processo batch</span><span class="sxs-lookup"><span data-stu-id="cd30b-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="cd30b-109">Questo comando elimina la pianificazione del processo il cui ID è MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="cd30b-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="cd30b-110">Il comando chiede conferma prima di eliminare il processo.</span><span class="sxs-lookup"><span data-stu-id="cd30b-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="cd30b-111">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="cd30b-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cd30b-112">Esempio 2: Eliminare un processo batch senza conferma usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="cd30b-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="cd30b-113">Questo comando recupera la pianificazione del processo che ha l'ID MyJobSchedule usando il cmdlet Get-AzBatchJobSchedule lavoro.</span><span class="sxs-lookup"><span data-stu-id="cd30b-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="cd30b-114">Il comando passa la pianificazione del processo al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd30b-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cd30b-115">Il comando elimina la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="cd30b-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="cd30b-116">Poiché il comando include il *parametro Force,* non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="cd30b-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cd30b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd30b-117">PARAMETERS</span></span>

### <span data-ttu-id="cd30b-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cd30b-118">-BatchContext</span></span>
<span data-ttu-id="cd30b-119">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cd30b-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cd30b-120">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cd30b-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cd30b-121">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="cd30b-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cd30b-122">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="cd30b-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cd30b-123">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cd30b-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cd30b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd30b-124">-DefaultProfile</span></span>
<span data-ttu-id="cd30b-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd30b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd30b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cd30b-126">-Force</span></span>
<span data-ttu-id="cd30b-127">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="cd30b-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd30b-128">-Id</span><span class="sxs-lookup"><span data-stu-id="cd30b-128">-Id</span></span>
<span data-ttu-id="cd30b-129">Specifica l'ID della pianificazione del processo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cd30b-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="cd30b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd30b-130">-Confirm</span></span>
<span data-ttu-id="cd30b-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd30b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd30b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd30b-132">-WhatIf</span></span>
<span data-ttu-id="cd30b-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd30b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd30b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd30b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd30b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd30b-135">CommonParameters</span></span>
<span data-ttu-id="cd30b-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd30b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd30b-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd30b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd30b-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd30b-138">INPUTS</span></span>

### <span data-ttu-id="cd30b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cd30b-139">System.String</span></span>

### <span data-ttu-id="cd30b-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cd30b-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cd30b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd30b-141">OUTPUTS</span></span>

### <span data-ttu-id="cd30b-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="cd30b-142">System.Void</span></span>

## <span data-ttu-id="cd30b-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd30b-143">NOTES</span></span>

## <span data-ttu-id="cd30b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd30b-144">RELATED LINKS</span></span>

[<span data-ttu-id="cd30b-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cd30b-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="cd30b-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cd30b-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="cd30b-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cd30b-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="cd30b-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cd30b-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="cd30b-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cd30b-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="cd30b-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cd30b-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


