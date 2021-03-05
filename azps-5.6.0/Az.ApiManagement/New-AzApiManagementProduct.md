---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 12de4862e91555b90a4168ac7ac5908b897d6e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988524"
---
# <span data-ttu-id="8d13a-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8d13a-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="8d13a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d13a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d13a-103">Crea un prodotto di gestione API.</span><span class="sxs-lookup"><span data-stu-id="8d13a-103">Creates an API Management product.</span></span>

## <span data-ttu-id="8d13a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d13a-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d13a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d13a-105">DESCRIPTION</span></span>
<span data-ttu-id="8d13a-106">Il cmdlet **New-AzApiManagementProduct** crea un prodotto di gestione API.</span><span class="sxs-lookup"><span data-stu-id="8d13a-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="8d13a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d13a-107">EXAMPLES</span></span>

### <span data-ttu-id="8d13a-108">Esempio 1: Creare un prodotto che non richiede un abbonamento</span><span class="sxs-lookup"><span data-stu-id="8d13a-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="8d13a-109">Questo comando crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8d13a-109">This command creates an API Management product.</span></span>
<span data-ttu-id="8d13a-110">Non è richiesto alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8d13a-110">No subscription is required.</span></span>

### <span data-ttu-id="8d13a-111">Esempio 2: Creare un prodotto che richiede un abbonamento e l'approvazione</span><span class="sxs-lookup"><span data-stu-id="8d13a-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="8d13a-112">Questo comando crea un prodotto.</span><span class="sxs-lookup"><span data-stu-id="8d13a-112">This command creates a product.</span></span>
<span data-ttu-id="8d13a-113">È necessario un abbonamento e l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="8d13a-113">A subscription and approval are required.</span></span>
<span data-ttu-id="8d13a-114">Questo comando imposta il periodo di notifica su 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="8d13a-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="8d13a-115">La durata dell'abbonamento è impostata su un anno.</span><span class="sxs-lookup"><span data-stu-id="8d13a-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="8d13a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d13a-116">PARAMETERS</span></span>

### <span data-ttu-id="8d13a-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="8d13a-117">-ApprovalRequired</span></span>
<span data-ttu-id="8d13a-118">Indica se l'abbonamento al prodotto richiede o meno l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="8d13a-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="8d13a-119">Per impostazione predefinita, questo parametro è **$False.**</span><span class="sxs-lookup"><span data-stu-id="8d13a-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13a-120">-Context</span><span class="sxs-lookup"><span data-stu-id="8d13a-120">-Context</span></span>
<span data-ttu-id="8d13a-121">Specifica un'istanza di un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="8d13a-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8d13a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d13a-122">-DefaultProfile</span></span>
<span data-ttu-id="8d13a-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d13a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d13a-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d13a-124">-Description</span></span>
<span data-ttu-id="8d13a-125">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8d13a-125">Specifies the product description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13a-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="8d13a-126">-LegalTerms</span></span>
<span data-ttu-id="8d13a-127">Specifica le condizioni legali per l'utilizzo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8d13a-127">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13a-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8d13a-128">-ProductId</span></span>
<span data-ttu-id="8d13a-129">Specifica l'identificatore del nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="8d13a-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="8d13a-130">Se non si specifica questo parametro, viene generato un nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="8d13a-130">If you do not specify this parameter, a new product is generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13a-131">-State</span><span class="sxs-lookup"><span data-stu-id="8d13a-131">-State</span></span>
<span data-ttu-id="8d13a-132">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8d13a-132">Specifies the product state.</span></span>
<span data-ttu-id="8d13a-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="8d13a-133">psdx_paramvalues</span></span>
- <span data-ttu-id="8d13a-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="8d13a-134">NotPublished</span></span>
- <span data-ttu-id="8d13a-135">Pubblicato Il valore predefinito è NotPublished.</span><span class="sxs-lookup"><span data-stu-id="8d13a-135">Published The default value is NotPublished.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases:
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13a-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="8d13a-136">-SubscriptionRequired</span></span>
<span data-ttu-id="8d13a-137">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8d13a-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="8d13a-138">Il valore predefinito è **$True.**</span><span class="sxs-lookup"><span data-stu-id="8d13a-138">The default value is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13a-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="8d13a-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="8d13a-140">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="8d13a-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="8d13a-141">Il valore predefinito è Nessuno.</span><span class="sxs-lookup"><span data-stu-id="8d13a-141">The default value is None.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13a-142">-Title</span><span class="sxs-lookup"><span data-stu-id="8d13a-142">-Title</span></span>
<span data-ttu-id="8d13a-143">Specifica il titolo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8d13a-143">Specifies the product title.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d13a-144">CommonParameters</span></span>
<span data-ttu-id="8d13a-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d13a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d13a-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d13a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d13a-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d13a-147">INPUTS</span></span>

### <span data-ttu-id="8d13a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d13a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d13a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8d13a-149">System.String</span></span>

### <span data-ttu-id="8d13a-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d13a-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8d13a-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d13a-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8d13a-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8d13a-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8d13a-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d13a-153">OUTPUTS</span></span>

### <span data-ttu-id="8d13a-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8d13a-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="8d13a-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d13a-155">NOTES</span></span>

## <span data-ttu-id="8d13a-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d13a-156">RELATED LINKS</span></span>

[<span data-ttu-id="8d13a-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8d13a-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="8d13a-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8d13a-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="8d13a-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8d13a-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


