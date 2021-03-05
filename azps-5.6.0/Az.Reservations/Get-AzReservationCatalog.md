---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 77fb1806ba2cbdd2e0398bcdf8289aed62c085fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000302"
---
# <span data-ttu-id="f0c41-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="f0c41-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="f0c41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c41-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c41-103">Ottenere il catalogo delle prenotazioni disponibili</span><span class="sxs-lookup"><span data-stu-id="f0c41-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="f0c41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0c41-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0c41-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0c41-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c41-106">Ottenere le aree geografiche e le SKU disponibili per l'acquisto di istanze riservate per la sottoscrizione di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="f0c41-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="f0c41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0c41-107">EXAMPLES</span></span>

### <span data-ttu-id="f0c41-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0c41-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="f0c41-109">Ottenere il catalogo VirtualMachines in WestUs per l'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="f0c41-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="f0c41-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f0c41-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="f0c41-111">Ottenere il catalogo SuseLinux per l'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="f0c41-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="f0c41-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0c41-112">PARAMETERS</span></span>

### <span data-ttu-id="f0c41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c41-113">-DefaultProfile</span></span>
<span data-ttu-id="f0c41-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0c41-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f0c41-115">-Location</span></span>
<span data-ttu-id="f0c41-116">Specifica la posizione delle risorse riservate nel catalogo</span><span class="sxs-lookup"><span data-stu-id="f0c41-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="f0c41-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="f0c41-117">-ReservedResourceType</span></span>
<span data-ttu-id="f0c41-118">Specifica il tipo di risorse riservate nel catalogo</span><span class="sxs-lookup"><span data-stu-id="f0c41-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="f0c41-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0c41-119">-SubscriptionId</span></span>
<span data-ttu-id="f0c41-120">ID della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="f0c41-120">Id of the subscription</span></span>

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

### <span data-ttu-id="f0c41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c41-121">CommonParameters</span></span>
<span data-ttu-id="f0c41-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c41-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0c41-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c41-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0c41-124">INPUTS</span></span>

### <span data-ttu-id="f0c41-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0c41-125">None</span></span>

## <span data-ttu-id="f0c41-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0c41-126">OUTPUTS</span></span>

### <span data-ttu-id="f0c41-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="f0c41-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="f0c41-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0c41-128">NOTES</span></span>

## <span data-ttu-id="f0c41-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0c41-129">RELATED LINKS</span></span>
