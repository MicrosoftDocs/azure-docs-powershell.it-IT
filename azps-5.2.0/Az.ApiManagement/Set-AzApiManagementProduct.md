---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356287"
---
# <span data-ttu-id="7fb33-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7fb33-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="7fb33-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7fb33-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb33-103">Imposta i dettagli del prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="7fb33-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="7fb33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fb33-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb33-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fb33-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb33-106">Il cmdlet **set-AzApiManagementProduct** imposta i dettagli del prodotto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="7fb33-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="7fb33-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fb33-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb33-108">Esempio 1: aggiornare i dettagli del prodotto</span><span class="sxs-lookup"><span data-stu-id="7fb33-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="7fb33-109">Questo comando Aggiorna i dettagli del prodotto per la gestione delle API, richiede un abbonamento e quindi Annulla la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="7fb33-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="7fb33-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7fb33-110">PARAMETERS</span></span>

### <span data-ttu-id="7fb33-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="7fb33-111">-ApprovalRequired</span></span>
<span data-ttu-id="7fb33-112">Indica se l'abbonamento al prodotto richiede l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="7fb33-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="7fb33-113">Il valore predefinito è **$false**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="7fb33-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7fb33-114">-Context</span></span>
<span data-ttu-id="7fb33-115">Specifica un'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7fb33-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7fb33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb33-116">-DefaultProfile</span></span>
<span data-ttu-id="7fb33-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb33-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fb33-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fb33-118">-Description</span></span>
<span data-ttu-id="7fb33-119">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7fb33-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="7fb33-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="7fb33-120">-LegalTerms</span></span>
<span data-ttu-id="7fb33-121">Specifica le condizioni legali per l'uso del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7fb33-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="7fb33-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fb33-122">-PassThru</span></span>
<span data-ttu-id="7fb33-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="7fb33-123">passthru</span></span>

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

### <span data-ttu-id="7fb33-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7fb33-124">-ProductId</span></span>
<span data-ttu-id="7fb33-125">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="7fb33-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="7fb33-126">-Stato</span><span class="sxs-lookup"><span data-stu-id="7fb33-126">-State</span></span>
<span data-ttu-id="7fb33-127">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7fb33-127">Specifies the product state.</span></span>
<span data-ttu-id="7fb33-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="7fb33-128">psdx_paramvalues</span></span>
- <span data-ttu-id="7fb33-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="7fb33-129">NotPublished</span></span>
- <span data-ttu-id="7fb33-130">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="7fb33-130">Published</span></span>

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

### <span data-ttu-id="7fb33-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="7fb33-131">-SubscriptionRequired</span></span>
<span data-ttu-id="7fb33-132">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7fb33-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="7fb33-133">Il valore predefinito per questo parametro è **$true**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="7fb33-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="7fb33-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="7fb33-135">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="7fb33-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="7fb33-136">Il valore predefinito per questo parametro è None.</span><span class="sxs-lookup"><span data-stu-id="7fb33-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="7fb33-137">-Titolo</span><span class="sxs-lookup"><span data-stu-id="7fb33-137">-Title</span></span>
<span data-ttu-id="7fb33-138">Specifica il titolo del prodotto impostato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fb33-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="7fb33-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7fb33-139">-Confirm</span></span>
<span data-ttu-id="7fb33-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fb33-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb33-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb33-141">-WhatIf</span></span>
<span data-ttu-id="7fb33-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fb33-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fb33-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fb33-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb33-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb33-144">CommonParameters</span></span>
<span data-ttu-id="7fb33-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb33-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb33-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fb33-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb33-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7fb33-147">INPUTS</span></span>

### <span data-ttu-id="7fb33-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7fb33-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7fb33-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7fb33-149">System.String</span></span>

### <span data-ttu-id="7fb33-150">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7fb33-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7fb33-151">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7fb33-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7fb33-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7fb33-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7fb33-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7fb33-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7fb33-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fb33-154">OUTPUTS</span></span>

### <span data-ttu-id="7fb33-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7fb33-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="7fb33-156">Note</span><span class="sxs-lookup"><span data-stu-id="7fb33-156">NOTES</span></span>

## <span data-ttu-id="7fb33-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fb33-157">RELATED LINKS</span></span>

[<span data-ttu-id="7fb33-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7fb33-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="7fb33-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7fb33-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="7fb33-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7fb33-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


