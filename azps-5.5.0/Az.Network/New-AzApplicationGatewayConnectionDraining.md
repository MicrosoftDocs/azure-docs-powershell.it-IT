---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184542"
---
# <span data-ttu-id="900bd-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="900bd-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="900bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="900bd-102">SYNOPSIS</span></span>
<span data-ttu-id="900bd-103">Crea una nuova configurazione di escolo della connessione per le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="900bd-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="900bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="900bd-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="900bd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="900bd-105">DESCRIPTION</span></span>
<span data-ttu-id="900bd-106">Il cmdlet **New-AzApplicationGatewayConnectionDraining** crea una nuova configurazione di escolo della connessione per le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="900bd-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="900bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="900bd-107">EXAMPLES</span></span>

### <span data-ttu-id="900bd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="900bd-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="900bd-109">Il comando crea una nuova configurazione di escolo della connessione con Enabled impostato su True e DrainTimeoutInSec impostato su 42 secondi e la archivia in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="900bd-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="900bd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="900bd-110">PARAMETERS</span></span>

### <span data-ttu-id="900bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="900bd-111">-DefaultProfile</span></span>
<span data-ttu-id="900bd-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="900bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="900bd-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="900bd-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="900bd-114">Il numero di secondi per cui è attivo lo scaricamento della connessione.</span><span class="sxs-lookup"><span data-stu-id="900bd-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="900bd-115">I valori accettabili sono da 1 secondo a 3600 secondi.</span><span class="sxs-lookup"><span data-stu-id="900bd-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="900bd-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="900bd-116">-Enabled</span></span>
<span data-ttu-id="900bd-117">Se lo scaricamento della connessione è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="900bd-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="900bd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="900bd-118">CommonParameters</span></span>
<span data-ttu-id="900bd-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="900bd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="900bd-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="900bd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="900bd-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="900bd-121">INPUTS</span></span>

### <span data-ttu-id="900bd-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="900bd-122">None</span></span>

## <span data-ttu-id="900bd-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="900bd-123">OUTPUTS</span></span>

### <span data-ttu-id="900bd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="900bd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="900bd-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="900bd-125">NOTES</span></span>

## <span data-ttu-id="900bd-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="900bd-126">RELATED LINKS</span></span>

[<span data-ttu-id="900bd-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="900bd-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="900bd-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="900bd-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="900bd-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="900bd-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

