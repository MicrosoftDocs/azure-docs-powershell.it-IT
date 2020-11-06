---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520824"
---
# <span data-ttu-id="87f35-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="87f35-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="87f35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87f35-102">SYNOPSIS</span></span>
<span data-ttu-id="87f35-103">Ottiene abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="87f35-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87f35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87f35-104">SYNTAX</span></span>

### <span data-ttu-id="87f35-105">Ottenere tutti gli abbonamenti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87f35-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87f35-106">Ottieni per subsctiption ID</span><span class="sxs-lookup"><span data-stu-id="87f35-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87f35-107">Ottieni per ID utente</span><span class="sxs-lookup"><span data-stu-id="87f35-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87f35-108">Ottenere per ID prodotto</span><span class="sxs-lookup"><span data-stu-id="87f35-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87f35-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87f35-109">DESCRIPTION</span></span>
<span data-ttu-id="87f35-110">Il cmdlet **Get-AzureRmApiManagementSubscription** ottiene un abbonamento specificato o tutti gli abbonamenti, se non è specificato alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="87f35-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="87f35-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87f35-111">EXAMPLES</span></span>

### <span data-ttu-id="87f35-112">Esempio 1: ottenere tutte le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="87f35-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="87f35-113">Questo comando consente di ottenere tutte le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="87f35-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="87f35-114">Esempio 2: ottenere un abbonamento con un ID specificato</span><span class="sxs-lookup"><span data-stu-id="87f35-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="87f35-115">Questo comando ottiene un abbonamento per ID.</span><span class="sxs-lookup"><span data-stu-id="87f35-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="87f35-116">Esempio 3: ottenere tutti gli abbonamenti per un utente</span><span class="sxs-lookup"><span data-stu-id="87f35-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="87f35-117">Questo comando ottiene le sottoscrizioni di un utente.</span><span class="sxs-lookup"><span data-stu-id="87f35-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="87f35-118">Esempio 4: ottenere tutti gli abbonamenti per un prodotto</span><span class="sxs-lookup"><span data-stu-id="87f35-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="87f35-119">Questo comando consente di ottenere tutte le sottoscrizioni per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="87f35-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="87f35-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87f35-120">PARAMETERS</span></span>

### <span data-ttu-id="87f35-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="87f35-121">-Context</span></span>
<span data-ttu-id="87f35-122">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="87f35-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f35-123">-ProductId</span><span class="sxs-lookup"><span data-stu-id="87f35-123">-ProductId</span></span>
<span data-ttu-id="87f35-124">Specifica un identificatore di prodotto.</span><span class="sxs-lookup"><span data-stu-id="87f35-124">Specifies a product identifier.</span></span>
<span data-ttu-id="87f35-125">Se specificato, questo cmdlet trova tutte le sottoscrizioni dall'identificatore del prodotto.</span><span class="sxs-lookup"><span data-stu-id="87f35-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f35-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87f35-126">-SubscriptionId</span></span>
<span data-ttu-id="87f35-127">Specifica un identificatore di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="87f35-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="87f35-128">Se specificato, questo cmdlet trova l'abbonamento dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="87f35-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f35-129">-UserId</span><span class="sxs-lookup"><span data-stu-id="87f35-129">-UserId</span></span>
<span data-ttu-id="87f35-130">Specifica un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="87f35-130">Specifies a user identifier.</span></span>
<span data-ttu-id="87f35-131">Se specificato, questo cmdlet trova tutte le sottoscrizioni dall'identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="87f35-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f35-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f35-132">-DefaultProfile</span></span>
<span data-ttu-id="87f35-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87f35-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87f35-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f35-134">CommonParameters</span></span>
<span data-ttu-id="87f35-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87f35-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f35-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87f35-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f35-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87f35-137">INPUTS</span></span>

## <span data-ttu-id="87f35-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87f35-138">OUTPUTS</span></span>

### <span data-ttu-id="87f35-139">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="87f35-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="87f35-140">Note</span><span class="sxs-lookup"><span data-stu-id="87f35-140">NOTES</span></span>

## <span data-ttu-id="87f35-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87f35-141">RELATED LINKS</span></span>

[<span data-ttu-id="87f35-142">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="87f35-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="87f35-143">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="87f35-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="87f35-144">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="87f35-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


