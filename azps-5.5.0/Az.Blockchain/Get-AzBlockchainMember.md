---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181959"
---
# <span data-ttu-id="c63f9-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c63f9-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="c63f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c63f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c63f9-103">Informazioni dettagliate su un membro del team.</span><span class="sxs-lookup"><span data-stu-id="c63f9-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="c63f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c63f9-104">SYNTAX</span></span>

### <span data-ttu-id="c63f9-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c63f9-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c63f9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c63f9-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c63f9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c63f9-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c63f9-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="c63f9-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c63f9-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c63f9-109">DESCRIPTION</span></span>
<span data-ttu-id="c63f9-110">Informazioni dettagliate su un membro del team.</span><span class="sxs-lookup"><span data-stu-id="c63f9-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="c63f9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c63f9-111">EXAMPLES</span></span>

### <span data-ttu-id="c63f9-112">Esempio 1: Elencare membri di members</span><span class="sxs-lookup"><span data-stu-id="c63f9-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c63f9-113">Questo comando elenca i membri di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c63f9-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="c63f9-114">Esempio 2: Elencare membri di members</span><span class="sxs-lookup"><span data-stu-id="c63f9-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c63f9-115">Questo comando elenca i membri di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c63f9-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="c63f9-116">Esempio 3: Ottenere un membro member</span><span class="sxs-lookup"><span data-stu-id="c63f9-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c63f9-117">Questo comando ottiene un membro di member member in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c63f9-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="c63f9-118">Esempio 4: Ottenere un membro member</span><span class="sxs-lookup"><span data-stu-id="c63f9-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c63f9-119">Questo comando ottiene un membro di member member in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c63f9-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="c63f9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c63f9-120">PARAMETERS</span></span>

### <span data-ttu-id="c63f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63f9-121">-DefaultProfile</span></span>
<span data-ttu-id="c63f9-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c63f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63f9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c63f9-123">-InputObject</span></span>
<span data-ttu-id="c63f9-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c63f9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c63f9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c63f9-125">-Name</span></span>
<span data-ttu-id="c63f9-126">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="c63f9-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="c63f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c63f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="c63f9-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c63f9-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c63f9-129">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c63f9-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c63f9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c63f9-130">-SubscriptionId</span></span>
<span data-ttu-id="c63f9-131">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c63f9-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c63f9-132">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c63f9-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c63f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63f9-133">CommonParameters</span></span>
<span data-ttu-id="c63f9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63f9-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c63f9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63f9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="c63f9-136">INPUTS</span></span>

### <span data-ttu-id="c63f9-137">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="c63f9-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="c63f9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c63f9-138">OUTPUTS</span></span>

### <span data-ttu-id="c63f9-139">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c63f9-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="c63f9-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="c63f9-140">NOTES</span></span>

<span data-ttu-id="c63f9-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c63f9-141">ALIASES</span></span>

<span data-ttu-id="c63f9-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="c63f9-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c63f9-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c63f9-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c63f9-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c63f9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c63f9-145">INPUTOBJECT <IBlockchainIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="c63f9-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c63f9-146">`[BlockchainMemberName <String>]`: nome membro dell'team di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="c63f9-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="c63f9-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="c63f9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c63f9-148">`[Location <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="c63f9-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="c63f9-149">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="c63f9-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="c63f9-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c63f9-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c63f9-151">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c63f9-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c63f9-152">`[SubscriptionId <String>]`: ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c63f9-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c63f9-153">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c63f9-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="c63f9-154">`[TransactionNodeName <String>]`: nome nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="c63f9-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="c63f9-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c63f9-155">RELATED LINKS</span></span>

