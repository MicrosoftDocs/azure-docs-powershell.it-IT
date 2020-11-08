---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203008"
---
# <span data-ttu-id="52fe1-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="52fe1-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="52fe1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="52fe1-103">Elencare le chiavi dell'API per il nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="52fe1-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="52fe1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52fe1-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="52fe1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52fe1-105">DESCRIPTION</span></span>
<span data-ttu-id="52fe1-106">Elencare le chiavi dell'API per il nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="52fe1-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="52fe1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52fe1-107">EXAMPLES</span></span>

### <span data-ttu-id="52fe1-108">Esempio 1: chiavi dell'API di elenco per un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="52fe1-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="52fe1-109">Questo comando elenca le chiavi API per un nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="52fe1-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="52fe1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52fe1-110">PARAMETERS</span></span>

### <span data-ttu-id="52fe1-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="52fe1-111">-BlockchainMemberName</span></span>
<span data-ttu-id="52fe1-112">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="52fe1-112">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fe1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fe1-113">-DefaultProfile</span></span>
<span data-ttu-id="52fe1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52fe1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52fe1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52fe1-115">-ResourceGroupName</span></span>
<span data-ttu-id="52fe1-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="52fe1-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="52fe1-117">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="52fe1-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fe1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52fe1-118">-SubscriptionId</span></span>
<span data-ttu-id="52fe1-119">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="52fe1-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="52fe1-120">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="52fe1-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fe1-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="52fe1-121">-TransactionNodeName</span></span>
<span data-ttu-id="52fe1-122">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="52fe1-122">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fe1-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52fe1-123">-Confirm</span></span>
<span data-ttu-id="52fe1-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fe1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52fe1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52fe1-125">-WhatIf</span></span>
<span data-ttu-id="52fe1-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52fe1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52fe1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52fe1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52fe1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fe1-128">CommonParameters</span></span>
<span data-ttu-id="52fe1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fe1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fe1-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52fe1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fe1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52fe1-131">INPUTS</span></span>

## <span data-ttu-id="52fe1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52fe1-132">OUTPUTS</span></span>

### <span data-ttu-id="52fe1-133">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="52fe1-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="52fe1-134">Note</span><span class="sxs-lookup"><span data-stu-id="52fe1-134">NOTES</span></span>

<span data-ttu-id="52fe1-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="52fe1-135">ALIASES</span></span>

## <span data-ttu-id="52fe1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52fe1-136">RELATED LINKS</span></span>

