---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673625"
---
# <span data-ttu-id="47292-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="47292-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="47292-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47292-102">SYNOPSIS</span></span>
<span data-ttu-id="47292-103">Ottiene abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="47292-103">Gets subscriptions.</span></span>

## <span data-ttu-id="47292-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47292-104">SYNTAX</span></span>

### <span data-ttu-id="47292-105">GetAllSubscriptions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47292-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47292-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47292-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47292-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="47292-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47292-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="47292-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47292-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47292-109">DESCRIPTION</span></span>
<span data-ttu-id="47292-110">Il cmdlet **Get-AzApiManagementSubscription** ottiene un abbonamento specificato o tutti gli abbonamenti, se non è specificato alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="47292-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="47292-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47292-111">EXAMPLES</span></span>

### <span data-ttu-id="47292-112">Esempio 1: ottenere tutte le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="47292-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="47292-113">Questo comando consente di ottenere tutte le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="47292-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="47292-114">Esempio 2: ottenere un abbonamento con un ID specificato</span><span class="sxs-lookup"><span data-stu-id="47292-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="47292-115">Questo comando ottiene un abbonamento per ID.</span><span class="sxs-lookup"><span data-stu-id="47292-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="47292-116">Esempio 3: ottenere tutti gli abbonamenti per un utente</span><span class="sxs-lookup"><span data-stu-id="47292-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="47292-117">Questo comando ottiene le sottoscrizioni di un utente.</span><span class="sxs-lookup"><span data-stu-id="47292-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="47292-118">Esempio 4: ottenere tutti gli abbonamenti per un prodotto</span><span class="sxs-lookup"><span data-stu-id="47292-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="47292-119">Questo comando consente di ottenere tutte le sottoscrizioni per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="47292-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="47292-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47292-120">PARAMETERS</span></span>

### <span data-ttu-id="47292-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="47292-121">-Context</span></span>
<span data-ttu-id="47292-122">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="47292-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="47292-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47292-123">-DefaultProfile</span></span>
<span data-ttu-id="47292-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47292-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47292-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="47292-125">-ProductId</span></span>
<span data-ttu-id="47292-126">Specifica un identificatore di prodotto.</span><span class="sxs-lookup"><span data-stu-id="47292-126">Specifies a product identifier.</span></span>
<span data-ttu-id="47292-127">Se specificato, questo cmdlet trova tutte le sottoscrizioni dall'identificatore del prodotto.</span><span class="sxs-lookup"><span data-stu-id="47292-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="47292-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47292-128">-SubscriptionId</span></span>
<span data-ttu-id="47292-129">Specifica un identificatore di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="47292-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="47292-130">Se specificato, questo cmdlet trova l'abbonamento dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="47292-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="47292-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="47292-131">-UserId</span></span>
<span data-ttu-id="47292-132">Specifica un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="47292-132">Specifies a user identifier.</span></span>
<span data-ttu-id="47292-133">Se specificato, questo cmdlet trova tutte le sottoscrizioni dall'identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="47292-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="47292-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47292-134">CommonParameters</span></span>
<span data-ttu-id="47292-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47292-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47292-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47292-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47292-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47292-137">INPUTS</span></span>

### <span data-ttu-id="47292-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47292-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47292-139">System. String</span><span class="sxs-lookup"><span data-stu-id="47292-139">System.String</span></span>

## <span data-ttu-id="47292-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47292-140">OUTPUTS</span></span>

### <span data-ttu-id="47292-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="47292-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="47292-142">Note</span><span class="sxs-lookup"><span data-stu-id="47292-142">NOTES</span></span>

## <span data-ttu-id="47292-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47292-143">RELATED LINKS</span></span>

[<span data-ttu-id="47292-144">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="47292-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="47292-145">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="47292-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="47292-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="47292-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


