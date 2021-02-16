---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177959"
---
# <span data-ttu-id="edc0b-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="edc0b-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="edc0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edc0b-102">SYNOPSIS</span></span>
<span data-ttu-id="edc0b-103">Elenca le chiavi API di un membro member di member member di member member.</span><span class="sxs-lookup"><span data-stu-id="edc0b-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="edc0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edc0b-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="edc0b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="edc0b-105">DESCRIPTION</span></span>
<span data-ttu-id="edc0b-106">Elenca le chiavi API di un membro member di member member di member member.</span><span class="sxs-lookup"><span data-stu-id="edc0b-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="edc0b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edc0b-107">EXAMPLES</span></span>

### <span data-ttu-id="edc0b-108">Esempio 1: Elencare le chiavi API api api di api api primarie</span><span class="sxs-lookup"><span data-stu-id="edc0b-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="edc0b-109">Questo comando elenca le chiavi API per un membro di team team.</span><span class="sxs-lookup"><span data-stu-id="edc0b-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="edc0b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edc0b-110">PARAMETERS</span></span>

### <span data-ttu-id="edc0b-111">-MemberName</span><span class="sxs-lookup"><span data-stu-id="edc0b-111">-BlockchainMemberName</span></span>
<span data-ttu-id="edc0b-112">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="edc0b-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="edc0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc0b-113">-DefaultProfile</span></span>
<span data-ttu-id="edc0b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="edc0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc0b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc0b-115">-ResourceGroupName</span></span>
<span data-ttu-id="edc0b-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="edc0b-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="edc0b-117">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="edc0b-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="edc0b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="edc0b-118">-SubscriptionId</span></span>
<span data-ttu-id="edc0b-119">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="edc0b-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="edc0b-120">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="edc0b-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="edc0b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edc0b-121">-Confirm</span></span>
<span data-ttu-id="edc0b-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edc0b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edc0b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc0b-123">-WhatIf</span></span>
<span data-ttu-id="edc0b-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edc0b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edc0b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edc0b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edc0b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc0b-126">CommonParameters</span></span>
<span data-ttu-id="edc0b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edc0b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc0b-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="edc0b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc0b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="edc0b-129">INPUTS</span></span>

## <span data-ttu-id="edc0b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edc0b-130">OUTPUTS</span></span>

### <span data-ttu-id="edc0b-131">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="edc0b-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="edc0b-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="edc0b-132">NOTES</span></span>

<span data-ttu-id="edc0b-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="edc0b-133">ALIASES</span></span>

## <span data-ttu-id="edc0b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edc0b-134">RELATED LINKS</span></span>

