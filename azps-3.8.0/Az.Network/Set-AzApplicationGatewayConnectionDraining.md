---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 76c017589afd5f8ef0abb6f016dbc80bb5bc30d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019321"
---
# <span data-ttu-id="c1dfd-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c1dfd-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c1dfd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="c1dfd-103">Modifica la configurazione di svuotamento della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c1dfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1dfd-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1dfd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="c1dfd-106">Il cmdlet **set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione di svuotamento della connessione di un oggetto impostazioni http back-end.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c1dfd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1dfd-107">EXAMPLES</span></span>

### <span data-ttu-id="c1dfd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1dfd-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="c1dfd-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c1dfd-110">Il secondo comando recupera le impostazioni HTTP di back-end denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="c1dfd-111">L'ultimo comando consente di modificare la configurazione di svuotamento della connessione dell'oggetto impostazioni HTTP back-end archiviato in $Settings impostando Enabled su false e DrainTimeoutInSec in 3600.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="c1dfd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1dfd-112">PARAMETERS</span></span>

### <span data-ttu-id="c1dfd-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1dfd-113">-BackendHttpSettings</span></span>
<span data-ttu-id="c1dfd-114">Impostazioni http di backend</span><span class="sxs-lookup"><span data-stu-id="c1dfd-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1dfd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1dfd-115">-DefaultProfile</span></span>
<span data-ttu-id="c1dfd-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1dfd-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="c1dfd-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="c1dfd-118">Il numero di secondi di svuotamento della connessione è attivo.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="c1dfd-119">I valori accettabili sono da 1 secondo a 3600 secondi.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="c1dfd-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="c1dfd-120">-Enabled</span></span>
<span data-ttu-id="c1dfd-121">Se lo svuotamento della connessione è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="c1dfd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1dfd-122">CommonParameters</span></span>
<span data-ttu-id="c1dfd-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1dfd-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1dfd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1dfd-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1dfd-125">INPUTS</span></span>

### <span data-ttu-id="c1dfd-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1dfd-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c1dfd-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1dfd-127">OUTPUTS</span></span>

### <span data-ttu-id="c1dfd-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1dfd-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c1dfd-129">Note</span><span class="sxs-lookup"><span data-stu-id="c1dfd-129">NOTES</span></span>

## <span data-ttu-id="c1dfd-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1dfd-130">RELATED LINKS</span></span>

[<span data-ttu-id="c1dfd-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1dfd-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c1dfd-132">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1dfd-132">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="c1dfd-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c1dfd-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c1dfd-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c1dfd-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c1dfd-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c1dfd-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

