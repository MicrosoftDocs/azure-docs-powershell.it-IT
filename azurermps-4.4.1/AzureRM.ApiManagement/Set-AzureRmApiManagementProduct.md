---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: dac6e48faba1590897161ab59fed05f1f0b331df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517171"
---
# <span data-ttu-id="922ea-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="922ea-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="922ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="922ea-102">SYNOPSIS</span></span>
<span data-ttu-id="922ea-103">Imposta i dettagli del prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="922ea-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="922ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="922ea-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="922ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="922ea-105">DESCRIPTION</span></span>
<span data-ttu-id="922ea-106">Il cmdlet **set-AzureRmApiManagementProduct** imposta i dettagli del prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="922ea-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="922ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="922ea-107">EXAMPLES</span></span>

### <span data-ttu-id="922ea-108">Esempio 1: aggiornare i dettagli del prodotto</span><span class="sxs-lookup"><span data-stu-id="922ea-108">Example 1: Update the product details</span></span>
```
PS C:\>Set-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="922ea-109">Questo comando Aggiorna i dettagli del prodotto per la gestione delle API, richiede un abbonamento e quindi Annulla la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="922ea-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="922ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="922ea-110">PARAMETERS</span></span>

### <span data-ttu-id="922ea-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="922ea-111">-ApprovalRequired</span></span>
<span data-ttu-id="922ea-112">Indica se l'abbonamento al prodotto richiede l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="922ea-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="922ea-113">Il valore predefinito è **$false**.</span><span class="sxs-lookup"><span data-stu-id="922ea-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="922ea-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="922ea-114">-Context</span></span>
<span data-ttu-id="922ea-115">Specifica un'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="922ea-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="922ea-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="922ea-116">-Description</span></span>
<span data-ttu-id="922ea-117">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="922ea-117">Specifies the product description.</span></span>

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

### <span data-ttu-id="922ea-118">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="922ea-118">-LegalTerms</span></span>
<span data-ttu-id="922ea-119">Specifica le condizioni legali per l'uso del prodotto.</span><span class="sxs-lookup"><span data-stu-id="922ea-119">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="922ea-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="922ea-120">-PassThru</span></span>
<span data-ttu-id="922ea-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="922ea-121">passthru</span></span>

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

### <span data-ttu-id="922ea-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="922ea-122">-ProductId</span></span>
<span data-ttu-id="922ea-123">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="922ea-123">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="922ea-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="922ea-124">-State</span></span>
<span data-ttu-id="922ea-125">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="922ea-125">Specifies the product state.</span></span>
<span data-ttu-id="922ea-126">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="922ea-126">psdx_paramvalues</span></span>

- <span data-ttu-id="922ea-127">NotPublished</span><span class="sxs-lookup"><span data-stu-id="922ea-127">NotPublished</span></span>
- <span data-ttu-id="922ea-128">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="922ea-128">Published</span></span>

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

### <span data-ttu-id="922ea-129">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="922ea-129">-SubscriptionRequired</span></span>
<span data-ttu-id="922ea-130">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="922ea-130">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="922ea-131">Il valore predefinito per questo parametro è **$true**.</span><span class="sxs-lookup"><span data-stu-id="922ea-131">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="922ea-132">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="922ea-132">-SubscriptionsLimit</span></span>
<span data-ttu-id="922ea-133">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="922ea-133">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="922ea-134">Il valore predefinito per questo parametro è 1.</span><span class="sxs-lookup"><span data-stu-id="922ea-134">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="922ea-135">-Titolo</span><span class="sxs-lookup"><span data-stu-id="922ea-135">-Title</span></span>
<span data-ttu-id="922ea-136">Specifica il titolo del prodotto impostato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="922ea-136">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="922ea-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922ea-137">-DefaultProfile</span></span>
<span data-ttu-id="922ea-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="922ea-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="922ea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922ea-139">CommonParameters</span></span>
<span data-ttu-id="922ea-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922ea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922ea-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922ea-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922ea-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="922ea-142">INPUTS</span></span>

## <span data-ttu-id="922ea-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="922ea-143">OUTPUTS</span></span>

### <span data-ttu-id="922ea-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="922ea-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="922ea-145">Note</span><span class="sxs-lookup"><span data-stu-id="922ea-145">NOTES</span></span>

## <span data-ttu-id="922ea-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="922ea-146">RELATED LINKS</span></span>

[<span data-ttu-id="922ea-147">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="922ea-147">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="922ea-148">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="922ea-148">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="922ea-149">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="922ea-149">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


