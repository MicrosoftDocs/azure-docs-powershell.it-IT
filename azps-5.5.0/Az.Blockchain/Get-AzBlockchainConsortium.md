---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181967"
---
# <span data-ttu-id="922f1-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="922f1-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="922f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="922f1-102">SYNOPSIS</span></span>
<span data-ttu-id="922f1-103">Elenca i consorzi disponibili per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="922f1-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="922f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="922f1-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="922f1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="922f1-105">DESCRIPTION</span></span>
<span data-ttu-id="922f1-106">Elenca i consorzi disponibili per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="922f1-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="922f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="922f1-107">EXAMPLES</span></span>

### <span data-ttu-id="922f1-108">Esempio 1: Creare un consorzio Dieresi.</span><span class="sxs-lookup"><span data-stu-id="922f1-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="922f1-109">Questo comando elenca i consorzi nell'ambito di una sottoscrizione per una località specifica.</span><span class="sxs-lookup"><span data-stu-id="922f1-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="922f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="922f1-110">PARAMETERS</span></span>

### <span data-ttu-id="922f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922f1-111">-DefaultProfile</span></span>
<span data-ttu-id="922f1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="922f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="922f1-113">-Location</span><span class="sxs-lookup"><span data-stu-id="922f1-113">-Location</span></span>
<span data-ttu-id="922f1-114">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="922f1-114">Location Name.</span></span>

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

### <span data-ttu-id="922f1-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="922f1-115">-SubscriptionId</span></span>
<span data-ttu-id="922f1-116">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="922f1-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="922f1-117">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="922f1-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="922f1-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="922f1-118">-Confirm</span></span>
<span data-ttu-id="922f1-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="922f1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922f1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922f1-120">-WhatIf</span></span>
<span data-ttu-id="922f1-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="922f1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922f1-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="922f1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922f1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922f1-123">CommonParameters</span></span>
<span data-ttu-id="922f1-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922f1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922f1-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="922f1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922f1-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="922f1-126">INPUTS</span></span>

## <span data-ttu-id="922f1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="922f1-127">OUTPUTS</span></span>

### <span data-ttu-id="922f1-128">Microsoft.Azure.PowerShell.Cmdlets.Cui.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="922f1-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="922f1-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="922f1-129">NOTES</span></span>

<span data-ttu-id="922f1-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="922f1-130">ALIASES</span></span>

## <span data-ttu-id="922f1-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="922f1-131">RELATED LINKS</span></span>

