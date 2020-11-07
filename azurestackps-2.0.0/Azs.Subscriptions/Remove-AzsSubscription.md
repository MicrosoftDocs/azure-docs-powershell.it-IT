---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860114"
---
# <span data-ttu-id="f91c9-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="f91c9-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="f91c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f91c9-102">SYNOPSIS</span></span>


## <span data-ttu-id="f91c9-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f91c9-103">SYNTAX</span></span>

### <span data-ttu-id="f91c9-104">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f91c9-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f91c9-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f91c9-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f91c9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f91c9-106">DESCRIPTION</span></span>


## <span data-ttu-id="f91c9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f91c9-107">EXAMPLES</span></span>

### <span data-ttu-id="f91c9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f91c9-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="f91c9-109">Eliminare l'abbonamento a specificato.</span><span class="sxs-lookup"><span data-stu-id="f91c9-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="f91c9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f91c9-110">PARAMETERS</span></span>

### <span data-ttu-id="f91c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91c9-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="f91c9-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f91c9-112">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f91c9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f91c9-113">-InputObject</span></span>
<span data-ttu-id="f91c9-114">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f91c9-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f91c9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f91c9-115">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f91c9-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f91c9-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f91c9-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f91c9-117">-Confirm</span></span>
<span data-ttu-id="f91c9-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f91c9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f91c9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f91c9-119">-WhatIf</span></span>
<span data-ttu-id="f91c9-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f91c9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f91c9-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f91c9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f91c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91c9-122">CommonParameters</span></span>
<span data-ttu-id="f91c9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f91c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91c9-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f91c9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91c9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f91c9-125">INPUTS</span></span>

### <span data-ttu-id="f91c9-126">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="f91c9-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="f91c9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f91c9-127">OUTPUTS</span></span>

### <span data-ttu-id="f91c9-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f91c9-128">System.Boolean</span></span>



## <span data-ttu-id="f91c9-129">Note</span><span class="sxs-lookup"><span data-stu-id="f91c9-129">NOTES</span></span>

<span data-ttu-id="f91c9-130">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f91c9-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f91c9-131">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f91c9-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f91c9-132">INPUTOBJECT <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="f91c9-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="f91c9-133">`[DelegatedProviderId <String>]`: ID del provider delegato.</span><span class="sxs-lookup"><span data-stu-id="f91c9-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="f91c9-134">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f91c9-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f91c9-135">`[OfferName <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="f91c9-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="f91c9-136">`[SubscriptionId <String>]`: ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f91c9-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="f91c9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f91c9-137">RELATED LINKS</span></span>

