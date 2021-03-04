---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: e827fcf43c151f0812d96456de430f57686d4562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959837"
---
# <span data-ttu-id="80668-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80668-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="80668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80668-102">SYNOPSIS</span></span>
<span data-ttu-id="80668-103">Imposta i dettagli del prodotto per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="80668-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="80668-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80668-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80668-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="80668-105">DESCRIPTION</span></span>
<span data-ttu-id="80668-106">Il cmdlet **Set-AzApiManagementProduct** imposta i dettagli del prodotto gestione API.</span><span class="sxs-lookup"><span data-stu-id="80668-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="80668-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80668-107">EXAMPLES</span></span>

### <span data-ttu-id="80668-108">Esempio 1: Aggiornare i dettagli del prodotto</span><span class="sxs-lookup"><span data-stu-id="80668-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="80668-109">Questo comando aggiorna i dettagli del prodotto per la gestione delle API, richiede una sottoscrizione e quindi annulla la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="80668-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="80668-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80668-110">PARAMETERS</span></span>

### <span data-ttu-id="80668-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="80668-111">-ApprovalRequired</span></span>
<span data-ttu-id="80668-112">Indica se l'abbonamento al prodotto richiede l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="80668-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="80668-113">Il valore predefinito è **$False.**</span><span class="sxs-lookup"><span data-stu-id="80668-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="80668-114">-Context</span><span class="sxs-lookup"><span data-stu-id="80668-114">-Context</span></span>
<span data-ttu-id="80668-115">Specifica un'istanza **dell'oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="80668-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="80668-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80668-116">-DefaultProfile</span></span>
<span data-ttu-id="80668-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80668-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80668-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="80668-118">-Description</span></span>
<span data-ttu-id="80668-119">Specifica la descrizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="80668-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="80668-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="80668-120">-LegalTerms</span></span>
<span data-ttu-id="80668-121">Specifica le condizioni legali per l'utilizzo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="80668-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="80668-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80668-122">-PassThru</span></span>
<span data-ttu-id="80668-123">passthru</span><span class="sxs-lookup"><span data-stu-id="80668-123">passthru</span></span>

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

### <span data-ttu-id="80668-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="80668-124">-ProductId</span></span>
<span data-ttu-id="80668-125">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="80668-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="80668-126">-State</span><span class="sxs-lookup"><span data-stu-id="80668-126">-State</span></span>
<span data-ttu-id="80668-127">Specifica lo stato del prodotto.</span><span class="sxs-lookup"><span data-stu-id="80668-127">Specifies the product state.</span></span>
<span data-ttu-id="80668-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="80668-128">psdx_paramvalues</span></span>
- <span data-ttu-id="80668-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="80668-129">NotPublished</span></span>
- <span data-ttu-id="80668-130">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="80668-130">Published</span></span>

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

### <span data-ttu-id="80668-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="80668-131">-SubscriptionRequired</span></span>
<span data-ttu-id="80668-132">Indica se il prodotto richiede un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="80668-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="80668-133">Il valore predefinito per questo parametro è **$True.**</span><span class="sxs-lookup"><span data-stu-id="80668-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="80668-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="80668-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="80668-135">Specifica il numero massimo di abbonamenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="80668-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="80668-136">Il valore predefinito per questo parametro è Nessuno.</span><span class="sxs-lookup"><span data-stu-id="80668-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="80668-137">-Title</span><span class="sxs-lookup"><span data-stu-id="80668-137">-Title</span></span>
<span data-ttu-id="80668-138">Specifica il titolo del prodotto impostato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80668-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="80668-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80668-139">-Confirm</span></span>
<span data-ttu-id="80668-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80668-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80668-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80668-141">-WhatIf</span></span>
<span data-ttu-id="80668-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80668-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80668-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80668-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80668-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80668-144">CommonParameters</span></span>
<span data-ttu-id="80668-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80668-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80668-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80668-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80668-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="80668-147">INPUTS</span></span>

### <span data-ttu-id="80668-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80668-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80668-149">System.String</span><span class="sxs-lookup"><span data-stu-id="80668-149">System.String</span></span>

### <span data-ttu-id="80668-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80668-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80668-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80668-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80668-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="80668-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="80668-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80668-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80668-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80668-154">OUTPUTS</span></span>

### <span data-ttu-id="80668-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80668-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="80668-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="80668-156">NOTES</span></span>

## <span data-ttu-id="80668-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80668-157">RELATED LINKS</span></span>

[<span data-ttu-id="80668-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80668-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="80668-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80668-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="80668-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80668-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


