---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177942"
---
# <span data-ttu-id="6cbce-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="6cbce-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="6cbce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cbce-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbce-103">Eliminare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="6cbce-103">Delete the transaction node.</span></span>

## <span data-ttu-id="6cbce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cbce-104">SYNTAX</span></span>

### <span data-ttu-id="6cbce-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6cbce-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6cbce-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6cbce-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cbce-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6cbce-107">DESCRIPTION</span></span>
<span data-ttu-id="6cbce-108">Eliminare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="6cbce-108">Delete the transaction node.</span></span>

## <span data-ttu-id="6cbce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cbce-109">EXAMPLES</span></span>

### <span data-ttu-id="6cbce-110">Esempio 1: Rimuovere un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="6cbce-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="6cbce-111">Questo comando rimuove un nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="6cbce-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="6cbce-112">Esempio 2: Rimuovere un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="6cbce-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="6cbce-113">Questo comando rimuove un nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="6cbce-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="6cbce-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cbce-114">PARAMETERS</span></span>

### <span data-ttu-id="6cbce-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cbce-115">-AsJob</span></span>
<span data-ttu-id="6cbce-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6cbce-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6cbce-117">-MemberName</span><span class="sxs-lookup"><span data-stu-id="6cbce-117">-BlockchainMemberName</span></span>
<span data-ttu-id="6cbce-118">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="6cbce-118">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbce-119">-DefaultProfile</span></span>
<span data-ttu-id="6cbce-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cbce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cbce-121">-InputObject</span></span>
<span data-ttu-id="6cbce-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6cbce-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cbce-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6cbce-123">-Name</span></span>
<span data-ttu-id="6cbce-124">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="6cbce-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbce-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6cbce-125">-NoWait</span></span>
<span data-ttu-id="6cbce-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6cbce-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6cbce-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cbce-127">-PassThru</span></span>
<span data-ttu-id="6cbce-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="6cbce-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6cbce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cbce-129">-ResourceGroupName</span></span>
<span data-ttu-id="6cbce-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6cbce-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6cbce-131">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="6cbce-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbce-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cbce-132">-SubscriptionId</span></span>
<span data-ttu-id="6cbce-133">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6cbce-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6cbce-134">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6cbce-134">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbce-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cbce-135">-Confirm</span></span>
<span data-ttu-id="6cbce-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cbce-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbce-137">-WhatIf</span></span>
<span data-ttu-id="6cbce-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cbce-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbce-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cbce-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbce-140">CommonParameters</span></span>
<span data-ttu-id="6cbce-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cbce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbce-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6cbce-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbce-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="6cbce-143">INPUTS</span></span>

### <span data-ttu-id="6cbce-144">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="6cbce-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="6cbce-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cbce-145">OUTPUTS</span></span>

### <span data-ttu-id="6cbce-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6cbce-146">System.Boolean</span></span>

## <span data-ttu-id="6cbce-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="6cbce-147">NOTES</span></span>

<span data-ttu-id="6cbce-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6cbce-148">ALIASES</span></span>

<span data-ttu-id="6cbce-149">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="6cbce-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cbce-150">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6cbce-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cbce-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cbce-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cbce-152">INPUTOBJECT <IBlockchainIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="6cbce-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cbce-153">`[BlockchainMemberName <String>]`: nome membro dell'team di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="6cbce-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="6cbce-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6cbce-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cbce-155">`[Location <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="6cbce-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="6cbce-156">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="6cbce-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="6cbce-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6cbce-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6cbce-158">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="6cbce-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6cbce-159">`[SubscriptionId <String>]`: ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6cbce-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="6cbce-160">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6cbce-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="6cbce-161">`[TransactionNodeName <String>]`: nome nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="6cbce-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="6cbce-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cbce-162">RELATED LINKS</span></span>

