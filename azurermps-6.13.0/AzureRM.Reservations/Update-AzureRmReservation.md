---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 64e2ec58c6ed31e54a4adf0ee983aa9ae485715d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513524"
---
# <span data-ttu-id="844a4-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="844a4-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="844a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="844a4-102">SYNOPSIS</span></span>
<span data-ttu-id="844a4-103">Aggiornare una `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="844a4-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="844a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="844a4-104">SYNTAX</span></span>

### <span data-ttu-id="844a4-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="844a4-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="844a4-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="844a4-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="844a4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="844a4-107">DESCRIPTION</span></span>
<span data-ttu-id="844a4-108">Aggiorna gli ambiti applicati di `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="844a4-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="844a4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="844a4-109">EXAMPLES</span></span>

### <span data-ttu-id="844a4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="844a4-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="844a4-111">Aggiorna il AppliedScopeType della specifica `Reservation` a single e InstanceFlexibility su attivato.</span><span class="sxs-lookup"><span data-stu-id="844a4-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="844a4-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="844a4-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="844a4-113">Aggiorna il AppliedScopeType dell'oggetto specificato `Reservation` in Shared e InstanceFlexibility su off.</span><span class="sxs-lookup"><span data-stu-id="844a4-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="844a4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="844a4-114">PARAMETERS</span></span>

### <span data-ttu-id="844a4-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="844a4-115">-AppliedScope</span></span>
<span data-ttu-id="844a4-116">SubscriptionId per applicare questa operazione `Reservation`</span><span class="sxs-lookup"><span data-stu-id="844a4-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844a4-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="844a4-117">-AppliedScopeType</span></span>
<span data-ttu-id="844a4-118">Tipo di ambito applicato</span><span class="sxs-lookup"><span data-stu-id="844a4-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="844a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="844a4-119">-DefaultProfile</span></span>
<span data-ttu-id="844a4-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="844a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="844a4-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="844a4-121">-InstanceFlexibility</span></span>
<span data-ttu-id="844a4-122">Se presente, aggiorna il valore di InstanceFlexibility `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="844a4-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="844a4-123">Se non specificato, il valore esistente rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="844a4-123">If not specified, the existing value remains unchanged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844a4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="844a4-124">-Name</span></span>
<span data-ttu-id="844a4-125">Nome della prenotazione</span><span class="sxs-lookup"><span data-stu-id="844a4-125">Name of Reservation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844a4-126">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="844a4-126">-Reservation</span></span>
<span data-ttu-id="844a4-127">Parametro oggetto pipe per `Reservation`</span><span class="sxs-lookup"><span data-stu-id="844a4-127">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="844a4-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="844a4-128">-ReservationId</span></span>
<span data-ttu-id="844a4-129">ID dell' `Reservation` aggiornamento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="844a4-129">Id of the `Reservation` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844a4-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="844a4-130">-ReservationOrderId</span></span>
<span data-ttu-id="844a4-131">ID dell' `ReservationOrder` aggiornamento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="844a4-131">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844a4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="844a4-132">-Confirm</span></span>
<span data-ttu-id="844a4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="844a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="844a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="844a4-134">-WhatIf</span></span>
<span data-ttu-id="844a4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="844a4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="844a4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="844a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="844a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="844a4-137">CommonParameters</span></span>
<span data-ttu-id="844a4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="844a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="844a4-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="844a4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="844a4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="844a4-140">INPUTS</span></span>

### <span data-ttu-id="844a4-141">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="844a4-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="844a4-142">Parametri: prenotazione (ByValue)</span><span class="sxs-lookup"><span data-stu-id="844a4-142">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="844a4-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="844a4-143">OUTPUTS</span></span>

### <span data-ttu-id="844a4-144">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="844a4-144">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="844a4-145">Note</span><span class="sxs-lookup"><span data-stu-id="844a4-145">NOTES</span></span>

## <span data-ttu-id="844a4-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="844a4-146">RELATED LINKS</span></span>
