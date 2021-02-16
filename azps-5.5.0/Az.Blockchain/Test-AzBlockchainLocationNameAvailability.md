---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177935"
---
# <span data-ttu-id="f8279-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f8279-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="f8279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8279-102">SYNOPSIS</span></span>
<span data-ttu-id="f8279-103">Per verificare se un nome di risorsa è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f8279-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="f8279-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8279-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8279-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8279-105">DESCRIPTION</span></span>
<span data-ttu-id="f8279-106">Per verificare se un nome di risorsa è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f8279-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="f8279-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8279-107">EXAMPLES</span></span>

### <span data-ttu-id="f8279-108">Esempio 1: Verificare la disponibilità di un nome di risorsa</span><span class="sxs-lookup"><span data-stu-id="f8279-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="f8279-109">Il comando controlla se un nome di risorsa è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f8279-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="f8279-110">Esempio 2: Verificare la disponibilità di un nome di risorsa</span><span class="sxs-lookup"><span data-stu-id="f8279-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="f8279-111">Il comando controlla se un nome di risorsa è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f8279-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="f8279-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8279-112">PARAMETERS</span></span>

### <span data-ttu-id="f8279-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8279-113">-DefaultProfile</span></span>
<span data-ttu-id="f8279-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8279-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8279-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f8279-115">-Location</span></span>
<span data-ttu-id="f8279-116">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="f8279-116">Location Name.</span></span>

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

### <span data-ttu-id="f8279-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f8279-117">-Name</span></span>
<span data-ttu-id="f8279-118">Ottiene o imposta il nome da controllare.</span><span class="sxs-lookup"><span data-stu-id="f8279-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="f8279-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8279-119">-SubscriptionId</span></span>
<span data-ttu-id="f8279-120">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f8279-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8279-121">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f8279-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f8279-122">-Type</span><span class="sxs-lookup"><span data-stu-id="f8279-122">-Type</span></span>
<span data-ttu-id="f8279-123">Ottiene o imposta il tipo di risorsa da controllare.</span><span class="sxs-lookup"><span data-stu-id="f8279-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="f8279-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8279-124">-Confirm</span></span>
<span data-ttu-id="f8279-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8279-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8279-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8279-126">-WhatIf</span></span>
<span data-ttu-id="f8279-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8279-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8279-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8279-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8279-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8279-129">CommonParameters</span></span>
<span data-ttu-id="f8279-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8279-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8279-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8279-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8279-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8279-132">INPUTS</span></span>

## <span data-ttu-id="f8279-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8279-133">OUTPUTS</span></span>

### <span data-ttu-id="f8279-134">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="f8279-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="f8279-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8279-135">NOTES</span></span>

<span data-ttu-id="f8279-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f8279-136">ALIASES</span></span>

## <span data-ttu-id="f8279-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8279-137">RELATED LINKS</span></span>

