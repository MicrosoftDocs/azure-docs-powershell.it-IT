---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: 4074afa1c3ba0ad3d4873d290191e63bcc0c57dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675979"
---
# <span data-ttu-id="7eb11-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7eb11-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="7eb11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7eb11-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb11-103">Crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7eb11-103">Creates a subscription.</span></span>

## <span data-ttu-id="7eb11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7eb11-104">SYNTAX</span></span>

### <span data-ttu-id="7eb11-105">OldSubscriptionModel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7eb11-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eb11-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="7eb11-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eb11-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eb11-107">DESCRIPTION</span></span>
<span data-ttu-id="7eb11-108">Il cmdlet **New-AzApiManagementSubscription** crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7eb11-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="7eb11-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7eb11-109">EXAMPLES</span></span>

### <span data-ttu-id="7eb11-110">Esempio 1: sottoscrivere un utente a un prodotto</span><span class="sxs-lookup"><span data-stu-id="7eb11-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="7eb11-111">Questo comando sottoscrive un utente esistente a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="7eb11-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="7eb11-112">Esempio 2: creare un abbonamento per tutti gli ambiti API</span><span class="sxs-lookup"><span data-stu-id="7eb11-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="7eb11-113">Esempio 3: creare un abbonamento per l'ambito del prodotto</span><span class="sxs-lookup"><span data-stu-id="7eb11-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="7eb11-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eb11-114">PARAMETERS</span></span>

### <span data-ttu-id="7eb11-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="7eb11-115">-AllowTracing</span></span>
<span data-ttu-id="7eb11-116">Contrassegno che determina se l'analisi può essere abilitata a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7eb11-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="7eb11-117">Questo parametro è facoltativo e il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="7eb11-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="7eb11-118">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7eb11-118">-Context</span></span>
<span data-ttu-id="7eb11-119">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7eb11-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7eb11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb11-120">-DefaultProfile</span></span>
<span data-ttu-id="7eb11-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb11-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eb11-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7eb11-122">-Name</span></span>
<span data-ttu-id="7eb11-123">Specifica il nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7eb11-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="7eb11-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7eb11-124">-PrimaryKey</span></span>
<span data-ttu-id="7eb11-125">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7eb11-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="7eb11-126">Se questo parametro non viene specificato, la chiave viene generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7eb11-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="7eb11-127">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7eb11-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7eb11-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7eb11-128">-ProductId</span></span>
<span data-ttu-id="7eb11-129">Specifica l'ID del prodotto a cui eseguire la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7eb11-129">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="7eb11-130">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7eb11-130">-Scope</span></span>
<span data-ttu-id="7eb11-131">L'ambito della sottoscrizione, sia che si tratti di ambito API/apis/{apiId} o ambito prodotto/products/{productId} o ambito API globale/Apis o ambito globale/.</span><span class="sxs-lookup"><span data-stu-id="7eb11-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="7eb11-132">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7eb11-132">This parameter is required.</span></span>

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

### <span data-ttu-id="7eb11-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7eb11-133">-SecondaryKey</span></span>
<span data-ttu-id="7eb11-134">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7eb11-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="7eb11-135">Questo parametro viene generato automaticamente se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="7eb11-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="7eb11-136">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7eb11-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7eb11-137">-Stato</span><span class="sxs-lookup"><span data-stu-id="7eb11-137">-State</span></span>
<span data-ttu-id="7eb11-138">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7eb11-138">Specifies the subscription state.</span></span>
<span data-ttu-id="7eb11-139">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="7eb11-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="7eb11-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7eb11-140">-SubscriptionId</span></span>
<span data-ttu-id="7eb11-141">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7eb11-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="7eb11-142">Questo parametro viene generato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="7eb11-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="7eb11-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="7eb11-143">-UserId</span></span>
<span data-ttu-id="7eb11-144">Specifica l'ID del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="7eb11-144">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="7eb11-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb11-145">CommonParameters</span></span>
<span data-ttu-id="7eb11-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb11-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb11-147">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7eb11-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb11-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7eb11-148">INPUTS</span></span>

### <span data-ttu-id="7eb11-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7eb11-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7eb11-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7eb11-150">System.String</span></span>

### <span data-ttu-id="7eb11-151">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7eb11-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7eb11-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7eb11-152">OUTPUTS</span></span>

### <span data-ttu-id="7eb11-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7eb11-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="7eb11-154">Note</span><span class="sxs-lookup"><span data-stu-id="7eb11-154">NOTES</span></span>

## <span data-ttu-id="7eb11-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7eb11-155">RELATED LINKS</span></span>

[<span data-ttu-id="7eb11-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7eb11-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="7eb11-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7eb11-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="7eb11-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7eb11-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)

