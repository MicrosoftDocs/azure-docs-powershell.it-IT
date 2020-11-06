---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ca03b95748203546fb8d9235cb7822a4dde359a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521192"
---
# <span data-ttu-id="ca895-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca895-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ca895-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca895-102">SYNOPSIS</span></span>
<span data-ttu-id="ca895-103">Crea una nuova connessione che svuota la configurazione per le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="ca895-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca895-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca895-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca895-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca895-105">DESCRIPTION</span></span>
<span data-ttu-id="ca895-106">Il cmdlet **New-AzureRmApplicationGatewayConnectionDraining** crea una nuova configurazione di svuotamento delle connessioni per le impostazioni http di back-end.</span><span class="sxs-lookup"><span data-stu-id="ca895-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="ca895-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca895-107">EXAMPLES</span></span>

### <span data-ttu-id="ca895-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca895-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="ca895-109">Il comando crea una nuova connessione che svuota la configurazione con Enabled impostato su true e DrainTimeoutInSec impostato su 42 secondi e lo archivia in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="ca895-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="ca895-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca895-110">PARAMETERS</span></span>

### <span data-ttu-id="ca895-111">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="ca895-111">-DrainTimeoutInSec</span></span>
<span data-ttu-id="ca895-112">Il numero di secondi di svuotamento della connessione è attivo.</span><span class="sxs-lookup"><span data-stu-id="ca895-112">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="ca895-113">I valori accettabili sono da 1 secondo a 3600 secondi.</span><span class="sxs-lookup"><span data-stu-id="ca895-113">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca895-114">-Enabled</span><span class="sxs-lookup"><span data-stu-id="ca895-114">-Enabled</span></span>
<span data-ttu-id="ca895-115">Se lo svuotamento della connessione è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="ca895-115">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca895-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca895-116">-DefaultProfile</span></span>
<span data-ttu-id="ca895-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca895-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca895-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca895-118">CommonParameters</span></span>
<span data-ttu-id="ca895-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca895-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca895-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca895-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca895-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca895-121">INPUTS</span></span>

### <span data-ttu-id="ca895-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ca895-122">None</span></span>

## <span data-ttu-id="ca895-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca895-123">OUTPUTS</span></span>

### <span data-ttu-id="ca895-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca895-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ca895-125">Note</span><span class="sxs-lookup"><span data-stu-id="ca895-125">NOTES</span></span>

## <span data-ttu-id="ca895-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca895-126">RELATED LINKS</span></span>

[<span data-ttu-id="ca895-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca895-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ca895-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca895-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ca895-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca895-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

