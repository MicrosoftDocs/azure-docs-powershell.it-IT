---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 8695d8866b83ed6cd7b29a3d94546da1114d3eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519790"
---
# <span data-ttu-id="29514-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="29514-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="29514-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29514-102">SYNOPSIS</span></span>
<span data-ttu-id="29514-103">Ottiene abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="29514-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29514-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29514-104">SYNTAX</span></span>

### <span data-ttu-id="29514-105">GetAllSubscriptions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29514-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29514-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29514-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29514-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="29514-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29514-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="29514-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29514-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29514-109">DESCRIPTION</span></span>
<span data-ttu-id="29514-110">Il cmdlet **Get-AzureRmApiManagementSubscription** ottiene un abbonamento specificato o tutti gli abbonamenti, se non è specificato alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="29514-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="29514-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29514-111">EXAMPLES</span></span>

### <span data-ttu-id="29514-112">Esempio 1: ottenere tutte le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="29514-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="29514-113">Questo comando consente di ottenere tutte le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="29514-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="29514-114">Esempio 2: ottenere un abbonamento con un ID specificato</span><span class="sxs-lookup"><span data-stu-id="29514-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="29514-115">Questo comando ottiene un abbonamento per ID.</span><span class="sxs-lookup"><span data-stu-id="29514-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="29514-116">Esempio 3: ottenere tutti gli abbonamenti per un utente</span><span class="sxs-lookup"><span data-stu-id="29514-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="29514-117">Questo comando ottiene le sottoscrizioni di un utente.</span><span class="sxs-lookup"><span data-stu-id="29514-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="29514-118">Esempio 4: ottenere tutti gli abbonamenti per un prodotto</span><span class="sxs-lookup"><span data-stu-id="29514-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="29514-119">Questo comando consente di ottenere tutte le sottoscrizioni per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="29514-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="29514-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29514-120">PARAMETERS</span></span>

### <span data-ttu-id="29514-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="29514-121">-Context</span></span>
<span data-ttu-id="29514-122">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="29514-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="29514-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29514-123">-DefaultProfile</span></span>
<span data-ttu-id="29514-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29514-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29514-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="29514-125">-ProductId</span></span>
<span data-ttu-id="29514-126">Specifica un identificatore di prodotto.</span><span class="sxs-lookup"><span data-stu-id="29514-126">Specifies a product identifier.</span></span>
<span data-ttu-id="29514-127">Se specificato, questo cmdlet trova tutte le sottoscrizioni dall'identificatore del prodotto.</span><span class="sxs-lookup"><span data-stu-id="29514-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29514-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29514-128">-SubscriptionId</span></span>
<span data-ttu-id="29514-129">Specifica un identificatore di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="29514-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="29514-130">Se specificato, questo cmdlet trova l'abbonamento dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="29514-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29514-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="29514-131">-UserId</span></span>
<span data-ttu-id="29514-132">Specifica un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="29514-132">Specifies a user identifier.</span></span>
<span data-ttu-id="29514-133">Se specificato, questo cmdlet trova tutte le sottoscrizioni dall'identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="29514-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29514-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29514-134">CommonParameters</span></span>
<span data-ttu-id="29514-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29514-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29514-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29514-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29514-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29514-137">INPUTS</span></span>

### <span data-ttu-id="29514-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29514-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="29514-139">System. String</span><span class="sxs-lookup"><span data-stu-id="29514-139">System.String</span></span>

## <span data-ttu-id="29514-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29514-140">OUTPUTS</span></span>

### <span data-ttu-id="29514-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="29514-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="29514-142">Note</span><span class="sxs-lookup"><span data-stu-id="29514-142">NOTES</span></span>

## <span data-ttu-id="29514-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29514-143">RELATED LINKS</span></span>

[<span data-ttu-id="29514-144">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="29514-144">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="29514-145">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="29514-145">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="29514-146">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="29514-146">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


