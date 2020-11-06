---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 9e59fb8ce19d705fffdd52a172be2a333a3ca7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516116"
---
# <span data-ttu-id="a1545-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="a1545-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="a1545-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1545-102">SYNOPSIS</span></span>
<span data-ttu-id="a1545-103">Ottenere gli abbonamenti a cui l'account corrente può accedere.</span><span class="sxs-lookup"><span data-stu-id="a1545-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1545-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1545-104">SYNTAX</span></span>

### <span data-ttu-id="a1545-105">ListByIdInTenant (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1545-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1545-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="a1545-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1545-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1545-107">DESCRIPTION</span></span>
<span data-ttu-id="a1545-108">Il cmdlet Get-AzureRmSubscription Ottiene l'ID sottoscrizione, il nome dell'abbonamento e il tenant Home per gli abbonamenti a cui l'account corrente può accedere.</span><span class="sxs-lookup"><span data-stu-id="a1545-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a1545-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1545-109">EXAMPLES</span></span>

### <span data-ttu-id="a1545-110">Esempio 1: ottenere tutte le sottoscrizioni in tutti i tenant</span><span class="sxs-lookup"><span data-stu-id="a1545-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a1545-111">Questo comando consente di ottenere tutte le sottoscrizioni in tutti i tenant autorizzati per l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="a1545-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="a1545-112">Esempio 2: ottenere tutti gli abbonamenti per un tenant specifico</span><span class="sxs-lookup"><span data-stu-id="a1545-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a1545-113">Elencare tutte le sottoscrizioni nel tenant indicato autorizzato per l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="a1545-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="a1545-114">Esempio 3: ottenere tutte le sottoscrizioni nel tenant corrente</span><span class="sxs-lookup"><span data-stu-id="a1545-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a1545-115">Questo comando consente di ottenere tutte le sottoscrizioni del tenant corrente autorizzate per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a1545-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="a1545-116">Esempio 4: cambiare il contesto corrente in uso di un abbonamento specifico</span><span class="sxs-lookup"><span data-stu-id="a1545-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a1545-117">Questo comando ottiene l'abbonamento specificato e quindi imposta il contesto corrente per usarlo.</span><span class="sxs-lookup"><span data-stu-id="a1545-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="a1545-118">Tutti i cmdlet successivi in questa sessione usano il nuovo abbonamento (contoso Subscription 1) per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a1545-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="a1545-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1545-119">PARAMETERS</span></span>

### <span data-ttu-id="a1545-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1545-120">-DefaultProfile</span></span>
<span data-ttu-id="a1545-121">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a1545-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1545-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1545-122">-SubscriptionId</span></span>
<span data-ttu-id="a1545-123">Specifica l'ID della sottoscrizione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a1545-123">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1545-124">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="a1545-124">-SubscriptionName</span></span>
<span data-ttu-id="a1545-125">Specifica il nome dell'abbonamento da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a1545-125">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1545-126">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="a1545-126">-TenantId</span></span>
<span data-ttu-id="a1545-127">Specifica l'ID del tenant che contiene le sottoscrizioni da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a1545-127">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="a1545-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1545-128">CommonParameters</span></span>
<span data-ttu-id="a1545-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1545-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1545-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1545-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1545-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1545-131">INPUTS</span></span>

## <span data-ttu-id="a1545-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1545-132">OUTPUTS</span></span>

### <span data-ttu-id="a1545-133">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a1545-133">PSAzureSubscription</span></span>

## <span data-ttu-id="a1545-134">Note</span><span class="sxs-lookup"><span data-stu-id="a1545-134">NOTES</span></span>

## <span data-ttu-id="a1545-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1545-135">RELATED LINKS</span></span>

