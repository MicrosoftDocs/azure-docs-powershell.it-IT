---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478116"
---
# <span data-ttu-id="5ab73-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="5ab73-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="5ab73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ab73-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab73-103">Elenca i consorzi disponibili per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5ab73-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="5ab73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ab73-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ab73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ab73-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab73-106">Elenca i consorzi disponibili per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5ab73-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="5ab73-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ab73-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab73-108">Esempio 1: ottenere consorzi blockchain.</span><span class="sxs-lookup"><span data-stu-id="5ab73-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="5ab73-109">Questo comando elenca i consorzi in un abbonamento per una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="5ab73-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="5ab73-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ab73-110">PARAMETERS</span></span>

### <span data-ttu-id="5ab73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab73-111">-DefaultProfile</span></span>
<span data-ttu-id="5ab73-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab73-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab73-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5ab73-113">-Location</span></span>
<span data-ttu-id="5ab73-114">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="5ab73-114">Location Name.</span></span>

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

### <span data-ttu-id="5ab73-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ab73-115">-SubscriptionId</span></span>
<span data-ttu-id="5ab73-116">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab73-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ab73-117">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5ab73-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5ab73-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ab73-118">-Confirm</span></span>
<span data-ttu-id="5ab73-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ab73-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab73-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab73-120">-WhatIf</span></span>
<span data-ttu-id="5ab73-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ab73-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab73-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ab73-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab73-123">CommonParameters</span></span>
<span data-ttu-id="5ab73-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab73-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ab73-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab73-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ab73-126">INPUTS</span></span>

## <span data-ttu-id="5ab73-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ab73-127">OUTPUTS</span></span>

### <span data-ttu-id="5ab73-128">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="5ab73-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="5ab73-129">Note</span><span class="sxs-lookup"><span data-stu-id="5ab73-129">NOTES</span></span>

<span data-ttu-id="5ab73-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5ab73-130">ALIASES</span></span>

## <span data-ttu-id="5ab73-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ab73-131">RELATED LINKS</span></span>

