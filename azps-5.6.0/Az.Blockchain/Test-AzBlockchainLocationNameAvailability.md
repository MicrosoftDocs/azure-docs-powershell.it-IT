---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 9507271fe283277c212e4ed8d4117483a2797857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969661"
---
# <span data-ttu-id="28e0a-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="28e0a-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="28e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="28e0a-103">Per verificare se un nome di risorsa è disponibile.</span><span class="sxs-lookup"><span data-stu-id="28e0a-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="28e0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28e0a-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28e0a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="28e0a-105">DESCRIPTION</span></span>
<span data-ttu-id="28e0a-106">Per verificare se un nome di risorsa è disponibile.</span><span class="sxs-lookup"><span data-stu-id="28e0a-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="28e0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28e0a-107">EXAMPLES</span></span>

### <span data-ttu-id="28e0a-108">Esempio 1: Verificare la disponibilità di un nome di risorsa</span><span class="sxs-lookup"><span data-stu-id="28e0a-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="28e0a-109">Il comando controlla se un nome di risorsa è disponibile.</span><span class="sxs-lookup"><span data-stu-id="28e0a-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="28e0a-110">Esempio 2: Verificare la disponibilità di un nome di risorsa</span><span class="sxs-lookup"><span data-stu-id="28e0a-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="28e0a-111">Il comando controlla se un nome di risorsa è disponibile.</span><span class="sxs-lookup"><span data-stu-id="28e0a-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="28e0a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28e0a-112">PARAMETERS</span></span>

### <span data-ttu-id="28e0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e0a-113">-DefaultProfile</span></span>
<span data-ttu-id="28e0a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28e0a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28e0a-115">-Location</span><span class="sxs-lookup"><span data-stu-id="28e0a-115">-Location</span></span>
<span data-ttu-id="28e0a-116">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="28e0a-116">Location Name.</span></span>

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

### <span data-ttu-id="28e0a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="28e0a-117">-Name</span></span>
<span data-ttu-id="28e0a-118">Ottiene o imposta il nome da controllare.</span><span class="sxs-lookup"><span data-stu-id="28e0a-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="28e0a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28e0a-119">-SubscriptionId</span></span>
<span data-ttu-id="28e0a-120">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="28e0a-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="28e0a-121">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="28e0a-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e0a-122">-Type</span><span class="sxs-lookup"><span data-stu-id="28e0a-122">-Type</span></span>
<span data-ttu-id="28e0a-123">Ottiene o imposta il tipo di risorsa da controllare.</span><span class="sxs-lookup"><span data-stu-id="28e0a-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="28e0a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28e0a-124">-Confirm</span></span>
<span data-ttu-id="28e0a-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28e0a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28e0a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e0a-126">-WhatIf</span></span>
<span data-ttu-id="28e0a-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28e0a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28e0a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28e0a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28e0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e0a-129">CommonParameters</span></span>
<span data-ttu-id="28e0a-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28e0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e0a-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28e0a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e0a-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="28e0a-132">INPUTS</span></span>

## <span data-ttu-id="28e0a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28e0a-133">OUTPUTS</span></span>

### <span data-ttu-id="28e0a-134">Microsoft.Azure.PowerShell.Cmdlets.Gateway.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="28e0a-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="28e0a-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="28e0a-135">NOTES</span></span>

<span data-ttu-id="28e0a-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="28e0a-136">ALIASES</span></span>

## <span data-ttu-id="28e0a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28e0a-137">RELATED LINKS</span></span>

