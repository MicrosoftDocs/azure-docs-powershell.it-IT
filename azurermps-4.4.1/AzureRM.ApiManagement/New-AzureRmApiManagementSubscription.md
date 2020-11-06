---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520811"
---
# <span data-ttu-id="7a0f9-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a0f9-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="7a0f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0f9-103">Crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a0f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a0f9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a0f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="7a0f9-106">Il cmdlet **New-AzureRmApiManagementSubscription** crea un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="7a0f9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a0f9-107">EXAMPLES</span></span>

### <span data-ttu-id="7a0f9-108">Esempio 1: sottoscrivere un utente a un prodotto</span><span class="sxs-lookup"><span data-stu-id="7a0f9-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="7a0f9-109">Questo comando sottoscrive un utente esistente a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="7a0f9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a0f9-110">PARAMETERS</span></span>

### <span data-ttu-id="7a0f9-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7a0f9-111">-Context</span></span>
<span data-ttu-id="7a0f9-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7a0f9-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7a0f9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a0f9-113">-Name</span></span>
<span data-ttu-id="7a0f9-114">Specifica il nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-114">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="7a0f9-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7a0f9-115">-PrimaryKey</span></span>
<span data-ttu-id="7a0f9-116">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="7a0f9-117">Se questo parametro non viene specificato, la chiave viene generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="7a0f9-118">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7a0f9-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7a0f9-119">-ProductId</span></span>
<span data-ttu-id="7a0f9-120">Specifica l'ID del prodotto a cui eseguire la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-120">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="7a0f9-121">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7a0f9-121">-SecondaryKey</span></span>
<span data-ttu-id="7a0f9-122">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="7a0f9-123">Questo parametro viene generato automaticamente se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="7a0f9-124">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7a0f9-125">-Stato</span><span class="sxs-lookup"><span data-stu-id="7a0f9-125">-State</span></span>
<span data-ttu-id="7a0f9-126">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-126">Specifies the subscription state.</span></span>
<span data-ttu-id="7a0f9-127">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-127">The default value is $Null.</span></span>

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

### <span data-ttu-id="7a0f9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a0f9-128">-SubscriptionId</span></span>
<span data-ttu-id="7a0f9-129">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="7a0f9-130">Questo parametro viene generato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="7a0f9-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="7a0f9-131">-UserId</span></span>
<span data-ttu-id="7a0f9-132">Specifica l'ID del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-132">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="7a0f9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0f9-133">-DefaultProfile</span></span>
<span data-ttu-id="7a0f9-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a0f9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0f9-135">CommonParameters</span></span>
<span data-ttu-id="7a0f9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0f9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0f9-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0f9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0f9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a0f9-138">INPUTS</span></span>

## <span data-ttu-id="7a0f9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a0f9-139">OUTPUTS</span></span>

### <span data-ttu-id="7a0f9-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a0f9-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="7a0f9-141">Note</span><span class="sxs-lookup"><span data-stu-id="7a0f9-141">NOTES</span></span>

## <span data-ttu-id="7a0f9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a0f9-142">RELATED LINKS</span></span>

[<span data-ttu-id="7a0f9-143">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a0f9-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="7a0f9-144">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a0f9-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="7a0f9-145">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a0f9-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


