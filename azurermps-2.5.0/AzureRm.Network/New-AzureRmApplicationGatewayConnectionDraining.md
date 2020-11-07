---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: 6e17db790cd776e8662c4c445e53604dcb8929de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866265"
---
# <span data-ttu-id="65940-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="65940-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="65940-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65940-102">SYNOPSIS</span></span>
<span data-ttu-id="65940-103">Crea una nuova connessione che svuota la configurazione per le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="65940-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65940-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65940-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65940-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65940-105">DESCRIPTION</span></span>
<span data-ttu-id="65940-106">Il cmdlet **New-AzureRmApplicationGatewayConnectionDraining** crea una nuova configurazione di svuotamento delle connessioni per le impostazioni http di back-end.</span><span class="sxs-lookup"><span data-stu-id="65940-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="65940-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65940-107">EXAMPLES</span></span>

### <span data-ttu-id="65940-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65940-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="65940-109">Il comando crea una nuova connessione che svuota la configurazione con Enabled impostato su true e DrainTimeoutInSec impostato su 42 secondi e lo archivia in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="65940-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="65940-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65940-110">PARAMETERS</span></span>

### <span data-ttu-id="65940-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65940-111">-DefaultProfile</span></span>
<span data-ttu-id="65940-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65940-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65940-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="65940-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="65940-114">Il numero di secondi di svuotamento della connessione è attivo.</span><span class="sxs-lookup"><span data-stu-id="65940-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="65940-115">I valori accettabili sono da 1 secondo a 3600 secondi.</span><span class="sxs-lookup"><span data-stu-id="65940-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65940-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="65940-116">-Enabled</span></span>
<span data-ttu-id="65940-117">Se lo svuotamento della connessione è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="65940-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65940-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65940-118">CommonParameters</span></span>
<span data-ttu-id="65940-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65940-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65940-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65940-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65940-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65940-121">INPUTS</span></span>

### <span data-ttu-id="65940-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="65940-122">None</span></span>

## <span data-ttu-id="65940-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65940-123">OUTPUTS</span></span>

### <span data-ttu-id="65940-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="65940-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="65940-125">Note</span><span class="sxs-lookup"><span data-stu-id="65940-125">NOTES</span></span>

## <span data-ttu-id="65940-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65940-126">RELATED LINKS</span></span>

[<span data-ttu-id="65940-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="65940-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="65940-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="65940-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="65940-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="65940-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

