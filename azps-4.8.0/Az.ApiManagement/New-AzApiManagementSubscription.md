---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033344"
---
# <span data-ttu-id="815ea-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="815ea-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="815ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="815ea-102">SYNOPSIS</span></span>
<span data-ttu-id="815ea-103">Crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="815ea-103">Creates a subscription.</span></span>

## <span data-ttu-id="815ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="815ea-104">SYNTAX</span></span>

### <span data-ttu-id="815ea-105">OldSubscriptionModel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="815ea-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="815ea-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="815ea-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="815ea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="815ea-107">DESCRIPTION</span></span>
<span data-ttu-id="815ea-108">Il cmdlet **New-AzApiManagementSubscription** crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="815ea-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="815ea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="815ea-109">EXAMPLES</span></span>

### <span data-ttu-id="815ea-110">Esempio 1: sottoscrivere un utente a un prodotto</span><span class="sxs-lookup"><span data-stu-id="815ea-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="815ea-111">Questo comando sottoscrive un utente esistente a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="815ea-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="815ea-112">Esempio 2: creare un abbonamento per tutti gli ambiti API</span><span class="sxs-lookup"><span data-stu-id="815ea-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="815ea-113">Esempio 3: creare un abbonamento per l'ambito del prodotto</span><span class="sxs-lookup"><span data-stu-id="815ea-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="815ea-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="815ea-114">PARAMETERS</span></span>

### <span data-ttu-id="815ea-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="815ea-115">-AllowTracing</span></span>
<span data-ttu-id="815ea-116">Contrassegno che determina se l'analisi può essere abilitata a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="815ea-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="815ea-117">Questo parametro è facoltativo e il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="815ea-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="815ea-118">-Contesto</span><span class="sxs-lookup"><span data-stu-id="815ea-118">-Context</span></span>
<span data-ttu-id="815ea-119">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="815ea-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="815ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815ea-120">-DefaultProfile</span></span>
<span data-ttu-id="815ea-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="815ea-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="815ea-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="815ea-122">-Name</span></span>
<span data-ttu-id="815ea-123">Specifica il nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="815ea-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="815ea-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="815ea-124">-PrimaryKey</span></span>
<span data-ttu-id="815ea-125">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="815ea-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="815ea-126">Se questo parametro non viene specificato, la chiave viene generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="815ea-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="815ea-127">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="815ea-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="815ea-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="815ea-128">-ProductId</span></span>
<span data-ttu-id="815ea-129">Specifica l'ID del prodotto a cui eseguire la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="815ea-129">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="815ea-130">-Ambito</span><span class="sxs-lookup"><span data-stu-id="815ea-130">-Scope</span></span>
<span data-ttu-id="815ea-131">L'ambito della sottoscrizione, sia che si tratti di ambito API/apis/{apiId} o ambito prodotto/products/{productId} o ambito API globale/Apis o ambito globale/.</span><span class="sxs-lookup"><span data-stu-id="815ea-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="815ea-132">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="815ea-132">This parameter is required.</span></span>

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

### <span data-ttu-id="815ea-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="815ea-133">-SecondaryKey</span></span>
<span data-ttu-id="815ea-134">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="815ea-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="815ea-135">Questo parametro viene generato automaticamente se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="815ea-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="815ea-136">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="815ea-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="815ea-137">-Stato</span><span class="sxs-lookup"><span data-stu-id="815ea-137">-State</span></span>
<span data-ttu-id="815ea-138">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="815ea-138">Specifies the subscription state.</span></span>
<span data-ttu-id="815ea-139">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="815ea-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="815ea-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="815ea-140">-SubscriptionId</span></span>
<span data-ttu-id="815ea-141">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="815ea-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="815ea-142">Questo parametro viene generato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="815ea-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="815ea-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="815ea-143">-UserId</span></span>
<span data-ttu-id="815ea-144">Specifica l'ID del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="815ea-144">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="815ea-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815ea-145">CommonParameters</span></span>
<span data-ttu-id="815ea-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="815ea-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815ea-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="815ea-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815ea-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="815ea-148">INPUTS</span></span>

### <span data-ttu-id="815ea-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="815ea-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="815ea-150">System. String</span><span class="sxs-lookup"><span data-stu-id="815ea-150">System.String</span></span>

### <span data-ttu-id="815ea-151">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="815ea-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="815ea-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="815ea-152">OUTPUTS</span></span>

### <span data-ttu-id="815ea-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="815ea-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="815ea-154">Note</span><span class="sxs-lookup"><span data-stu-id="815ea-154">NOTES</span></span>

## <span data-ttu-id="815ea-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="815ea-155">RELATED LINKS</span></span>

[<span data-ttu-id="815ea-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="815ea-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="815ea-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="815ea-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="815ea-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="815ea-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


