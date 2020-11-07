---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 813569705831dcd3d8c379b3c40078184498899e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860593"
---
# <span data-ttu-id="6a0e3-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6a0e3-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="6a0e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0e3-103">Crea una nuova connessione che svuota la configurazione per le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="6a0e3-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="6a0e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a0e3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a0e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="6a0e3-106">Il cmdlet **New-AzApplicationGatewayConnectionDraining** crea una nuova configurazione di svuotamento delle connessioni per le impostazioni http di back-end.</span><span class="sxs-lookup"><span data-stu-id="6a0e3-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="6a0e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a0e3-107">EXAMPLES</span></span>

### <span data-ttu-id="6a0e3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a0e3-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="6a0e3-109">Il comando crea una nuova connessione che svuota la configurazione con Enabled impostato su true e DrainTimeoutInSec impostato su 42 secondi e lo archivia in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="6a0e3-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="6a0e3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a0e3-110">PARAMETERS</span></span>

### <span data-ttu-id="6a0e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0e3-111">-DefaultProfile</span></span>
<span data-ttu-id="6a0e3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a0e3-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="6a0e3-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="6a0e3-114">Il numero di secondi di svuotamento della connessione è attivo.</span><span class="sxs-lookup"><span data-stu-id="6a0e3-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="6a0e3-115">I valori accettabili sono da 1 secondo a 3600 secondi.</span><span class="sxs-lookup"><span data-stu-id="6a0e3-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="6a0e3-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="6a0e3-116">-Enabled</span></span>
<span data-ttu-id="6a0e3-117">Se lo svuotamento della connessione è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="6a0e3-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="6a0e3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0e3-118">CommonParameters</span></span>
<span data-ttu-id="6a0e3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a0e3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0e3-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a0e3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0e3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a0e3-121">INPUTS</span></span>

### <span data-ttu-id="6a0e3-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a0e3-122">None</span></span>

## <span data-ttu-id="6a0e3-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a0e3-123">OUTPUTS</span></span>

### <span data-ttu-id="6a0e3-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6a0e3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="6a0e3-125">Note</span><span class="sxs-lookup"><span data-stu-id="6a0e3-125">NOTES</span></span>

## <span data-ttu-id="6a0e3-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a0e3-126">RELATED LINKS</span></span>

[<span data-ttu-id="6a0e3-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6a0e3-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="6a0e3-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6a0e3-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="6a0e3-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6a0e3-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

