---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302544"
---
# <span data-ttu-id="85210-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="85210-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="85210-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85210-102">SYNOPSIS</span></span>
<span data-ttu-id="85210-103">Ottenere il catalogo delle prenotazioni disponibili</span><span class="sxs-lookup"><span data-stu-id="85210-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="85210-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85210-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85210-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85210-105">DESCRIPTION</span></span>
<span data-ttu-id="85210-106">Ottenere le aree geografiche e le SKU disponibili per l'acquisto di istanze riservate per l'abbonamento Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="85210-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="85210-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85210-107">EXAMPLES</span></span>

### <span data-ttu-id="85210-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85210-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="85210-109">Ottenere il catalogo VirtualMachines in westus per l'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="85210-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="85210-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="85210-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="85210-111">Ottenere il catalogo Riferimentorapido SUSELinux per la sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="85210-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="85210-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85210-112">PARAMETERS</span></span>

### <span data-ttu-id="85210-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85210-113">-DefaultProfile</span></span>
<span data-ttu-id="85210-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85210-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85210-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="85210-115">-Location</span></span>
<span data-ttu-id="85210-116">Specifica la posizione delle risorse riservate nel catalogo</span><span class="sxs-lookup"><span data-stu-id="85210-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="85210-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="85210-117">-ReservedResourceType</span></span>
<span data-ttu-id="85210-118">Specifica il tipo di risorse riservate nel catalogo</span><span class="sxs-lookup"><span data-stu-id="85210-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="85210-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85210-119">-SubscriptionId</span></span>
<span data-ttu-id="85210-120">ID dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="85210-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85210-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85210-121">CommonParameters</span></span>
<span data-ttu-id="85210-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85210-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85210-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85210-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85210-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85210-124">INPUTS</span></span>

### <span data-ttu-id="85210-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="85210-125">None</span></span>

## <span data-ttu-id="85210-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85210-126">OUTPUTS</span></span>

### <span data-ttu-id="85210-127">Microsoft. Azure. Commands. reservations. Models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="85210-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="85210-128">Note</span><span class="sxs-lookup"><span data-stu-id="85210-128">NOTES</span></span>

## <span data-ttu-id="85210-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85210-129">RELATED LINKS</span></span>
