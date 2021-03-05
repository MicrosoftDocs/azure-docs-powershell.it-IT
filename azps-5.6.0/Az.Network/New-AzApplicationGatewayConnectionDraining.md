---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b5bfedea118aa3770bac3141d05db379a4655906
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006221"
---
# <span data-ttu-id="d642c-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d642c-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="d642c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d642c-102">SYNOPSIS</span></span>
<span data-ttu-id="d642c-103">Crea una nuova configurazione di escolo della connessione per le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="d642c-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="d642c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d642c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d642c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d642c-105">DESCRIPTION</span></span>
<span data-ttu-id="d642c-106">Il cmdlet **New-AzApplicationGatewayConnectionDraining crea** una nuova configurazione di escolo della connessione per le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="d642c-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="d642c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d642c-107">EXAMPLES</span></span>

### <span data-ttu-id="d642c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d642c-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="d642c-109">Il comando crea una nuova configurazione di escolo della connessione con Enabled impostato su True e DrainTimeoutInSec impostato su 42 secondi e la archivia in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="d642c-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="d642c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d642c-110">PARAMETERS</span></span>

### <span data-ttu-id="d642c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d642c-111">-DefaultProfile</span></span>
<span data-ttu-id="d642c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d642c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d642c-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="d642c-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="d642c-114">Il numero di secondi per cui è attivo lo scaricamento della connessione.</span><span class="sxs-lookup"><span data-stu-id="d642c-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="d642c-115">I valori accettabili sono da 1 secondo a 3600 secondi.</span><span class="sxs-lookup"><span data-stu-id="d642c-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="d642c-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d642c-116">-Enabled</span></span>
<span data-ttu-id="d642c-117">Se lo scaricamento delle connessioni è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="d642c-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="d642c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d642c-118">CommonParameters</span></span>
<span data-ttu-id="d642c-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d642c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d642c-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d642c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d642c-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="d642c-121">INPUTS</span></span>

### <span data-ttu-id="d642c-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d642c-122">None</span></span>

## <span data-ttu-id="d642c-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d642c-123">OUTPUTS</span></span>

### <span data-ttu-id="d642c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d642c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="d642c-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="d642c-125">NOTES</span></span>

## <span data-ttu-id="d642c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d642c-126">RELATED LINKS</span></span>

[<span data-ttu-id="d642c-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d642c-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d642c-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d642c-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d642c-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d642c-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

