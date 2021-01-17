---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488755"
---
# <span data-ttu-id="04e85-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="04e85-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="04e85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04e85-102">SYNOPSIS</span></span>
<span data-ttu-id="04e85-103">Ottenere informazioni dettagliate su un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="04e85-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="04e85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04e85-104">SYNTAX</span></span>

### <span data-ttu-id="04e85-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="04e85-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="04e85-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="04e85-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="04e85-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="04e85-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="04e85-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="04e85-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="04e85-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04e85-109">DESCRIPTION</span></span>
<span data-ttu-id="04e85-110">Ottenere informazioni dettagliate su un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="04e85-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="04e85-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04e85-111">EXAMPLES</span></span>

### <span data-ttu-id="04e85-112">Esempio 1: elencare i membri di blockchain</span><span class="sxs-lookup"><span data-stu-id="04e85-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="04e85-113">Questo comando elenca i membri di blockchain in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="04e85-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="04e85-114">Esempio 2: elencare i membri di blockchain</span><span class="sxs-lookup"><span data-stu-id="04e85-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="04e85-115">Questo comando elenca i membri di blockchain in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="04e85-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="04e85-116">Esempio 3: ottenere un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="04e85-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="04e85-117">Questo comando ottiene un membro di blockchain in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="04e85-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="04e85-118">Esempio 4: ottenere un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="04e85-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="04e85-119">Questo comando ottiene un membro di blockchain in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="04e85-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="04e85-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04e85-120">PARAMETERS</span></span>

### <span data-ttu-id="04e85-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e85-121">-DefaultProfile</span></span>
<span data-ttu-id="04e85-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04e85-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04e85-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04e85-123">-InputObject</span></span>
<span data-ttu-id="04e85-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="04e85-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04e85-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="04e85-125">-Name</span></span>
<span data-ttu-id="04e85-126">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="04e85-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="04e85-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04e85-127">-ResourceGroupName</span></span>
<span data-ttu-id="04e85-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="04e85-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="04e85-129">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="04e85-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="04e85-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04e85-130">-SubscriptionId</span></span>
<span data-ttu-id="04e85-131">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="04e85-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="04e85-132">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="04e85-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="04e85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e85-133">CommonParameters</span></span>
<span data-ttu-id="04e85-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04e85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e85-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04e85-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e85-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04e85-136">INPUTS</span></span>

### <span data-ttu-id="04e85-137">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="04e85-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="04e85-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04e85-138">OUTPUTS</span></span>

### <span data-ttu-id="04e85-139">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="04e85-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="04e85-140">Note</span><span class="sxs-lookup"><span data-stu-id="04e85-140">NOTES</span></span>

<span data-ttu-id="04e85-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="04e85-141">ALIASES</span></span>

<span data-ttu-id="04e85-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04e85-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04e85-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="04e85-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04e85-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="04e85-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04e85-145">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="04e85-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04e85-146">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="04e85-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="04e85-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="04e85-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04e85-148">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="04e85-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="04e85-149">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="04e85-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="04e85-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="04e85-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="04e85-151">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="04e85-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="04e85-152">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="04e85-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="04e85-153">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="04e85-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="04e85-154">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="04e85-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="04e85-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04e85-155">RELATED LINKS</span></span>

