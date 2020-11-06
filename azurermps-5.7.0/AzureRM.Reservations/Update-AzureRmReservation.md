---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514140"
---
# <span data-ttu-id="d2f48-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d2f48-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="d2f48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2f48-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f48-103">Aggiornare una `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d2f48-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2f48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2f48-104">SYNTAX</span></span>

### <span data-ttu-id="d2f48-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2f48-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f48-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d2f48-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f48-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2f48-107">DESCRIPTION</span></span>
<span data-ttu-id="d2f48-108">Aggiorna gli ambiti applicati di `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d2f48-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="d2f48-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2f48-109">EXAMPLES</span></span>

### <span data-ttu-id="d2f48-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2f48-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="d2f48-111">Aggiorna il AppliedScopeType della prenotazione specificata in single</span><span class="sxs-lookup"><span data-stu-id="d2f48-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="d2f48-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d2f48-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="d2f48-113">Aggiorna il AppliedScopeType della prenotazione specificata in Shared</span><span class="sxs-lookup"><span data-stu-id="d2f48-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="d2f48-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2f48-114">PARAMETERS</span></span>

### <span data-ttu-id="d2f48-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="d2f48-115">-AppliedScope</span></span>
<span data-ttu-id="d2f48-116">SubscriptionId per applicare questa operazione `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d2f48-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f48-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="d2f48-117">-AppliedScopeType</span></span>
<span data-ttu-id="d2f48-118">Tipo di `Reservation` da aggiornare</span><span class="sxs-lookup"><span data-stu-id="d2f48-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f48-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f48-119">-DefaultProfile</span></span>
<span data-ttu-id="d2f48-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f48-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f48-121">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="d2f48-121">-Reservation</span></span>
<span data-ttu-id="d2f48-122">Parametro oggetto pipe per `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d2f48-122">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f48-123">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d2f48-123">-ReservationId</span></span>
<span data-ttu-id="d2f48-124">ID dell' `Reservation` aggiornamento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="d2f48-124">Id of the `Reservation` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f48-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d2f48-125">-ReservationOrderId</span></span>
<span data-ttu-id="d2f48-126">ID dell' `ReservationOrder` aggiornamento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="d2f48-126">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f48-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2f48-127">-Confirm</span></span>
<span data-ttu-id="d2f48-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2f48-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f48-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f48-129">-WhatIf</span></span>
<span data-ttu-id="d2f48-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2f48-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2f48-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2f48-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f48-132">CommonParameters</span></span>
<span data-ttu-id="d2f48-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f48-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2f48-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f48-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2f48-135">INPUTS</span></span>

### <span data-ttu-id="d2f48-136">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d2f48-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d2f48-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2f48-137">OUTPUTS</span></span>

### <span data-ttu-id="d2f48-138">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d2f48-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d2f48-139">Note</span><span class="sxs-lookup"><span data-stu-id="d2f48-139">NOTES</span></span>

## <span data-ttu-id="d2f48-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2f48-140">RELATED LINKS</span></span>

