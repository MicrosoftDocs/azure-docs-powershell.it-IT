---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: b836fec6074767e4b97188b5bb75f38d22724eb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852533"
---
# <span data-ttu-id="adcc6-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="adcc6-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="adcc6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adcc6-102">SYNOPSIS</span></span>
<span data-ttu-id="adcc6-103">Crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="adcc6-103">Creates a subscription.</span></span>

## <span data-ttu-id="adcc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adcc6-104">SYNTAX</span></span>

```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adcc6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adcc6-105">DESCRIPTION</span></span>
<span data-ttu-id="adcc6-106">Il cmdlet **New-AzApiManagementSubscription** crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="adcc6-106">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="adcc6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adcc6-107">EXAMPLES</span></span>

### <span data-ttu-id="adcc6-108">Esempio 1: sottoscrivere un utente a un prodotto</span><span class="sxs-lookup"><span data-stu-id="adcc6-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="adcc6-109">Questo comando sottoscrive un utente esistente a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="adcc6-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="adcc6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adcc6-110">PARAMETERS</span></span>

### <span data-ttu-id="adcc6-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="adcc6-111">-Context</span></span>
<span data-ttu-id="adcc6-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="adcc6-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="adcc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adcc6-113">-DefaultProfile</span></span>
<span data-ttu-id="adcc6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adcc6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adcc6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="adcc6-115">-Name</span></span>
<span data-ttu-id="adcc6-116">Specifica il nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="adcc6-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="adcc6-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="adcc6-117">-PrimaryKey</span></span>
<span data-ttu-id="adcc6-118">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="adcc6-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="adcc6-119">Se questo parametro non viene specificato, la chiave viene generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="adcc6-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="adcc6-120">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="adcc6-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="adcc6-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="adcc6-121">-ProductId</span></span>
<span data-ttu-id="adcc6-122">Specifica l'ID del prodotto a cui eseguire la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="adcc6-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="adcc6-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="adcc6-123">-SecondaryKey</span></span>
<span data-ttu-id="adcc6-124">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="adcc6-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="adcc6-125">Questo parametro viene generato automaticamente se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="adcc6-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="adcc6-126">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="adcc6-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="adcc6-127">-Stato</span><span class="sxs-lookup"><span data-stu-id="adcc6-127">-State</span></span>
<span data-ttu-id="adcc6-128">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="adcc6-128">Specifies the subscription state.</span></span>
<span data-ttu-id="adcc6-129">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="adcc6-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="adcc6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adcc6-130">-SubscriptionId</span></span>
<span data-ttu-id="adcc6-131">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="adcc6-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="adcc6-132">Questo parametro viene generato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="adcc6-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="adcc6-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="adcc6-133">-UserId</span></span>
<span data-ttu-id="adcc6-134">Specifica l'ID del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="adcc6-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="adcc6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcc6-135">CommonParameters</span></span>
<span data-ttu-id="adcc6-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adcc6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcc6-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adcc6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcc6-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adcc6-138">INPUTS</span></span>

### <span data-ttu-id="adcc6-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="adcc6-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="adcc6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="adcc6-140">System.String</span></span>

### <span data-ttu-id="adcc6-141">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="adcc6-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="adcc6-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adcc6-142">OUTPUTS</span></span>

### <span data-ttu-id="adcc6-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="adcc6-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="adcc6-144">Note</span><span class="sxs-lookup"><span data-stu-id="adcc6-144">NOTES</span></span>

## <span data-ttu-id="adcc6-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adcc6-145">RELATED LINKS</span></span>

[<span data-ttu-id="adcc6-146">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="adcc6-146">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="adcc6-147">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="adcc6-147">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="adcc6-148">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="adcc6-148">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


