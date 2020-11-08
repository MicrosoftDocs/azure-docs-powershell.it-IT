---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203019"
---
# <span data-ttu-id="88b08-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="88b08-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="88b08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88b08-102">SYNOPSIS</span></span>
<span data-ttu-id="88b08-103">Elenca le chiavi dell'API per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="88b08-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="88b08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88b08-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88b08-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88b08-105">DESCRIPTION</span></span>
<span data-ttu-id="88b08-106">Elenca le chiavi dell'API per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="88b08-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="88b08-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88b08-107">EXAMPLES</span></span>

### <span data-ttu-id="88b08-108">Esempio 1: chiavi dell'API elenco blockchain</span><span class="sxs-lookup"><span data-stu-id="88b08-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="88b08-109">Questo comando elenca le chiavi API per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="88b08-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="88b08-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88b08-110">PARAMETERS</span></span>

### <span data-ttu-id="88b08-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="88b08-111">-BlockchainMemberName</span></span>
<span data-ttu-id="88b08-112">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="88b08-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="88b08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b08-113">-DefaultProfile</span></span>
<span data-ttu-id="88b08-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88b08-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b08-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b08-115">-ResourceGroupName</span></span>
<span data-ttu-id="88b08-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="88b08-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="88b08-117">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="88b08-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="88b08-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88b08-118">-SubscriptionId</span></span>
<span data-ttu-id="88b08-119">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="88b08-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="88b08-120">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="88b08-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="88b08-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88b08-121">-Confirm</span></span>
<span data-ttu-id="88b08-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b08-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b08-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b08-123">-WhatIf</span></span>
<span data-ttu-id="88b08-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b08-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b08-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b08-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88b08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b08-126">CommonParameters</span></span>
<span data-ttu-id="88b08-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b08-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88b08-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b08-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88b08-129">INPUTS</span></span>

## <span data-ttu-id="88b08-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88b08-130">OUTPUTS</span></span>

### <span data-ttu-id="88b08-131">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="88b08-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="88b08-132">Note</span><span class="sxs-lookup"><span data-stu-id="88b08-132">NOTES</span></span>

<span data-ttu-id="88b08-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="88b08-133">ALIASES</span></span>

## <span data-ttu-id="88b08-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88b08-134">RELATED LINKS</span></span>

