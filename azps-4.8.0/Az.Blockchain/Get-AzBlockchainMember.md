---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032624"
---
# <span data-ttu-id="feace-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="feace-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="feace-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="feace-102">SYNOPSIS</span></span>
<span data-ttu-id="feace-103">Ottenere informazioni dettagliate su un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="feace-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="feace-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="feace-104">SYNTAX</span></span>

### <span data-ttu-id="feace-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="feace-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="feace-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="feace-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="feace-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="feace-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="feace-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="feace-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="feace-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="feace-109">DESCRIPTION</span></span>
<span data-ttu-id="feace-110">Ottenere informazioni dettagliate su un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="feace-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="feace-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="feace-111">EXAMPLES</span></span>

### <span data-ttu-id="feace-112">Esempio 1: elencare i membri di blockchain</span><span class="sxs-lookup"><span data-stu-id="feace-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="feace-113">Questo comando elenca i membri di blockchain in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="feace-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="feace-114">Esempio 2: elencare i membri di blockchain</span><span class="sxs-lookup"><span data-stu-id="feace-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="feace-115">Questo comando elenca i membri di blockchain in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="feace-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="feace-116">Esempio 3: ottenere un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="feace-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="feace-117">Questo comando ottiene un membro di blockchain in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="feace-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="feace-118">Esempio 4: ottenere un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="feace-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="feace-119">Questo comando ottiene un membro di blockchain in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="feace-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="feace-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="feace-120">PARAMETERS</span></span>

### <span data-ttu-id="feace-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feace-121">-DefaultProfile</span></span>
<span data-ttu-id="feace-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="feace-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feace-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feace-123">-InputObject</span></span>
<span data-ttu-id="feace-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="feace-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="feace-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="feace-125">-Name</span></span>
<span data-ttu-id="feace-126">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="feace-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feace-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feace-127">-ResourceGroupName</span></span>
<span data-ttu-id="feace-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="feace-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="feace-129">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="feace-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="feace-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="feace-130">-SubscriptionId</span></span>
<span data-ttu-id="feace-131">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="feace-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="feace-132">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="feace-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feace-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feace-133">CommonParameters</span></span>
<span data-ttu-id="feace-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feace-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feace-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="feace-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feace-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="feace-136">INPUTS</span></span>

### <span data-ttu-id="feace-137">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="feace-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="feace-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="feace-138">OUTPUTS</span></span>

### <span data-ttu-id="feace-139">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="feace-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="feace-140">Note</span><span class="sxs-lookup"><span data-stu-id="feace-140">NOTES</span></span>

<span data-ttu-id="feace-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="feace-141">ALIASES</span></span>

<span data-ttu-id="feace-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="feace-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="feace-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="feace-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="feace-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="feace-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="feace-145">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="feace-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="feace-146">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="feace-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="feace-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="feace-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="feace-148">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="feace-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="feace-149">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="feace-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="feace-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="feace-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="feace-151">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="feace-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="feace-152">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="feace-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="feace-153">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="feace-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="feace-154">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="feace-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="feace-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="feace-155">RELATED LINKS</span></span>

