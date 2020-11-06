---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 673aa943263a789e7d8be0a63634ddd176e09cae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508443"
---
# <span data-ttu-id="4de71-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4de71-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="4de71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4de71-102">SYNOPSIS</span></span>
<span data-ttu-id="4de71-103">Crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="4de71-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4de71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4de71-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4de71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4de71-105">DESCRIPTION</span></span>
<span data-ttu-id="4de71-106">Il cmdlet **New-AzureRmApiManagementProduct** crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="4de71-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="4de71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4de71-107">EXAMPLES</span></span>

### <span data-ttu-id="4de71-108">Esempio 1: creare un prodotto che non richiede un abbonamento</span><span class="sxs-lookup"><span data-stu-id="4de71-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="4de71-109">Questo comando crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="4de71-109">This command creates an API Management product.</span></span>
<span data-ttu-id="4de71-110">Non è necessario alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4de71-110">No subscription is required.</span></span>

### <span data-ttu-id="4de71-111">Esempio 2: creare un prodotto che richiede un abbonamento e l'approvazione</span><span class="sxs-lookup"><span data-stu-id="4de71-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="4de71-112">Questo comando crea un prodotto.</span><span class="sxs-lookup"><span data-stu-id="4de71-112">This command creates a product.</span></span>
<span data-ttu-id="4de71-113">È necessario un abbonamento e l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="4de71-113">A subscription and approval are required.</span></span>
<span data-ttu-id="4de71-114">Questo comando imposta il periodo di notifica su 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="4de71-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="4de71-115">La durata dell'abbonamento è impostata su un anno.</span><span class="sxs-lookup"><span data-stu-id="4de71-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="4de71-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4de71-116">PARAMETERS</span></span>

### <span data-ttu-id="4de71-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="4de71-117">-ApprovalRequired</span></span>
<span data-ttu-id="4de71-118">Indica se l'abbonamento al prodotto richiede l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="4de71-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="4de71-119">Per impostazione predefinita, questo parametro è **$false**.</span><span class="sxs-lookup"><span data-stu-id="4de71-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4de71-120">-Context</span></span>
<span data-ttu-id="4de71-121">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4de71-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de71-122">-DefaultProfile</span></span>
<span data-ttu-id="4de71-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4de71-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4de71-124">-Description</span></span>
<span data-ttu-id="4de71-125">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="4de71-125">Specifies the product description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="4de71-126">-LegalTerms</span></span>
<span data-ttu-id="4de71-127">Specifica le condizioni legali per l'uso del prodotto.</span><span class="sxs-lookup"><span data-stu-id="4de71-127">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4de71-128">-ProductId</span></span>
<span data-ttu-id="4de71-129">Specifica l'identificatore del nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="4de71-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="4de71-130">Se non specifichi questo parametro, viene generato un nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="4de71-130">If you do not specify this parameter, a new product is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="4de71-131">-State</span></span>
<span data-ttu-id="4de71-132">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="4de71-132">Specifies the product state.</span></span>
<span data-ttu-id="4de71-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="4de71-133">psdx_paramvalues</span></span>

- <span data-ttu-id="4de71-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="4de71-134">NotPublished</span></span>
- <span data-ttu-id="4de71-135">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="4de71-135">Published</span></span> 

<span data-ttu-id="4de71-136">Il valore predefinito è NotPublished.</span><span class="sxs-lookup"><span data-stu-id="4de71-136">The default value is NotPublished.</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-137">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="4de71-137">-SubscriptionRequired</span></span>
<span data-ttu-id="4de71-138">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4de71-138">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="4de71-139">Il valore predefinito è **$true**.</span><span class="sxs-lookup"><span data-stu-id="4de71-139">The default value is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-140">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="4de71-140">-SubscriptionsLimit</span></span>
<span data-ttu-id="4de71-141">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="4de71-141">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="4de71-142">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="4de71-142">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-143">-Titolo</span><span class="sxs-lookup"><span data-stu-id="4de71-143">-Title</span></span>
<span data-ttu-id="4de71-144">Specifica il titolo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="4de71-144">Specifies the product title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de71-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de71-145">CommonParameters</span></span>
<span data-ttu-id="4de71-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de71-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de71-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de71-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de71-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4de71-148">INPUTS</span></span>

### <span data-ttu-id="4de71-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4de71-149">None</span></span>
<span data-ttu-id="4de71-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4de71-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4de71-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4de71-151">OUTPUTS</span></span>

### <span data-ttu-id="4de71-152">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4de71-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="4de71-153">Note</span><span class="sxs-lookup"><span data-stu-id="4de71-153">NOTES</span></span>

## <span data-ttu-id="4de71-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4de71-154">RELATED LINKS</span></span>

[<span data-ttu-id="4de71-155">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4de71-155">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="4de71-156">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4de71-156">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="4de71-157">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4de71-157">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


