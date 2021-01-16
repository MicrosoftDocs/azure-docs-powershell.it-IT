---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341896"
---
# <span data-ttu-id="d998a-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="d998a-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="d998a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d998a-102">SYNOPSIS</span></span>
<span data-ttu-id="d998a-103">Ottenere i dettagli del nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="d998a-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="d998a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d998a-104">SYNTAX</span></span>

### <span data-ttu-id="d998a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d998a-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d998a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d998a-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d998a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d998a-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d998a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d998a-108">DESCRIPTION</span></span>
<span data-ttu-id="d998a-109">Ottenere i dettagli del nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="d998a-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="d998a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d998a-110">EXAMPLES</span></span>

### <span data-ttu-id="d998a-111">Esempio 1: elencare i nodi delle transazioni per un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="d998a-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="d998a-112">Questo comando elenca i nodi delle transazioni per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="d998a-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="d998a-113">Esempio 2: ottenere un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="d998a-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="d998a-114">Questo comando ottiene un nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="d998a-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="d998a-115">Esempio 3: ottenere un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="d998a-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="d998a-116">Questo comando ottiene un nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="d998a-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="d998a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d998a-117">PARAMETERS</span></span>

### <span data-ttu-id="d998a-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="d998a-118">-BlockchainMemberName</span></span>
<span data-ttu-id="d998a-119">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="d998a-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="d998a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d998a-120">-DefaultProfile</span></span>
<span data-ttu-id="d998a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d998a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d998a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d998a-122">-InputObject</span></span>
<span data-ttu-id="d998a-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d998a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d998a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d998a-124">-Name</span></span>
<span data-ttu-id="d998a-125">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="d998a-125">Transaction node name.</span></span>

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

### <span data-ttu-id="d998a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d998a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d998a-127">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d998a-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d998a-128">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="d998a-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d998a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d998a-129">-SubscriptionId</span></span>
<span data-ttu-id="d998a-130">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d998a-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d998a-131">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d998a-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d998a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d998a-132">CommonParameters</span></span>
<span data-ttu-id="d998a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d998a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d998a-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d998a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d998a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d998a-135">INPUTS</span></span>

### <span data-ttu-id="d998a-136">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="d998a-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="d998a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d998a-137">OUTPUTS</span></span>

### <span data-ttu-id="d998a-138">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="d998a-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="d998a-139">Note</span><span class="sxs-lookup"><span data-stu-id="d998a-139">NOTES</span></span>

<span data-ttu-id="d998a-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d998a-140">ALIASES</span></span>

<span data-ttu-id="d998a-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d998a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d998a-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d998a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d998a-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d998a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d998a-144">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d998a-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d998a-145">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="d998a-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="d998a-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d998a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d998a-147">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="d998a-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="d998a-148">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="d998a-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="d998a-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d998a-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d998a-150">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="d998a-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d998a-151">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d998a-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d998a-152">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d998a-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="d998a-153">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="d998a-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="d998a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d998a-154">RELATED LINKS</span></span>

