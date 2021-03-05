---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: b93dd1462bb019b12fe761e0bdd6cc4172c01b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000174"
---
# <span data-ttu-id="41d43-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="41d43-101">Update-AzReservation</span></span>

## <span data-ttu-id="41d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41d43-102">SYNOPSIS</span></span>
<span data-ttu-id="41d43-103">Aggiornare un `Reservation` file.</span><span class="sxs-lookup"><span data-stu-id="41d43-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="41d43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41d43-104">SYNTAX</span></span>

### <span data-ttu-id="41d43-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41d43-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d43-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="41d43-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41d43-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41d43-107">DESCRIPTION</span></span>
<span data-ttu-id="41d43-108">Aggiorna gli ambiti applicati dell'oggetto `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="41d43-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="41d43-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41d43-109">EXAMPLES</span></span>

### <span data-ttu-id="41d43-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41d43-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="41d43-111">Aggiorna AppliedScopeType dell'elemento specificato `Reservation` in Single e InstanceFlexibility in On.</span><span class="sxs-lookup"><span data-stu-id="41d43-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="41d43-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="41d43-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="41d43-113">Aggiorna AppliedScopeType dell'elemento specificato `Reservation` in Shared e InstanceFlexibility in Off.</span><span class="sxs-lookup"><span data-stu-id="41d43-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="41d43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41d43-114">PARAMETERS</span></span>

### <span data-ttu-id="41d43-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="41d43-115">-AppliedScope</span></span>
<span data-ttu-id="41d43-116">SubscriptionId per `Reservation` l'applicazione</span><span class="sxs-lookup"><span data-stu-id="41d43-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="41d43-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="41d43-117">-AppliedScopeType</span></span>
<span data-ttu-id="41d43-118">Tipo dell'ambito applicato</span><span class="sxs-lookup"><span data-stu-id="41d43-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="41d43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d43-119">-DefaultProfile</span></span>
<span data-ttu-id="41d43-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41d43-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d43-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="41d43-121">-InstanceFlexibility</span></span>
<span data-ttu-id="41d43-122">Se presente, aggiorna il valore di InstanceFlexibility dell'istanza di `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="41d43-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="41d43-123">Se non viene specificato, il valore esistente rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="41d43-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="41d43-124">-Name</span><span class="sxs-lookup"><span data-stu-id="41d43-124">-Name</span></span>
<span data-ttu-id="41d43-125">Nome della prenotazione</span><span class="sxs-lookup"><span data-stu-id="41d43-125">Name of Reservation</span></span>

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

### <span data-ttu-id="41d43-126">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="41d43-126">-Reservation</span></span>
<span data-ttu-id="41d43-127">Parametro per l'oggetto pipe per `Reservation`</span><span class="sxs-lookup"><span data-stu-id="41d43-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="41d43-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="41d43-128">-ReservationId</span></span>
<span data-ttu-id="41d43-129">ID `Reservation` dell'elemento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="41d43-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="41d43-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="41d43-130">-ReservationOrderId</span></span>
<span data-ttu-id="41d43-131">ID `ReservationOrder` dell'elemento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="41d43-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="41d43-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41d43-132">-Confirm</span></span>
<span data-ttu-id="41d43-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d43-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d43-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d43-134">-WhatIf</span></span>
<span data-ttu-id="41d43-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41d43-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41d43-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41d43-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d43-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d43-137">CommonParameters</span></span>
<span data-ttu-id="41d43-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d43-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d43-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41d43-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d43-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="41d43-140">INPUTS</span></span>

### <span data-ttu-id="41d43-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="41d43-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="41d43-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41d43-142">OUTPUTS</span></span>

### <span data-ttu-id="41d43-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="41d43-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="41d43-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="41d43-144">NOTES</span></span>

## <span data-ttu-id="41d43-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41d43-145">RELATED LINKS</span></span>
