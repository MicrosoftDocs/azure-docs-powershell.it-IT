---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191655"
---
# <span data-ttu-id="a962e-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a962e-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="a962e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a962e-102">SYNOPSIS</span></span>
<span data-ttu-id="a962e-103">Per verificare se è disponibile un nome di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a962e-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="a962e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a962e-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a962e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a962e-105">DESCRIPTION</span></span>
<span data-ttu-id="a962e-106">Per verificare se è disponibile un nome di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a962e-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="a962e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a962e-107">EXAMPLES</span></span>

### <span data-ttu-id="a962e-108">Esempio 1: verificare se il nome di una risorsa è disponibile</span><span class="sxs-lookup"><span data-stu-id="a962e-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="a962e-109">Il comando verifica se è disponibile un nome di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a962e-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="a962e-110">Esempio 2: verificare se il nome di una risorsa è disponibile</span><span class="sxs-lookup"><span data-stu-id="a962e-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="a962e-111">Il comando verifica se è disponibile un nome di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a962e-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="a962e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a962e-112">PARAMETERS</span></span>

### <span data-ttu-id="a962e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a962e-113">-DefaultProfile</span></span>
<span data-ttu-id="a962e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a962e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a962e-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a962e-115">-Location</span></span>
<span data-ttu-id="a962e-116">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="a962e-116">Location Name.</span></span>

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

### <span data-ttu-id="a962e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a962e-117">-Name</span></span>
<span data-ttu-id="a962e-118">Ottiene o imposta il nome da controllare.</span><span class="sxs-lookup"><span data-stu-id="a962e-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="a962e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a962e-119">-SubscriptionId</span></span>
<span data-ttu-id="a962e-120">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a962e-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a962e-121">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a962e-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a962e-122">-Digitare</span><span class="sxs-lookup"><span data-stu-id="a962e-122">-Type</span></span>
<span data-ttu-id="a962e-123">Ottiene o imposta il tipo della risorsa da controllare.</span><span class="sxs-lookup"><span data-stu-id="a962e-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="a962e-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a962e-124">-Confirm</span></span>
<span data-ttu-id="a962e-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a962e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a962e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a962e-126">-WhatIf</span></span>
<span data-ttu-id="a962e-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a962e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a962e-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a962e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a962e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a962e-129">CommonParameters</span></span>
<span data-ttu-id="a962e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a962e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a962e-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a962e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a962e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a962e-132">INPUTS</span></span>

## <span data-ttu-id="a962e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a962e-133">OUTPUTS</span></span>

### <span data-ttu-id="a962e-134">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. INameAvailability</span><span class="sxs-lookup"><span data-stu-id="a962e-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="a962e-135">Note</span><span class="sxs-lookup"><span data-stu-id="a962e-135">NOTES</span></span>

<span data-ttu-id="a962e-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a962e-136">ALIASES</span></span>

## <span data-ttu-id="a962e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a962e-137">RELATED LINKS</span></span>

