---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030488"
---
# <span data-ttu-id="dfcce-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="dfcce-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="dfcce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfcce-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcce-103">Ottiene i dettagli su un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="dfcce-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="dfcce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfcce-104">SYNTAX</span></span>

### <span data-ttu-id="dfcce-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfcce-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dfcce-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="dfcce-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dfcce-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dfcce-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dfcce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfcce-108">DESCRIPTION</span></span>
<span data-ttu-id="dfcce-109">Ottiene i dettagli su un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="dfcce-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="dfcce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfcce-110">EXAMPLES</span></span>

### <span data-ttu-id="dfcce-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dfcce-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="dfcce-112">Ottenere l'elenco degli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="dfcce-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="dfcce-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfcce-113">PARAMETERS</span></span>

### <span data-ttu-id="dfcce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcce-114">-DefaultProfile</span></span>
<span data-ttu-id="dfcce-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfcce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfcce-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfcce-116">-InputObject</span></span>
<span data-ttu-id="dfcce-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dfcce-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dfcce-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfcce-118">-SubscriptionId</span></span>
<span data-ttu-id="dfcce-119">ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dfcce-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfcce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcce-120">CommonParameters</span></span>
<span data-ttu-id="dfcce-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcce-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfcce-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcce-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfcce-123">INPUTS</span></span>

### <span data-ttu-id="dfcce-124">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="dfcce-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="dfcce-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfcce-125">OUTPUTS</span></span>

### <span data-ttu-id="dfcce-126">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="dfcce-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="dfcce-127">Note</span><span class="sxs-lookup"><span data-stu-id="dfcce-127">NOTES</span></span>

<span data-ttu-id="dfcce-128">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="dfcce-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfcce-129">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfcce-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dfcce-130">INPUTOBJECT <ISubscriptionIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="dfcce-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfcce-131">`[DelegatedProviderId <String>]`: ID del provider delegato.</span><span class="sxs-lookup"><span data-stu-id="dfcce-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="dfcce-132">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="dfcce-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfcce-133">`[OfferName <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="dfcce-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="dfcce-134">`[SubscriptionId <String>]`: ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dfcce-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="dfcce-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfcce-135">RELATED LINKS</span></span>

