---
external help file: Microsoft.Azure.Commands.Subscription.dll-Help.xml
Module Name: AzureRM.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription/new-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
ms.openlocfilehash: cc88f762f1e965eb4e46462f7d43074fa3fe4646
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521288"
---
# <span data-ttu-id="44976-101">New-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="44976-101">New-AzureRmSubscription</span></span>

## <span data-ttu-id="44976-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44976-102">SYNOPSIS</span></span>
<span data-ttu-id="44976-103">Crea un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="44976-103">Creates an Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44976-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44976-104">SYNTAX</span></span>

```
New-AzureRmSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44976-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44976-105">DESCRIPTION</span></span>
<span data-ttu-id="44976-106">Il cmdlet **New-AzureRmSubscription** crea un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="44976-106">The **New-AzureRmSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="44976-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44976-107">EXAMPLES</span></span>

### <span data-ttu-id="44976-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44976-108">Example 1</span></span>
```
PS C:\> New-AzureRmSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzureRmEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="44976-109">Crea un abbonamento a Azure sotto l'account di registrazione specificato con il tipo di offerta specificato.</span><span class="sxs-lookup"><span data-stu-id="44976-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="44976-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44976-110">PARAMETERS</span></span>

### <span data-ttu-id="44976-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44976-111">-AsJob</span></span>
<span data-ttu-id="44976-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="44976-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44976-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44976-113">-DefaultProfile</span></span>
<span data-ttu-id="44976-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44976-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44976-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="44976-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="44976-116">Nome dell'account di registrazione da usare durante la creazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="44976-116">Name of the enrollment account to use when creating the subscription.</span></span>

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

### <span data-ttu-id="44976-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="44976-117">-Name</span></span>
<span data-ttu-id="44976-118">Nome della sottoscrizione da creare.</span><span class="sxs-lookup"><span data-stu-id="44976-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44976-119">-OfferType</span><span class="sxs-lookup"><span data-stu-id="44976-119">-OfferType</span></span>
<span data-ttu-id="44976-120">Tipo di offerta da usare durante la creazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="44976-120">The type of offer to use when creating the subscription.</span></span>

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

### <span data-ttu-id="44976-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="44976-121">-OwnerApplicationId</span></span>
<span data-ttu-id="44976-122">Il nome SPN dell'app a cui concedere l'accesso proprietario all'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="44976-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44976-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="44976-123">-OwnerObjectId</span></span>
<span data-ttu-id="44976-124">Gli utenti o gli ID o gli oggetti gruppo (s) a cui viene concesso l'accesso proprietario all'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="44976-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44976-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="44976-125">-OwnerSignInName</span></span>
<span data-ttu-id="44976-126">L'utente o gli utenti a cui concedere l'accesso al proprietario per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="44976-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44976-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44976-127">-Confirm</span></span>
<span data-ttu-id="44976-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44976-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44976-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44976-129">-WhatIf</span></span>
<span data-ttu-id="44976-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44976-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44976-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44976-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44976-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44976-132">CommonParameters</span></span>
<span data-ttu-id="44976-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44976-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44976-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44976-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44976-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44976-135">INPUTS</span></span>

### <span data-ttu-id="44976-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="44976-136">None</span></span>

## <span data-ttu-id="44976-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44976-137">OUTPUTS</span></span>

### <span data-ttu-id="44976-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="44976-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="44976-139">Note</span><span class="sxs-lookup"><span data-stu-id="44976-139">NOTES</span></span>

## <span data-ttu-id="44976-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44976-140">RELATED LINKS</span></span>
