---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363229"
---
# <span data-ttu-id="86b8b-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="86b8b-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="86b8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="86b8b-103">Eliminare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="86b8b-103">Delete the transaction node.</span></span>

## <span data-ttu-id="86b8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86b8b-104">SYNTAX</span></span>

### <span data-ttu-id="86b8b-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86b8b-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="86b8b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="86b8b-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="86b8b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86b8b-107">DESCRIPTION</span></span>
<span data-ttu-id="86b8b-108">Eliminare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="86b8b-108">Delete the transaction node.</span></span>

## <span data-ttu-id="86b8b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86b8b-109">EXAMPLES</span></span>

### <span data-ttu-id="86b8b-110">Esempio 1: rimuovere un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="86b8b-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="86b8b-111">Questo comando rimuove un nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="86b8b-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="86b8b-112">Esempio 2: rimuovere un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="86b8b-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="86b8b-113">Questo comando rimuove un nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="86b8b-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="86b8b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86b8b-114">PARAMETERS</span></span>

### <span data-ttu-id="86b8b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86b8b-115">-AsJob</span></span>
<span data-ttu-id="86b8b-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="86b8b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="86b8b-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="86b8b-117">-BlockchainMemberName</span></span>
<span data-ttu-id="86b8b-118">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="86b8b-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="86b8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b8b-119">-DefaultProfile</span></span>
<span data-ttu-id="86b8b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86b8b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86b8b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86b8b-121">-InputObject</span></span>
<span data-ttu-id="86b8b-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="86b8b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="86b8b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="86b8b-123">-Name</span></span>
<span data-ttu-id="86b8b-124">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="86b8b-124">Transaction node name.</span></span>

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

### <span data-ttu-id="86b8b-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="86b8b-125">-NoWait</span></span>
<span data-ttu-id="86b8b-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="86b8b-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="86b8b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86b8b-127">-PassThru</span></span>
<span data-ttu-id="86b8b-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="86b8b-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="86b8b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86b8b-129">-ResourceGroupName</span></span>
<span data-ttu-id="86b8b-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="86b8b-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="86b8b-131">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="86b8b-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="86b8b-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86b8b-132">-SubscriptionId</span></span>
<span data-ttu-id="86b8b-133">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="86b8b-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="86b8b-134">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="86b8b-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="86b8b-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86b8b-135">-Confirm</span></span>
<span data-ttu-id="86b8b-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86b8b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86b8b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86b8b-137">-WhatIf</span></span>
<span data-ttu-id="86b8b-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86b8b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86b8b-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86b8b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86b8b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b8b-140">CommonParameters</span></span>
<span data-ttu-id="86b8b-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86b8b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b8b-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86b8b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b8b-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86b8b-143">INPUTS</span></span>

### <span data-ttu-id="86b8b-144">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="86b8b-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="86b8b-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86b8b-145">OUTPUTS</span></span>

### <span data-ttu-id="86b8b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86b8b-146">System.Boolean</span></span>

## <span data-ttu-id="86b8b-147">Note</span><span class="sxs-lookup"><span data-stu-id="86b8b-147">NOTES</span></span>

<span data-ttu-id="86b8b-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="86b8b-148">ALIASES</span></span>

<span data-ttu-id="86b8b-149">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86b8b-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86b8b-150">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="86b8b-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86b8b-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86b8b-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86b8b-152">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="86b8b-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="86b8b-153">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="86b8b-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="86b8b-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="86b8b-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86b8b-155">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="86b8b-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="86b8b-156">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="86b8b-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="86b8b-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="86b8b-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="86b8b-158">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="86b8b-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="86b8b-159">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="86b8b-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="86b8b-160">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="86b8b-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="86b8b-161">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="86b8b-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="86b8b-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86b8b-162">RELATED LINKS</span></span>

