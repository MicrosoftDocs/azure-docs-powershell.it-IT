---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: e3400ea600ed2891101a94f9ec1a7853326a7c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187711"
---
# <span data-ttu-id="e1d95-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e1d95-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="e1d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d95-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d95-103">Ottiene abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="e1d95-103">Gets subscriptions.</span></span>

## <span data-ttu-id="e1d95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1d95-104">SYNTAX</span></span>

### <span data-ttu-id="e1d95-105">GetAllSubscriptions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1d95-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1d95-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1d95-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1d95-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="e1d95-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1d95-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="e1d95-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1d95-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e1d95-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1d95-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="e1d95-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d95-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1d95-111">DESCRIPTION</span></span>
<span data-ttu-id="e1d95-112">Il cmdlet **Get-AzApiManagementSubscription** ottiene una sottoscrizione specificata o tutte le sottoscrizioni, se non è specificato alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e1d95-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="e1d95-113">Le chiavi non verranno incluse nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="e1d95-113">Keys will not be included into result details.</span></span> <span data-ttu-id="e1d95-114">Per ottenere le chiavi, usare **Get-AzApiManagementSubscriptionKey.**</span><span class="sxs-lookup"><span data-stu-id="e1d95-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="e1d95-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1d95-115">EXAMPLES</span></span>

### <span data-ttu-id="e1d95-116">Esempio 1: Ottenere tutti gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="e1d95-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="e1d95-117">Questo comando recupera tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="e1d95-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="e1d95-118">Esempio 2: Ottenere un abbonamento con un ID specificato</span><span class="sxs-lookup"><span data-stu-id="e1d95-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="e1d95-119">Questo comando ottiene un abbonamento in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="e1d95-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="e1d95-120">Esempio 3: Ottenere tutte le sottoscrizioni per un utente</span><span class="sxs-lookup"><span data-stu-id="e1d95-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="e1d95-121">Questo comando recupera le sottoscrizioni di un utente.</span><span class="sxs-lookup"><span data-stu-id="e1d95-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="e1d95-122">Esempio 4: Ottenere tutti gli abbonamenti per un prodotto</span><span class="sxs-lookup"><span data-stu-id="e1d95-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="e1d95-123">Questo comando recupera tutte le sottoscrizioni per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="e1d95-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="e1d95-124">Esempio 5: Ottenere tutte le sottoscrizioni per un ambito</span><span class="sxs-lookup"><span data-stu-id="e1d95-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
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

<span data-ttu-id="e1d95-125">Questo comando recupera tutte le sottoscrizioni configurate per l'ambito api globale</span><span class="sxs-lookup"><span data-stu-id="e1d95-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="e1d95-126">Esempio 6: Ottenere tutte le sottoscrizioni per un prodotto e un ambito utente</span><span class="sxs-lookup"><span data-stu-id="e1d95-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
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

<span data-ttu-id="e1d95-127">Questo comando recupera tutte le sottoscrizioni configurate per l'ambito api globale</span><span class="sxs-lookup"><span data-stu-id="e1d95-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="e1d95-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1d95-128">PARAMETERS</span></span>

### <span data-ttu-id="e1d95-129">-Context</span><span class="sxs-lookup"><span data-stu-id="e1d95-129">-Context</span></span>
<span data-ttu-id="e1d95-130">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e1d95-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e1d95-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d95-131">-DefaultProfile</span></span>
<span data-ttu-id="e1d95-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d95-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d95-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e1d95-133">-ProductId</span></span>
<span data-ttu-id="e1d95-134">Specifica un identificatore di prodotto.</span><span class="sxs-lookup"><span data-stu-id="e1d95-134">Specifies a product identifier.</span></span>
<span data-ttu-id="e1d95-135">Se specificato, questo cmdlet trova tutte le sottoscrizioni in base all'identificatore prodotto.</span><span class="sxs-lookup"><span data-stu-id="e1d95-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="e1d95-136">-Scope</span><span class="sxs-lookup"><span data-stu-id="e1d95-136">-Scope</span></span>
<span data-ttu-id="e1d95-137">Identificatore di ambito.</span><span class="sxs-lookup"><span data-stu-id="e1d95-137">Scope identifier.</span></span> <span data-ttu-id="e1d95-138">Ambito della sottoscrizione, che si tratta di Ambito API /api/{apiId} o Ambito prodotto /products/{productId} o Ambito API globale /api o Ambito globale /.</span><span class="sxs-lookup"><span data-stu-id="e1d95-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="e1d95-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1d95-139">-SubscriptionId</span></span>
<span data-ttu-id="e1d95-140">Specifica un identificatore di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e1d95-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="e1d95-141">Se specificato, questo cmdlet trova la sottoscrizione in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="e1d95-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="e1d95-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="e1d95-142">-UserId</span></span>
<span data-ttu-id="e1d95-143">Specifica un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="e1d95-143">Specifies a user identifier.</span></span>
<span data-ttu-id="e1d95-144">Se specificato, questo cmdlet trova tutte le sottoscrizioni in base all'identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="e1d95-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="e1d95-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d95-145">CommonParameters</span></span>
<span data-ttu-id="e1d95-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d95-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d95-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1d95-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d95-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1d95-148">INPUTS</span></span>

### <span data-ttu-id="e1d95-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e1d95-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e1d95-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e1d95-150">System.String</span></span>

## <span data-ttu-id="e1d95-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1d95-151">OUTPUTS</span></span>

### <span data-ttu-id="e1d95-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e1d95-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="e1d95-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1d95-153">NOTES</span></span>

## <span data-ttu-id="e1d95-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1d95-154">RELATED LINKS</span></span>

[<span data-ttu-id="e1d95-155">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e1d95-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="e1d95-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e1d95-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="e1d95-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e1d95-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


