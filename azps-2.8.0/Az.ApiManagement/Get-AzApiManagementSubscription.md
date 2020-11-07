---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676052"
---
# <span data-ttu-id="cf2de-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cf2de-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="cf2de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf2de-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2de-103">Ottiene abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="cf2de-103">Gets subscriptions.</span></span>

## <span data-ttu-id="cf2de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf2de-104">SYNTAX</span></span>

### <span data-ttu-id="cf2de-105">GetAllSubscriptions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf2de-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf2de-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf2de-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf2de-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="cf2de-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf2de-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="cf2de-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf2de-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="cf2de-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf2de-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="cf2de-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf2de-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf2de-111">DESCRIPTION</span></span>
<span data-ttu-id="cf2de-112">Il cmdlet **Get-AzApiManagementSubscription** ottiene un abbonamento specificato o tutti gli abbonamenti, se non è specificato alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cf2de-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="cf2de-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf2de-113">EXAMPLES</span></span>

### <span data-ttu-id="cf2de-114">Esempio 1: ottenere tutte le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="cf2de-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="cf2de-115">Questo comando consente di ottenere tutte le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="cf2de-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="cf2de-116">Esempio 2: ottenere un abbonamento con un ID specificato</span><span class="sxs-lookup"><span data-stu-id="cf2de-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="cf2de-117">Questo comando ottiene un abbonamento per ID.</span><span class="sxs-lookup"><span data-stu-id="cf2de-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="cf2de-118">Esempio 3: ottenere tutti gli abbonamenti per un utente</span><span class="sxs-lookup"><span data-stu-id="cf2de-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="cf2de-119">Questo comando ottiene le sottoscrizioni di un utente.</span><span class="sxs-lookup"><span data-stu-id="cf2de-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="cf2de-120">Esempio 4: ottenere tutti gli abbonamenti per un prodotto</span><span class="sxs-lookup"><span data-stu-id="cf2de-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="cf2de-121">Questo comando consente di ottenere tutte le sottoscrizioni per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="cf2de-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="cf2de-122">Esempio 5: ottenere tutti gli abbonamenti per un ambito</span><span class="sxs-lookup"><span data-stu-id="cf2de-122">Example 5: Get all subscriptions for a Scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="cf2de-123">Questo comando consente di ottenere tutte le sottoscrizioni configurate per l'ambito API globale</span><span class="sxs-lookup"><span data-stu-id="cf2de-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="cf2de-124">Esempio 5: ottenere tutti gli abbonamenti per un prodotto e un ambito utente</span><span class="sxs-lookup"><span data-stu-id="cf2de-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="cf2de-125">Questo comando consente di ottenere tutte le sottoscrizioni configurate per l'ambito API globale</span><span class="sxs-lookup"><span data-stu-id="cf2de-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="cf2de-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf2de-126">PARAMETERS</span></span>

### <span data-ttu-id="cf2de-127">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cf2de-127">-Context</span></span>
<span data-ttu-id="cf2de-128">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cf2de-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2de-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2de-129">-DefaultProfile</span></span>
<span data-ttu-id="cf2de-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2de-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf2de-131">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cf2de-131">-ProductId</span></span>
<span data-ttu-id="cf2de-132">Specifica un identificatore di prodotto.</span><span class="sxs-lookup"><span data-stu-id="cf2de-132">Specifies a product identifier.</span></span>
<span data-ttu-id="cf2de-133">Se specificato, questo cmdlet trova tutte le sottoscrizioni dall'identificatore del prodotto.</span><span class="sxs-lookup"><span data-stu-id="cf2de-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="cf2de-134">-Ambito</span><span class="sxs-lookup"><span data-stu-id="cf2de-134">-Scope</span></span>
<span data-ttu-id="cf2de-135">Identificatore ambito.</span><span class="sxs-lookup"><span data-stu-id="cf2de-135">Scope identifier.</span></span> <span data-ttu-id="cf2de-136">L'ambito della sottoscrizione, sia che si tratti di ambito API/apis/{apiId} o ambito prodotto/products/{productId} o ambito API globale/Apis o ambito globale/.</span><span class="sxs-lookup"><span data-stu-id="cf2de-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2de-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf2de-137">-SubscriptionId</span></span>
<span data-ttu-id="cf2de-138">Specifica un identificatore di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cf2de-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="cf2de-139">Se specificato, questo cmdlet trova l'abbonamento dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="cf2de-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="cf2de-140">-UserId</span><span class="sxs-lookup"><span data-stu-id="cf2de-140">-UserId</span></span>
<span data-ttu-id="cf2de-141">Specifica un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="cf2de-141">Specifies a user identifier.</span></span>
<span data-ttu-id="cf2de-142">Se specificato, questo cmdlet trova tutte le sottoscrizioni dall'identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="cf2de-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="cf2de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2de-143">CommonParameters</span></span>
<span data-ttu-id="cf2de-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2de-145">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf2de-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2de-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf2de-146">INPUTS</span></span>

### <span data-ttu-id="cf2de-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cf2de-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cf2de-148">System. String</span><span class="sxs-lookup"><span data-stu-id="cf2de-148">System.String</span></span>

## <span data-ttu-id="cf2de-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf2de-149">OUTPUTS</span></span>

### <span data-ttu-id="cf2de-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cf2de-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="cf2de-151">Note</span><span class="sxs-lookup"><span data-stu-id="cf2de-151">NOTES</span></span>

## <span data-ttu-id="cf2de-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf2de-152">RELATED LINKS</span></span>

[<span data-ttu-id="cf2de-153">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cf2de-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="cf2de-154">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cf2de-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="cf2de-155">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cf2de-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


