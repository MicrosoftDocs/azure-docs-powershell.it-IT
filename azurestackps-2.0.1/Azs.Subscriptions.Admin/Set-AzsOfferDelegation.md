---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023294"
---
# <span data-ttu-id="d513a-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d513a-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="d513a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d513a-102">SYNOPSIS</span></span>
<span data-ttu-id="d513a-103">Creare o aggiornare la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="d513a-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="d513a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d513a-104">SYNTAX</span></span>

### <span data-ttu-id="d513a-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d513a-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d513a-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d513a-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d513a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d513a-107">DESCRIPTION</span></span>
<span data-ttu-id="d513a-108">Creare o aggiornare la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="d513a-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="d513a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d513a-109">EXAMPLES</span></span>

### <span data-ttu-id="d513a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d513a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="d513a-111">Aggiorna la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="d513a-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="d513a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d513a-112">PARAMETERS</span></span>

### <span data-ttu-id="d513a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d513a-113">-DefaultProfile</span></span>
<span data-ttu-id="d513a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d513a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d513a-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d513a-115">-Location</span></span>
<span data-ttu-id="d513a-116">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="d513a-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d513a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d513a-117">-Name</span></span>
<span data-ttu-id="d513a-118">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="d513a-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d513a-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="d513a-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="d513a-120">Delega offerta.</span><span class="sxs-lookup"><span data-stu-id="d513a-120">Offer delegation.</span></span>
<span data-ttu-id="d513a-121">Per costruire, vedere la sezione Note per le proprietà di OFFERDELEGATIONDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d513a-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d513a-122">-Offername</span><span class="sxs-lookup"><span data-stu-id="d513a-122">-OfferName</span></span>
<span data-ttu-id="d513a-123">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="d513a-123">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d513a-124">-PropertiesSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d513a-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="d513a-125">Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="d513a-125">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d513a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d513a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d513a-127">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d513a-127">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d513a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d513a-128">-SubscriptionId</span></span>
<span data-ttu-id="d513a-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d513a-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d513a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d513a-130">-Confirm</span></span>
<span data-ttu-id="d513a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d513a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d513a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d513a-132">-WhatIf</span></span>
<span data-ttu-id="d513a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d513a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d513a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d513a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d513a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d513a-135">CommonParameters</span></span>
<span data-ttu-id="d513a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d513a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d513a-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d513a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d513a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d513a-138">INPUTS</span></span>

### <span data-ttu-id="d513a-139">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d513a-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="d513a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d513a-140">OUTPUTS</span></span>

### <span data-ttu-id="d513a-141">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d513a-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="d513a-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d513a-142">ALIASES</span></span>

## <span data-ttu-id="d513a-143">Note</span><span class="sxs-lookup"><span data-stu-id="d513a-143">NOTES</span></span>

<span data-ttu-id="d513a-144">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d513a-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d513a-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d513a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d513a-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : delega offerta.</span><span class="sxs-lookup"><span data-stu-id="d513a-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="d513a-147">`[Location <String>]`: Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="d513a-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="d513a-148">`[SubscriptionId <String>]`: Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="d513a-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="d513a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d513a-149">RELATED LINKS</span></span>

