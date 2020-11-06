---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 08685a84817f55e030a62b0b98ddc35be9f05843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515844"
---
# <span data-ttu-id="5f499-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f499-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="5f499-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f499-102">SYNOPSIS</span></span>
<span data-ttu-id="5f499-103">Crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5f499-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f499-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f499-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f499-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f499-105">DESCRIPTION</span></span>
<span data-ttu-id="5f499-106">Il cmdlet **New-AzureRmApiManagementSubscription** crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5f499-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="5f499-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f499-107">EXAMPLES</span></span>

### <span data-ttu-id="5f499-108">Esempio 1: sottoscrivere un utente a un prodotto</span><span class="sxs-lookup"><span data-stu-id="5f499-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="5f499-109">Questo comando sottoscrive un utente esistente a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="5f499-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="5f499-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f499-110">PARAMETERS</span></span>

### <span data-ttu-id="5f499-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5f499-111">-Context</span></span>
<span data-ttu-id="5f499-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5f499-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f499-113">-DefaultProfile</span></span>
<span data-ttu-id="5f499-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f499-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f499-115">-Name</span></span>
<span data-ttu-id="5f499-116">Specifica il nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5f499-116">Specifies the subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5f499-117">-PrimaryKey</span></span>
<span data-ttu-id="5f499-118">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5f499-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="5f499-119">Se questo parametro non viene specificato, la chiave viene generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5f499-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="5f499-120">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5f499-120">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5f499-121">-ProductId</span></span>
<span data-ttu-id="5f499-122">Specifica l'ID del prodotto a cui eseguire la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5f499-122">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5f499-123">-SecondaryKey</span></span>
<span data-ttu-id="5f499-124">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5f499-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="5f499-125">Questo parametro viene generato automaticamente se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="5f499-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="5f499-126">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5f499-126">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-127">-Stato</span><span class="sxs-lookup"><span data-stu-id="5f499-127">-State</span></span>
<span data-ttu-id="5f499-128">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5f499-128">Specifies the subscription state.</span></span>
<span data-ttu-id="5f499-129">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="5f499-129">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f499-130">-SubscriptionId</span></span>
<span data-ttu-id="5f499-131">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5f499-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="5f499-132">Questo parametro viene generato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="5f499-132">This parameter is generated if not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="5f499-133">-UserId</span></span>
<span data-ttu-id="5f499-134">Specifica l'ID del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="5f499-134">Specifies the subscriber ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f499-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f499-135">CommonParameters</span></span>
<span data-ttu-id="5f499-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f499-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f499-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f499-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f499-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f499-138">INPUTS</span></span>

### <span data-ttu-id="5f499-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5f499-139">None</span></span>
<span data-ttu-id="5f499-140">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5f499-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f499-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f499-141">OUTPUTS</span></span>

### <span data-ttu-id="5f499-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f499-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="5f499-143">Note</span><span class="sxs-lookup"><span data-stu-id="5f499-143">NOTES</span></span>

## <span data-ttu-id="5f499-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f499-144">RELATED LINKS</span></span>

[<span data-ttu-id="5f499-145">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f499-145">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="5f499-146">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f499-146">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="5f499-147">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f499-147">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


