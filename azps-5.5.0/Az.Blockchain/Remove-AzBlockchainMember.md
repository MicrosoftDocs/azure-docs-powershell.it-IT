---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205146"
---
# <span data-ttu-id="681dd-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="681dd-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="681dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="681dd-102">SYNOPSIS</span></span>
<span data-ttu-id="681dd-103">Eliminare un membro del team.</span><span class="sxs-lookup"><span data-stu-id="681dd-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="681dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="681dd-104">SYNTAX</span></span>

### <span data-ttu-id="681dd-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="681dd-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="681dd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="681dd-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="681dd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="681dd-107">DESCRIPTION</span></span>
<span data-ttu-id="681dd-108">Eliminare un membro del team.</span><span class="sxs-lookup"><span data-stu-id="681dd-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="681dd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="681dd-109">EXAMPLES</span></span>

### <span data-ttu-id="681dd-110">Esempio 1: Rimuovere un membro member member di member member</span><span class="sxs-lookup"><span data-stu-id="681dd-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="681dd-111">Questo comando rimuove un membro di member member.</span><span class="sxs-lookup"><span data-stu-id="681dd-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="681dd-112">Esempio 2: Rimuovere un membro member member</span><span class="sxs-lookup"><span data-stu-id="681dd-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="681dd-113">Questo comando rimuove un membro di member member.</span><span class="sxs-lookup"><span data-stu-id="681dd-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="681dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="681dd-114">PARAMETERS</span></span>

### <span data-ttu-id="681dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="681dd-115">-AsJob</span></span>
<span data-ttu-id="681dd-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="681dd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="681dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681dd-117">-DefaultProfile</span></span>
<span data-ttu-id="681dd-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="681dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="681dd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="681dd-119">-InputObject</span></span>
<span data-ttu-id="681dd-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="681dd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="681dd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="681dd-121">-Name</span></span>
<span data-ttu-id="681dd-122">Nome di un membro del team</span><span class="sxs-lookup"><span data-stu-id="681dd-122">Blockchain member name</span></span>

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

### <span data-ttu-id="681dd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="681dd-123">-NoWait</span></span>
<span data-ttu-id="681dd-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="681dd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="681dd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="681dd-125">-PassThru</span></span>
<span data-ttu-id="681dd-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="681dd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="681dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="681dd-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="681dd-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="681dd-129">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="681dd-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="681dd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="681dd-130">-SubscriptionId</span></span>
<span data-ttu-id="681dd-131">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="681dd-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="681dd-132">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="681dd-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="681dd-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="681dd-133">-Confirm</span></span>
<span data-ttu-id="681dd-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="681dd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="681dd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="681dd-135">-WhatIf</span></span>
<span data-ttu-id="681dd-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="681dd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="681dd-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="681dd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="681dd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681dd-138">CommonParameters</span></span>
<span data-ttu-id="681dd-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="681dd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681dd-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="681dd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681dd-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="681dd-141">INPUTS</span></span>

### <span data-ttu-id="681dd-142">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="681dd-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="681dd-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="681dd-143">OUTPUTS</span></span>

### <span data-ttu-id="681dd-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="681dd-144">System.Boolean</span></span>

## <span data-ttu-id="681dd-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="681dd-145">NOTES</span></span>

<span data-ttu-id="681dd-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="681dd-146">ALIASES</span></span>

<span data-ttu-id="681dd-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="681dd-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="681dd-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="681dd-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="681dd-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="681dd-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="681dd-150">INPUTOBJECT <IBlockchainIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="681dd-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="681dd-151">`[BlockchainMemberName <String>]`: nome membro dell'team di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="681dd-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="681dd-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="681dd-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="681dd-153">`[Location <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="681dd-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="681dd-154">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="681dd-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="681dd-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="681dd-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="681dd-156">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="681dd-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="681dd-157">`[SubscriptionId <String>]`: ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="681dd-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="681dd-158">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="681dd-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="681dd-159">`[TransactionNodeName <String>]`: nome nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="681dd-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="681dd-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="681dd-160">RELATED LINKS</span></span>

