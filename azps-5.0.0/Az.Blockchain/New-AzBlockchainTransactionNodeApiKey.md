---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201114"
---
# <span data-ttu-id="1ac4d-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="1ac4d-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="1ac4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ac4d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac4d-103">Rigenerare le chiavi dell'API per il membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="1ac4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ac4d-104">SYNTAX</span></span>

### <span data-ttu-id="1ac4d-105">RegenerateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ac4d-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ac4d-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1ac4d-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ac4d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ac4d-107">DESCRIPTION</span></span>
<span data-ttu-id="1ac4d-108">Rigenerare le chiavi dell'API per il membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="1ac4d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ac4d-109">EXAMPLES</span></span>

### <span data-ttu-id="1ac4d-110">Esempio 1: rigenerare le chiavi API per un nodo transazione tramite Name.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="1ac4d-111">Questo comando genera le chiavi API per un nodo transazione tramite nome, gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="1ac4d-112">Esempio 2: rigenerare le chiavi API per un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="1ac4d-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="1ac4d-113">Questo comando genera le chiavi API per un nodo di transazione usando l'identità.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="1ac4d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ac4d-114">PARAMETERS</span></span>

### <span data-ttu-id="1ac4d-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="1ac4d-115">-BlockchainMemberName</span></span>
<span data-ttu-id="1ac4d-116">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="1ac4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac4d-117">-DefaultProfile</span></span>
<span data-ttu-id="1ac4d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ac4d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ac4d-119">-InputObject</span></span>
<span data-ttu-id="1ac4d-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ac4d-121">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="1ac4d-121">-KeyName</span></span>
<span data-ttu-id="1ac4d-122">Ottiene o imposta il nome della chiave dell'API.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="1ac4d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac4d-123">-ResourceGroupName</span></span>
<span data-ttu-id="1ac4d-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1ac4d-125">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1ac4d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ac4d-126">-SubscriptionId</span></span>
<span data-ttu-id="1ac4d-127">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ac4d-128">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1ac4d-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="1ac4d-129">-TransactionNodeName</span></span>
<span data-ttu-id="1ac4d-130">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-130">Transaction node name.</span></span>

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

### <span data-ttu-id="1ac4d-131">-Valore</span><span class="sxs-lookup"><span data-stu-id="1ac4d-131">-Value</span></span>
<span data-ttu-id="1ac4d-132">Ottiene o imposta il valore della chiave API.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="1ac4d-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ac4d-133">-Confirm</span></span>
<span data-ttu-id="1ac4d-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ac4d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac4d-135">-WhatIf</span></span>
<span data-ttu-id="1ac4d-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ac4d-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ac4d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac4d-138">CommonParameters</span></span>
<span data-ttu-id="1ac4d-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac4d-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ac4d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac4d-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ac4d-141">INPUTS</span></span>

### <span data-ttu-id="1ac4d-142">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="1ac4d-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="1ac4d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ac4d-143">OUTPUTS</span></span>

### <span data-ttu-id="1ac4d-144">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="1ac4d-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="1ac4d-145">Note</span><span class="sxs-lookup"><span data-stu-id="1ac4d-145">NOTES</span></span>

<span data-ttu-id="1ac4d-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1ac4d-146">ALIASES</span></span>

<span data-ttu-id="1ac4d-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ac4d-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ac4d-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ac4d-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ac4d-150">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1ac4d-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ac4d-151">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="1ac4d-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1ac4d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ac4d-153">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="1ac4d-154">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="1ac4d-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1ac4d-156">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1ac4d-157">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="1ac4d-158">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="1ac4d-159">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="1ac4d-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="1ac4d-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ac4d-160">RELATED LINKS</span></span>

