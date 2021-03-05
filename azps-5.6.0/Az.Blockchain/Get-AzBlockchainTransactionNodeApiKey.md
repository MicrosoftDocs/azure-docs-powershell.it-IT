---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: dbde273c1694f4622904ac00b261e902036c6e03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971454"
---
# <span data-ttu-id="7bd43-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="7bd43-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="7bd43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd43-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd43-103">Elencare le chiavi API per il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7bd43-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="7bd43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bd43-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7bd43-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7bd43-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd43-106">Elencare le chiavi API per il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7bd43-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="7bd43-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bd43-107">EXAMPLES</span></span>

### <span data-ttu-id="7bd43-108">Esempio 1: Elencare le chiavi API per un nodo di transazione</span><span class="sxs-lookup"><span data-stu-id="7bd43-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="7bd43-109">Questo comando elenca le chiavi API per un nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="7bd43-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="7bd43-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bd43-110">PARAMETERS</span></span>

### <span data-ttu-id="7bd43-111">-MemberName</span><span class="sxs-lookup"><span data-stu-id="7bd43-111">-BlockchainMemberName</span></span>
<span data-ttu-id="7bd43-112">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="7bd43-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="7bd43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd43-113">-DefaultProfile</span></span>
<span data-ttu-id="7bd43-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd43-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd43-115">-ResourceGroupName</span></span>
<span data-ttu-id="7bd43-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7bd43-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7bd43-117">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="7bd43-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7bd43-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bd43-118">-SubscriptionId</span></span>
<span data-ttu-id="7bd43-119">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd43-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7bd43-120">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7bd43-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7bd43-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="7bd43-121">-TransactionNodeName</span></span>
<span data-ttu-id="7bd43-122">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="7bd43-122">Transaction node name.</span></span>

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

### <span data-ttu-id="7bd43-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bd43-123">-Confirm</span></span>
<span data-ttu-id="7bd43-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bd43-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd43-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd43-125">-WhatIf</span></span>
<span data-ttu-id="7bd43-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bd43-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd43-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bd43-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd43-128">CommonParameters</span></span>
<span data-ttu-id="7bd43-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd43-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7bd43-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd43-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="7bd43-131">INPUTS</span></span>

## <span data-ttu-id="7bd43-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bd43-132">OUTPUTS</span></span>

### <span data-ttu-id="7bd43-133">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="7bd43-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="7bd43-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="7bd43-134">NOTES</span></span>

<span data-ttu-id="7bd43-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7bd43-135">ALIASES</span></span>

## <span data-ttu-id="7bd43-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bd43-136">RELATED LINKS</span></span>

