---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177943"
---
# <span data-ttu-id="13291-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="13291-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="13291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13291-102">SYNOPSIS</span></span>
<span data-ttu-id="13291-103">Rigenerare le chiavi API per il membro member member.</span><span class="sxs-lookup"><span data-stu-id="13291-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="13291-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13291-104">SYNTAX</span></span>

### <span data-ttu-id="13291-105">RegenerateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="13291-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="13291-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="13291-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13291-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13291-107">DESCRIPTION</span></span>
<span data-ttu-id="13291-108">Rigenerare le chiavi API per il membro member member.</span><span class="sxs-lookup"><span data-stu-id="13291-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="13291-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13291-109">EXAMPLES</span></span>

### <span data-ttu-id="13291-110">Esempio 1: Rigenerare le chiavi API per un nodo di transazione usando il nome.</span><span class="sxs-lookup"><span data-stu-id="13291-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="13291-111">Questo comando genera le chiavi API per un nodo di transazione usando il nome, gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13291-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="13291-112">Esempio 2: Rigenerare le chiavi API per un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="13291-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="13291-113">Questo comando genera le chiavi Api per un nodo di transazione usando idenity.</span><span class="sxs-lookup"><span data-stu-id="13291-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="13291-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13291-114">PARAMETERS</span></span>

### <span data-ttu-id="13291-115">-MemberName</span><span class="sxs-lookup"><span data-stu-id="13291-115">-BlockchainMemberName</span></span>
<span data-ttu-id="13291-116">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="13291-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13291-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13291-117">-DefaultProfile</span></span>
<span data-ttu-id="13291-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13291-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13291-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13291-119">-InputObject</span></span>
<span data-ttu-id="13291-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="13291-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13291-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="13291-121">-KeyName</span></span>
<span data-ttu-id="13291-122">Ottiene o imposta il nome della chiave API.</span><span class="sxs-lookup"><span data-stu-id="13291-122">Gets or sets the API key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13291-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13291-123">-ResourceGroupName</span></span>
<span data-ttu-id="13291-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="13291-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="13291-125">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="13291-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13291-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13291-126">-SubscriptionId</span></span>
<span data-ttu-id="13291-127">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="13291-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="13291-128">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="13291-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13291-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="13291-129">-TransactionNodeName</span></span>
<span data-ttu-id="13291-130">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="13291-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13291-131">-Value</span><span class="sxs-lookup"><span data-stu-id="13291-131">-Value</span></span>
<span data-ttu-id="13291-132">Ottiene o imposta il valore della chiave API.</span><span class="sxs-lookup"><span data-stu-id="13291-132">Gets or sets the API key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13291-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13291-133">-Confirm</span></span>
<span data-ttu-id="13291-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13291-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13291-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13291-135">-WhatIf</span></span>
<span data-ttu-id="13291-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13291-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13291-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13291-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13291-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13291-138">CommonParameters</span></span>
<span data-ttu-id="13291-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13291-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13291-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13291-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13291-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="13291-141">INPUTS</span></span>

### <span data-ttu-id="13291-142">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="13291-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="13291-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13291-143">OUTPUTS</span></span>

### <span data-ttu-id="13291-144">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="13291-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="13291-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="13291-145">NOTES</span></span>

<span data-ttu-id="13291-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="13291-146">ALIASES</span></span>

<span data-ttu-id="13291-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="13291-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13291-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="13291-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13291-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13291-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13291-150">INPUTOBJECT <IBlockchainIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="13291-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13291-151">`[BlockchainMemberName <String>]`: nome membro dell'team di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="13291-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="13291-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="13291-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13291-153">`[Location <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="13291-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="13291-154">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="13291-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="13291-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="13291-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="13291-156">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="13291-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="13291-157">`[SubscriptionId <String>]`: ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="13291-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="13291-158">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="13291-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="13291-159">`[TransactionNodeName <String>]`: nome nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="13291-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="13291-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13291-160">RELATED LINKS</span></span>

