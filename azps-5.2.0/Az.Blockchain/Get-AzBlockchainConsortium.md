---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333124"
---
# <span data-ttu-id="604d3-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="604d3-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="604d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="604d3-102">SYNOPSIS</span></span>
<span data-ttu-id="604d3-103">Elenca i consorzi disponibili per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="604d3-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="604d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="604d3-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="604d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="604d3-105">DESCRIPTION</span></span>
<span data-ttu-id="604d3-106">Elenca i consorzi disponibili per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="604d3-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="604d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="604d3-107">EXAMPLES</span></span>

### <span data-ttu-id="604d3-108">Esempio 1: ottenere consorzi blockchain.</span><span class="sxs-lookup"><span data-stu-id="604d3-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="604d3-109">Questo comando elenca i consorzi in un abbonamento per una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="604d3-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="604d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="604d3-110">PARAMETERS</span></span>

### <span data-ttu-id="604d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604d3-111">-DefaultProfile</span></span>
<span data-ttu-id="604d3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="604d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="604d3-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="604d3-113">-Location</span></span>
<span data-ttu-id="604d3-114">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="604d3-114">Location Name.</span></span>

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

### <span data-ttu-id="604d3-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="604d3-115">-SubscriptionId</span></span>
<span data-ttu-id="604d3-116">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="604d3-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="604d3-117">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="604d3-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="604d3-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="604d3-118">-Confirm</span></span>
<span data-ttu-id="604d3-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="604d3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="604d3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="604d3-120">-WhatIf</span></span>
<span data-ttu-id="604d3-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="604d3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="604d3-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="604d3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="604d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604d3-123">CommonParameters</span></span>
<span data-ttu-id="604d3-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="604d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604d3-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="604d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604d3-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="604d3-126">INPUTS</span></span>

## <span data-ttu-id="604d3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="604d3-127">OUTPUTS</span></span>

### <span data-ttu-id="604d3-128">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="604d3-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="604d3-129">Note</span><span class="sxs-lookup"><span data-stu-id="604d3-129">NOTES</span></span>

<span data-ttu-id="604d3-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="604d3-130">ALIASES</span></span>

## <span data-ttu-id="604d3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="604d3-131">RELATED LINKS</span></span>

