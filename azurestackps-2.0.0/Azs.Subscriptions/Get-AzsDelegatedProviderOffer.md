---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863914"
---
# <span data-ttu-id="c941f-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="c941f-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="c941f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c941f-102">SYNOPSIS</span></span>
<span data-ttu-id="c941f-103">Ottieni l'offerta specificata per il provider delegato.</span><span class="sxs-lookup"><span data-stu-id="c941f-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="c941f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c941f-104">SYNTAX</span></span>

### <span data-ttu-id="c941f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c941f-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c941f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c941f-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c941f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c941f-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c941f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c941f-108">DESCRIPTION</span></span>
<span data-ttu-id="c941f-109">Ottieni l'offerta specificata per il provider delegato.</span><span class="sxs-lookup"><span data-stu-id="c941f-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="c941f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c941f-110">EXAMPLES</span></span>

### <span data-ttu-id="c941f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c941f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="c941f-112">Ottenere l'elenco delle offerte per il provider delegato specificato</span><span class="sxs-lookup"><span data-stu-id="c941f-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="c941f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c941f-113">PARAMETERS</span></span>

### <span data-ttu-id="c941f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c941f-114">-DefaultProfile</span></span>
<span data-ttu-id="c941f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c941f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c941f-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="c941f-116">-DelegatedProviderId</span></span>
<span data-ttu-id="c941f-117">ID del provider delegato.</span><span class="sxs-lookup"><span data-stu-id="c941f-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c941f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c941f-118">-InputObject</span></span>
<span data-ttu-id="c941f-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c941f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c941f-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="c941f-120">-OfferName</span></span>
<span data-ttu-id="c941f-121">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="c941f-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c941f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c941f-122">CommonParameters</span></span>
<span data-ttu-id="c941f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c941f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c941f-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c941f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c941f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c941f-125">INPUTS</span></span>

### <span data-ttu-id="c941f-126">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="c941f-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="c941f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c941f-127">OUTPUTS</span></span>

### <span data-ttu-id="c941f-128">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="c941f-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="c941f-129">Note</span><span class="sxs-lookup"><span data-stu-id="c941f-129">NOTES</span></span>

<span data-ttu-id="c941f-130">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c941f-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c941f-131">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c941f-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c941f-132">INPUTOBJECT <ISubscriptionIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c941f-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c941f-133">`[DelegatedProviderId <String>]`: ID del provider delegato.</span><span class="sxs-lookup"><span data-stu-id="c941f-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="c941f-134">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c941f-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c941f-135">`[OfferName <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="c941f-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c941f-136">`[SubscriptionId <String>]`: ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c941f-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="c941f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c941f-137">RELATED LINKS</span></span>

