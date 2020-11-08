---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 3d14ef7dca35796baa3e3aecf0c3df98674bfb9b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200559"
---
# <span data-ttu-id="d6416-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d6416-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="d6416-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6416-102">SYNOPSIS</span></span>
<span data-ttu-id="d6416-103">Crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d6416-103">Creates an API Management product.</span></span>

## <span data-ttu-id="d6416-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6416-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6416-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6416-105">DESCRIPTION</span></span>
<span data-ttu-id="d6416-106">Il cmdlet **New-AzApiManagementProduct** crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d6416-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="d6416-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6416-107">EXAMPLES</span></span>

### <span data-ttu-id="d6416-108">Esempio 1: creare un prodotto che non richiede un abbonamento</span><span class="sxs-lookup"><span data-stu-id="d6416-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="d6416-109">Questo comando crea un prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d6416-109">This command creates an API Management product.</span></span>
<span data-ttu-id="d6416-110">Non è necessario alcun abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d6416-110">No subscription is required.</span></span>

### <span data-ttu-id="d6416-111">Esempio 2: creare un prodotto che richiede un abbonamento e l'approvazione</span><span class="sxs-lookup"><span data-stu-id="d6416-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="d6416-112">Questo comando crea un prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6416-112">This command creates a product.</span></span>
<span data-ttu-id="d6416-113">È necessario un abbonamento e l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="d6416-113">A subscription and approval are required.</span></span>
<span data-ttu-id="d6416-114">Questo comando imposta il periodo di notifica su 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="d6416-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="d6416-115">La durata dell'abbonamento è impostata su un anno.</span><span class="sxs-lookup"><span data-stu-id="d6416-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="d6416-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6416-116">PARAMETERS</span></span>

### <span data-ttu-id="d6416-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="d6416-117">-ApprovalRequired</span></span>
<span data-ttu-id="d6416-118">Indica se l'abbonamento al prodotto richiede l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="d6416-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="d6416-119">Per impostazione predefinita, questo parametro è **$false**.</span><span class="sxs-lookup"><span data-stu-id="d6416-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="d6416-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d6416-120">-Context</span></span>
<span data-ttu-id="d6416-121">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d6416-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d6416-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6416-122">-DefaultProfile</span></span>
<span data-ttu-id="d6416-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6416-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6416-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6416-124">-Description</span></span>
<span data-ttu-id="d6416-125">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6416-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="d6416-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="d6416-126">-LegalTerms</span></span>
<span data-ttu-id="d6416-127">Specifica le condizioni legali per l'uso del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6416-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="d6416-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d6416-128">-ProductId</span></span>
<span data-ttu-id="d6416-129">Specifica l'identificatore del nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6416-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="d6416-130">Se non specifichi questo parametro, viene generato un nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6416-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="d6416-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="d6416-131">-State</span></span>
<span data-ttu-id="d6416-132">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6416-132">Specifies the product state.</span></span>
<span data-ttu-id="d6416-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="d6416-133">psdx_paramvalues</span></span>
- <span data-ttu-id="d6416-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="d6416-134">NotPublished</span></span>
- <span data-ttu-id="d6416-135">Pubblicato il valore predefinito è NotPublished.</span><span class="sxs-lookup"><span data-stu-id="d6416-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="d6416-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="d6416-136">-SubscriptionRequired</span></span>
<span data-ttu-id="d6416-137">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d6416-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="d6416-138">Il valore predefinito è **$true**.</span><span class="sxs-lookup"><span data-stu-id="d6416-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="d6416-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="d6416-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="d6416-140">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="d6416-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="d6416-141">Il valore predefinito è None.</span><span class="sxs-lookup"><span data-stu-id="d6416-141">The default value is None.</span></span>

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

### <span data-ttu-id="d6416-142">-Titolo</span><span class="sxs-lookup"><span data-stu-id="d6416-142">-Title</span></span>
<span data-ttu-id="d6416-143">Specifica il titolo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6416-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="d6416-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6416-144">CommonParameters</span></span>
<span data-ttu-id="d6416-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6416-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6416-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6416-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6416-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6416-147">INPUTS</span></span>

### <span data-ttu-id="d6416-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6416-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6416-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d6416-149">System.String</span></span>

### <span data-ttu-id="d6416-150">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6416-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d6416-151">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6416-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d6416-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d6416-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d6416-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6416-153">OUTPUTS</span></span>

### <span data-ttu-id="d6416-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d6416-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="d6416-155">Note</span><span class="sxs-lookup"><span data-stu-id="d6416-155">NOTES</span></span>

## <span data-ttu-id="d6416-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6416-156">RELATED LINKS</span></span>

[<span data-ttu-id="d6416-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d6416-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="d6416-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d6416-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="d6416-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d6416-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


