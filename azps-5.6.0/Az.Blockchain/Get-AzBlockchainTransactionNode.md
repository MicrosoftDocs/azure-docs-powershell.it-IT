---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 53178cf8e9eb38024e264aaeb2378349ba3dfa03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971469"
---
# <span data-ttu-id="cabdd-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="cabdd-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="cabdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cabdd-102">SYNOPSIS</span></span>
<span data-ttu-id="cabdd-103">Ottenere i dettagli del nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="cabdd-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="cabdd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cabdd-104">SYNTAX</span></span>

### <span data-ttu-id="cabdd-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cabdd-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cabdd-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cabdd-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cabdd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cabdd-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cabdd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cabdd-108">DESCRIPTION</span></span>
<span data-ttu-id="cabdd-109">Ottenere i dettagli del nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="cabdd-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="cabdd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cabdd-110">EXAMPLES</span></span>

### <span data-ttu-id="cabdd-111">Esempio 1: Elencare i nodi di transazione per un membro member</span><span class="sxs-lookup"><span data-stu-id="cabdd-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="cabdd-112">Questo comando elenca i nodi della transazione per un membro di member member di member member.</span><span class="sxs-lookup"><span data-stu-id="cabdd-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="cabdd-113">Esempio 2: Ottenere un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="cabdd-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="cabdd-114">Questo comando ottiene un nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="cabdd-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="cabdd-115">Esempio 3: Ottenere un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="cabdd-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="cabdd-116">Questo comando ottiene un nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="cabdd-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="cabdd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cabdd-117">PARAMETERS</span></span>

### <span data-ttu-id="cabdd-118">-MemberName</span><span class="sxs-lookup"><span data-stu-id="cabdd-118">-BlockchainMemberName</span></span>
<span data-ttu-id="cabdd-119">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="cabdd-119">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabdd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabdd-120">-DefaultProfile</span></span>
<span data-ttu-id="cabdd-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cabdd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cabdd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cabdd-122">-InputObject</span></span>
<span data-ttu-id="cabdd-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cabdd-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cabdd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cabdd-124">-Name</span></span>
<span data-ttu-id="cabdd-125">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="cabdd-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabdd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabdd-126">-ResourceGroupName</span></span>
<span data-ttu-id="cabdd-127">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cabdd-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cabdd-128">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="cabdd-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabdd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cabdd-129">-SubscriptionId</span></span>
<span data-ttu-id="cabdd-130">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cabdd-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cabdd-131">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cabdd-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabdd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabdd-132">CommonParameters</span></span>
<span data-ttu-id="cabdd-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabdd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabdd-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cabdd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabdd-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="cabdd-135">INPUTS</span></span>

### <span data-ttu-id="cabdd-136">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="cabdd-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="cabdd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cabdd-137">OUTPUTS</span></span>

### <span data-ttu-id="cabdd-138">Microsoft.Azure.PowerShell.Cmdlets.Cmdlets.Gateway.Models.Api20180601Preview.INode</span><span class="sxs-lookup"><span data-stu-id="cabdd-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="cabdd-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="cabdd-139">NOTES</span></span>

<span data-ttu-id="cabdd-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cabdd-140">ALIASES</span></span>

<span data-ttu-id="cabdd-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cabdd-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cabdd-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cabdd-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cabdd-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cabdd-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cabdd-144">INPUTOBJECT <IBlockchainIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="cabdd-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cabdd-145">`[BlockchainMemberName <String>]`: nome di membro dell'team di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="cabdd-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="cabdd-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="cabdd-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cabdd-147">`[Location <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="cabdd-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="cabdd-148">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="cabdd-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="cabdd-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cabdd-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cabdd-150">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="cabdd-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cabdd-151">`[SubscriptionId <String>]`: ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cabdd-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="cabdd-152">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cabdd-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="cabdd-153">`[TransactionNodeName <String>]`: nome nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="cabdd-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="cabdd-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cabdd-154">RELATED LINKS</span></span>

