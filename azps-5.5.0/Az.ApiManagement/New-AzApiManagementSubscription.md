---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205651"
---
# <span data-ttu-id="3742e-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3742e-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="3742e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3742e-102">SYNOPSIS</span></span>
<span data-ttu-id="3742e-103">Crea una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3742e-103">Creates a subscription.</span></span>

## <span data-ttu-id="3742e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3742e-104">SYNTAX</span></span>

### <span data-ttu-id="3742e-105">OldSubscriptionModel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3742e-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3742e-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="3742e-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3742e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3742e-107">DESCRIPTION</span></span>
<span data-ttu-id="3742e-108">Il cmdlet **New-AzApiManagementSubscription** crea una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3742e-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="3742e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3742e-109">EXAMPLES</span></span>

### <span data-ttu-id="3742e-110">Esempio 1: Sottoscrivere un utente per un prodotto</span><span class="sxs-lookup"><span data-stu-id="3742e-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="3742e-111">Questo comando sottoscrive un utente esistente per un prodotto.</span><span class="sxs-lookup"><span data-stu-id="3742e-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="3742e-112">Esempio 2: Creare una sottoscrizione per tutto l'ambito API</span><span class="sxs-lookup"><span data-stu-id="3742e-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="3742e-113">Esempio 3: Creare una sottoscrizione per l'ambito del prodotto</span><span class="sxs-lookup"><span data-stu-id="3742e-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="3742e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3742e-114">PARAMETERS</span></span>

### <span data-ttu-id="3742e-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="3742e-115">-AllowTracing</span></span>
<span data-ttu-id="3742e-116">Flag che determina se la traccia può essere abilitata a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3742e-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="3742e-117">Questo parametro è facoltativo e l'impostazione predefinita $null.</span><span class="sxs-lookup"><span data-stu-id="3742e-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="3742e-118">-Context</span><span class="sxs-lookup"><span data-stu-id="3742e-118">-Context</span></span>
<span data-ttu-id="3742e-119">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3742e-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3742e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3742e-120">-DefaultProfile</span></span>
<span data-ttu-id="3742e-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3742e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3742e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3742e-122">-Name</span></span>
<span data-ttu-id="3742e-123">Specifica il nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3742e-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="3742e-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="3742e-124">-PrimaryKey</span></span>
<span data-ttu-id="3742e-125">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3742e-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="3742e-126">Se questo parametro non è specificato, la chiave viene generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3742e-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="3742e-127">Questo parametro deve contenere da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="3742e-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="3742e-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3742e-128">-ProductId</span></span>
<span data-ttu-id="3742e-129">Specifica l'ID del prodotto a cui effettuare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3742e-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3742e-130">-Scope</span><span class="sxs-lookup"><span data-stu-id="3742e-130">-Scope</span></span>
<span data-ttu-id="3742e-131">Ambito della sottoscrizione, che si tratta di Ambito API /api/{apiId} o Ambito prodotto /products/{productId} o Ambito API globale /api o Ambito globale /.</span><span class="sxs-lookup"><span data-stu-id="3742e-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="3742e-132">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3742e-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3742e-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="3742e-133">-SecondaryKey</span></span>
<span data-ttu-id="3742e-134">Specifica la chiave secondaria di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3742e-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="3742e-135">Questo parametro viene generato automaticamente se non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="3742e-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="3742e-136">Questo parametro deve contenere da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="3742e-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="3742e-137">-State</span><span class="sxs-lookup"><span data-stu-id="3742e-137">-State</span></span>
<span data-ttu-id="3742e-138">Specifica lo stato della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3742e-138">Specifies the subscription state.</span></span>
<span data-ttu-id="3742e-139">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="3742e-139">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3742e-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3742e-140">-SubscriptionId</span></span>
<span data-ttu-id="3742e-141">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3742e-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="3742e-142">Se non viene specificato, questo parametro viene generato.</span><span class="sxs-lookup"><span data-stu-id="3742e-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="3742e-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="3742e-143">-UserId</span></span>
<span data-ttu-id="3742e-144">Specifica l'ID abbonato.</span><span class="sxs-lookup"><span data-stu-id="3742e-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3742e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3742e-145">CommonParameters</span></span>
<span data-ttu-id="3742e-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3742e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3742e-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3742e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3742e-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="3742e-148">INPUTS</span></span>

### <span data-ttu-id="3742e-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3742e-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3742e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="3742e-150">System.String</span></span>

### <span data-ttu-id="3742e-151">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3742e-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3742e-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3742e-152">OUTPUTS</span></span>

### <span data-ttu-id="3742e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3742e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="3742e-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="3742e-154">NOTES</span></span>

## <span data-ttu-id="3742e-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3742e-155">RELATED LINKS</span></span>

[<span data-ttu-id="3742e-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3742e-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="3742e-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3742e-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="3742e-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3742e-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


