---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018359"
---
# <span data-ttu-id="e81ca-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="e81ca-101">Update-AzReservation</span></span>

## <span data-ttu-id="e81ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e81ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e81ca-103">Aggiornare una `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e81ca-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="e81ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e81ca-104">SYNTAX</span></span>

### <span data-ttu-id="e81ca-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e81ca-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81ca-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e81ca-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e81ca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e81ca-107">DESCRIPTION</span></span>
<span data-ttu-id="e81ca-108">Aggiorna gli ambiti applicati di `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e81ca-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="e81ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e81ca-109">EXAMPLES</span></span>

### <span data-ttu-id="e81ca-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e81ca-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="e81ca-111">Aggiorna il AppliedScopeType della specifica `Reservation` a single e InstanceFlexibility su attivato.</span><span class="sxs-lookup"><span data-stu-id="e81ca-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="e81ca-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e81ca-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="e81ca-113">Aggiorna il AppliedScopeType dell'oggetto specificato `Reservation` in Shared e InstanceFlexibility su off.</span><span class="sxs-lookup"><span data-stu-id="e81ca-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="e81ca-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e81ca-114">PARAMETERS</span></span>

### <span data-ttu-id="e81ca-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="e81ca-115">-AppliedScope</span></span>
<span data-ttu-id="e81ca-116">SubscriptionId per applicare questa operazione `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e81ca-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="e81ca-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="e81ca-117">-AppliedScopeType</span></span>
<span data-ttu-id="e81ca-118">Tipo di ambito applicato</span><span class="sxs-lookup"><span data-stu-id="e81ca-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="e81ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81ca-119">-DefaultProfile</span></span>
<span data-ttu-id="e81ca-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e81ca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e81ca-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="e81ca-121">-InstanceFlexibility</span></span>
<span data-ttu-id="e81ca-122">Se presente, aggiorna il valore di InstanceFlexibility `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e81ca-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="e81ca-123">Se non specificato, il valore esistente rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="e81ca-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="e81ca-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e81ca-124">-Name</span></span>
<span data-ttu-id="e81ca-125">Nome della prenotazione</span><span class="sxs-lookup"><span data-stu-id="e81ca-125">Name of Reservation</span></span>

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

### <span data-ttu-id="e81ca-126">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="e81ca-126">-Reservation</span></span>
<span data-ttu-id="e81ca-127">Parametro oggetto pipe per `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e81ca-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="e81ca-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="e81ca-128">-ReservationId</span></span>
<span data-ttu-id="e81ca-129">ID dell' `Reservation` aggiornamento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="e81ca-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="e81ca-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e81ca-130">-ReservationOrderId</span></span>
<span data-ttu-id="e81ca-131">ID dell' `ReservationOrder` aggiornamento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="e81ca-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="e81ca-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e81ca-132">-Confirm</span></span>
<span data-ttu-id="e81ca-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81ca-134">-WhatIf</span></span>
<span data-ttu-id="e81ca-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e81ca-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e81ca-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e81ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81ca-137">CommonParameters</span></span>
<span data-ttu-id="e81ca-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81ca-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e81ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81ca-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e81ca-140">INPUTS</span></span>

### <span data-ttu-id="e81ca-141">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="e81ca-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e81ca-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e81ca-142">OUTPUTS</span></span>

### <span data-ttu-id="e81ca-143">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="e81ca-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e81ca-144">Note</span><span class="sxs-lookup"><span data-stu-id="e81ca-144">NOTES</span></span>

## <span data-ttu-id="e81ca-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e81ca-145">RELATED LINKS</span></span>
