---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 1b99a5ac02364b54cf4411a0341ceaf749b8fa70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675991"
---
# <span data-ttu-id="5ffcc-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5ffcc-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="5ffcc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ffcc-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffcc-103">Crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-103">Creates an API Management product.</span></span>

## <span data-ttu-id="5ffcc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ffcc-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ffcc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ffcc-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffcc-106">Il cmdlet **New-AzApiManagementProduct** crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="5ffcc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ffcc-107">EXAMPLES</span></span>

### <span data-ttu-id="5ffcc-108">Esempio 1: creare un prodotto che non richiede un abbonamento</span><span class="sxs-lookup"><span data-stu-id="5ffcc-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="5ffcc-109">Questo comando crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-109">This command creates an API Management product.</span></span>
<span data-ttu-id="5ffcc-110">Non è necessario alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-110">No subscription is required.</span></span>

### <span data-ttu-id="5ffcc-111">Esempio 2: creare un prodotto che richiede un abbonamento e l'approvazione</span><span class="sxs-lookup"><span data-stu-id="5ffcc-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="5ffcc-112">Questo comando crea un prodotto.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-112">This command creates a product.</span></span>
<span data-ttu-id="5ffcc-113">È necessario un abbonamento e l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-113">A subscription and approval are required.</span></span>
<span data-ttu-id="5ffcc-114">Questo comando imposta il periodo di notifica su 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="5ffcc-115">La durata dell'abbonamento è impostata su un anno.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="5ffcc-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ffcc-116">PARAMETERS</span></span>

### <span data-ttu-id="5ffcc-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="5ffcc-117">-ApprovalRequired</span></span>
<span data-ttu-id="5ffcc-118">Indica se l'abbonamento al prodotto richiede l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="5ffcc-119">Per impostazione predefinita, questo parametro è **$false**.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="5ffcc-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5ffcc-120">-Context</span></span>
<span data-ttu-id="5ffcc-121">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5ffcc-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5ffcc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffcc-122">-DefaultProfile</span></span>
<span data-ttu-id="5ffcc-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ffcc-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ffcc-124">-Description</span></span>
<span data-ttu-id="5ffcc-125">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="5ffcc-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="5ffcc-126">-LegalTerms</span></span>
<span data-ttu-id="5ffcc-127">Specifica le condizioni legali per l'uso del prodotto.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="5ffcc-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5ffcc-128">-ProductId</span></span>
<span data-ttu-id="5ffcc-129">Specifica l'identificatore del nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="5ffcc-130">Se non specifichi questo parametro, viene generato un nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="5ffcc-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="5ffcc-131">-State</span></span>
<span data-ttu-id="5ffcc-132">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-132">Specifies the product state.</span></span>
<span data-ttu-id="5ffcc-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="5ffcc-133">psdx_paramvalues</span></span>
- <span data-ttu-id="5ffcc-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="5ffcc-134">NotPublished</span></span>
- <span data-ttu-id="5ffcc-135">Pubblicato il valore predefinito è NotPublished.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="5ffcc-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="5ffcc-136">-SubscriptionRequired</span></span>
<span data-ttu-id="5ffcc-137">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="5ffcc-138">Il valore predefinito è **$true**.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="5ffcc-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="5ffcc-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="5ffcc-140">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="5ffcc-141">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-141">The default value is 1.</span></span>

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

### <span data-ttu-id="5ffcc-142">-Titolo</span><span class="sxs-lookup"><span data-stu-id="5ffcc-142">-Title</span></span>
<span data-ttu-id="5ffcc-143">Specifica il titolo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="5ffcc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffcc-144">CommonParameters</span></span>
<span data-ttu-id="5ffcc-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffcc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffcc-146">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ffcc-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffcc-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ffcc-147">INPUTS</span></span>

### <span data-ttu-id="5ffcc-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5ffcc-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5ffcc-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5ffcc-149">System.String</span></span>

### <span data-ttu-id="5ffcc-150">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ffcc-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5ffcc-151">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ffcc-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5ffcc-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ffcc-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5ffcc-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ffcc-153">OUTPUTS</span></span>

### <span data-ttu-id="5ffcc-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5ffcc-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="5ffcc-155">Note</span><span class="sxs-lookup"><span data-stu-id="5ffcc-155">NOTES</span></span>

## <span data-ttu-id="5ffcc-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ffcc-156">RELATED LINKS</span></span>

[<span data-ttu-id="5ffcc-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5ffcc-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="5ffcc-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5ffcc-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="5ffcc-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5ffcc-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


