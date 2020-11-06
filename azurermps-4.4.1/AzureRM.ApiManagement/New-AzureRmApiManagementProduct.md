---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: a978fce4d44a061796597f2f3ae08c78c1021bdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517188"
---
# <span data-ttu-id="74c54-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="74c54-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="74c54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74c54-102">SYNOPSIS</span></span>
<span data-ttu-id="74c54-103">Crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="74c54-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74c54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74c54-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74c54-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74c54-105">DESCRIPTION</span></span>
<span data-ttu-id="74c54-106">Il cmdlet **New-AzureRmApiManagementProduct** crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="74c54-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="74c54-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74c54-107">EXAMPLES</span></span>

### <span data-ttu-id="74c54-108">Esempio 1: creare un prodotto che non richiede un abbonamento</span><span class="sxs-lookup"><span data-stu-id="74c54-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="74c54-109">Questo comando crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="74c54-109">This command creates an API Management product.</span></span>
<span data-ttu-id="74c54-110">Non è necessario alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="74c54-110">No subscription is required.</span></span>

### <span data-ttu-id="74c54-111">Esempio 2: creare un prodotto che richiede un abbonamento e l'approvazione</span><span class="sxs-lookup"><span data-stu-id="74c54-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="74c54-112">Questo comando crea un prodotto.</span><span class="sxs-lookup"><span data-stu-id="74c54-112">This command creates a product.</span></span>
<span data-ttu-id="74c54-113">È necessario un abbonamento e l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="74c54-113">A subscription and approval are required.</span></span>
<span data-ttu-id="74c54-114">Questo comando imposta il periodo di notifica su 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="74c54-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="74c54-115">La durata dell'abbonamento è impostata su un anno.</span><span class="sxs-lookup"><span data-stu-id="74c54-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="74c54-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74c54-116">PARAMETERS</span></span>

### <span data-ttu-id="74c54-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="74c54-117">-ApprovalRequired</span></span>
<span data-ttu-id="74c54-118">Indica se l'abbonamento al prodotto richiede l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="74c54-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="74c54-119">Per impostazione predefinita, questo parametro è **$false**.</span><span class="sxs-lookup"><span data-stu-id="74c54-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="74c54-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="74c54-120">-Context</span></span>
<span data-ttu-id="74c54-121">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="74c54-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="74c54-122">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="74c54-122">-Description</span></span>
<span data-ttu-id="74c54-123">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="74c54-123">Specifies the product description.</span></span>

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

### <span data-ttu-id="74c54-124">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="74c54-124">-LegalTerms</span></span>
<span data-ttu-id="74c54-125">Specifica le condizioni legali per l'uso del prodotto.</span><span class="sxs-lookup"><span data-stu-id="74c54-125">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="74c54-126">-ProductId</span><span class="sxs-lookup"><span data-stu-id="74c54-126">-ProductId</span></span>
<span data-ttu-id="74c54-127">Specifica l'identificatore del nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="74c54-127">Specifies the identifier of new product.</span></span>
<span data-ttu-id="74c54-128">Se non specifichi questo parametro, viene generato un nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="74c54-128">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="74c54-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="74c54-129">-State</span></span>
<span data-ttu-id="74c54-130">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="74c54-130">Specifies the product state.</span></span>
<span data-ttu-id="74c54-131">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="74c54-131">psdx_paramvalues</span></span>

- <span data-ttu-id="74c54-132">NotPublished</span><span class="sxs-lookup"><span data-stu-id="74c54-132">NotPublished</span></span>
- <span data-ttu-id="74c54-133">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="74c54-133">Published</span></span> 

<span data-ttu-id="74c54-134">Il valore predefinito è NotPublished.</span><span class="sxs-lookup"><span data-stu-id="74c54-134">The default value is NotPublished.</span></span>

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

### <span data-ttu-id="74c54-135">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="74c54-135">-SubscriptionRequired</span></span>
<span data-ttu-id="74c54-136">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="74c54-136">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="74c54-137">Il valore predefinito è **$true**.</span><span class="sxs-lookup"><span data-stu-id="74c54-137">The default value is **$True**.</span></span>

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

### <span data-ttu-id="74c54-138">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="74c54-138">-SubscriptionsLimit</span></span>
<span data-ttu-id="74c54-139">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="74c54-139">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="74c54-140">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="74c54-140">The default value is 1.</span></span>

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

### <span data-ttu-id="74c54-141">-Titolo</span><span class="sxs-lookup"><span data-stu-id="74c54-141">-Title</span></span>
<span data-ttu-id="74c54-142">Specifica il titolo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="74c54-142">Specifies the product title.</span></span>

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

### <span data-ttu-id="74c54-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c54-143">-DefaultProfile</span></span>
<span data-ttu-id="74c54-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74c54-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74c54-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c54-145">CommonParameters</span></span>
<span data-ttu-id="74c54-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c54-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c54-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c54-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c54-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74c54-148">INPUTS</span></span>

## <span data-ttu-id="74c54-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74c54-149">OUTPUTS</span></span>

### <span data-ttu-id="74c54-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="74c54-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="74c54-151">Note</span><span class="sxs-lookup"><span data-stu-id="74c54-151">NOTES</span></span>

## <span data-ttu-id="74c54-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74c54-152">RELATED LINKS</span></span>

[<span data-ttu-id="74c54-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="74c54-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="74c54-154">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="74c54-154">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="74c54-155">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="74c54-155">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


