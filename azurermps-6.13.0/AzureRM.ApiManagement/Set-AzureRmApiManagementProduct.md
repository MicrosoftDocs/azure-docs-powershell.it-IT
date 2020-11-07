---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: f28bfc223ed187724aa8702c378bfce5d88755fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685588"
---
# <span data-ttu-id="2a2f3-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a2f3-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="2a2f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2f3-103">Imposta i dettagli del prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a2f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a2f3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a2f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a2f3-105">DESCRIPTION</span></span>
<span data-ttu-id="2a2f3-106">Il cmdlet **set-AzureRmApiManagementProduct** imposta i dettagli del prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="2a2f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a2f3-107">EXAMPLES</span></span>

### <span data-ttu-id="2a2f3-108">Esempio 1: aggiornare i dettagli del prodotto</span><span class="sxs-lookup"><span data-stu-id="2a2f3-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="2a2f3-109">Questo comando Aggiorna i dettagli del prodotto per la gestione delle API, richiede un abbonamento e quindi Annulla la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="2a2f3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a2f3-110">PARAMETERS</span></span>

### <span data-ttu-id="2a2f3-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="2a2f3-111">-ApprovalRequired</span></span>
<span data-ttu-id="2a2f3-112">Indica se l'abbonamento al prodotto richiede l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="2a2f3-113">Il valore predefinito è **$false**.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="2a2f3-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2a2f3-114">-Context</span></span>
<span data-ttu-id="2a2f3-115">Specifica un'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2a2f3-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2a2f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2f3-116">-DefaultProfile</span></span>
<span data-ttu-id="2a2f3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a2f3-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a2f3-118">-Description</span></span>
<span data-ttu-id="2a2f3-119">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="2a2f3-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="2a2f3-120">-LegalTerms</span></span>
<span data-ttu-id="2a2f3-121">Specifica le condizioni legali per l'uso del prodotto.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="2a2f3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a2f3-122">-PassThru</span></span>
<span data-ttu-id="2a2f3-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="2a2f3-123">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a2f3-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2a2f3-124">-ProductId</span></span>
<span data-ttu-id="2a2f3-125">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="2a2f3-126">-Stato</span><span class="sxs-lookup"><span data-stu-id="2a2f3-126">-State</span></span>
<span data-ttu-id="2a2f3-127">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-127">Specifies the product state.</span></span>
<span data-ttu-id="2a2f3-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="2a2f3-128">psdx_paramvalues</span></span>
- <span data-ttu-id="2a2f3-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="2a2f3-129">NotPublished</span></span>
- <span data-ttu-id="2a2f3-130">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="2a2f3-130">Published</span></span>

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

### <span data-ttu-id="2a2f3-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="2a2f3-131">-SubscriptionRequired</span></span>
<span data-ttu-id="2a2f3-132">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="2a2f3-133">Il valore predefinito per questo parametro è **$true**.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="2a2f3-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="2a2f3-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="2a2f3-135">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="2a2f3-136">Il valore predefinito per questo parametro è 1.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="2a2f3-137">-Titolo</span><span class="sxs-lookup"><span data-stu-id="2a2f3-137">-Title</span></span>
<span data-ttu-id="2a2f3-138">Specifica il titolo del prodotto impostato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="2a2f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2f3-139">CommonParameters</span></span>
<span data-ttu-id="2a2f3-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a2f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2f3-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a2f3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2f3-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a2f3-142">INPUTS</span></span>

### <span data-ttu-id="2a2f3-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a2f3-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a2f3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2f3-144">System.String</span></span>

### <span data-ttu-id="2a2f3-145">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2a2f3-145">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2a2f3-146">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2a2f3-146">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2a2f3-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2a2f3-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2a2f3-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a2f3-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a2f3-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a2f3-149">OUTPUTS</span></span>

### <span data-ttu-id="2a2f3-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a2f3-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="2a2f3-151">Note</span><span class="sxs-lookup"><span data-stu-id="2a2f3-151">NOTES</span></span>

## <span data-ttu-id="2a2f3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a2f3-152">RELATED LINKS</span></span>

[<span data-ttu-id="2a2f3-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a2f3-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="2a2f3-154">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a2f3-154">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="2a2f3-155">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a2f3-155">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


