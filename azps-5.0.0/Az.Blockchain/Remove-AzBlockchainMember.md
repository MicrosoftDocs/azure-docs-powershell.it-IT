---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200273"
---
# <span data-ttu-id="74120-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="74120-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="74120-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74120-102">SYNOPSIS</span></span>
<span data-ttu-id="74120-103">Eliminare un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="74120-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="74120-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74120-104">SYNTAX</span></span>

### <span data-ttu-id="74120-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="74120-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74120-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74120-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74120-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74120-107">DESCRIPTION</span></span>
<span data-ttu-id="74120-108">Eliminare un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="74120-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="74120-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74120-109">EXAMPLES</span></span>

### <span data-ttu-id="74120-110">Esempio 1: rimuovere un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="74120-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="74120-111">Questo comando rimuove un membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="74120-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="74120-112">Esempio 2: rimuovere un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="74120-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="74120-113">Questo comando rimuove un membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="74120-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="74120-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74120-114">PARAMETERS</span></span>

### <span data-ttu-id="74120-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74120-115">-AsJob</span></span>
<span data-ttu-id="74120-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="74120-116">Run the command as a job</span></span>

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

### <span data-ttu-id="74120-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74120-117">-DefaultProfile</span></span>
<span data-ttu-id="74120-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74120-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74120-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74120-119">-InputObject</span></span>
<span data-ttu-id="74120-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="74120-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74120-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="74120-121">-Name</span></span>
<span data-ttu-id="74120-122">Nome membro blockchain</span><span class="sxs-lookup"><span data-stu-id="74120-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74120-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="74120-123">-NoWait</span></span>
<span data-ttu-id="74120-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="74120-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74120-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74120-125">-PassThru</span></span>
<span data-ttu-id="74120-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="74120-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="74120-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74120-127">-ResourceGroupName</span></span>
<span data-ttu-id="74120-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="74120-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="74120-129">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="74120-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="74120-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74120-130">-SubscriptionId</span></span>
<span data-ttu-id="74120-131">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="74120-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="74120-132">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="74120-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="74120-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74120-133">-Confirm</span></span>
<span data-ttu-id="74120-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74120-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74120-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74120-135">-WhatIf</span></span>
<span data-ttu-id="74120-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74120-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74120-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74120-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74120-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74120-138">CommonParameters</span></span>
<span data-ttu-id="74120-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74120-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74120-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74120-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74120-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74120-141">INPUTS</span></span>

### <span data-ttu-id="74120-142">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="74120-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="74120-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74120-143">OUTPUTS</span></span>

### <span data-ttu-id="74120-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74120-144">System.Boolean</span></span>

## <span data-ttu-id="74120-145">Note</span><span class="sxs-lookup"><span data-stu-id="74120-145">NOTES</span></span>

<span data-ttu-id="74120-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="74120-146">ALIASES</span></span>

<span data-ttu-id="74120-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74120-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74120-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="74120-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74120-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74120-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74120-150">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="74120-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74120-151">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="74120-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="74120-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="74120-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74120-153">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="74120-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="74120-154">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="74120-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="74120-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="74120-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="74120-156">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="74120-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="74120-157">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="74120-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="74120-158">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="74120-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="74120-159">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="74120-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="74120-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74120-160">RELATED LINKS</span></span>

