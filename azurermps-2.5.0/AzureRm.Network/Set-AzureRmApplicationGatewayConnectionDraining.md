---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: ab876b5bc0ea63a2299ec17168b56125c9dbcdba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866232"
---
# <span data-ttu-id="42e9d-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="42e9d-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="42e9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="42e9d-103">Modifica la configurazione di svuotamento della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="42e9d-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42e9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42e9d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42e9d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42e9d-105">DESCRIPTION</span></span>
<span data-ttu-id="42e9d-106">Il cmdlet **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione di svuotamento della connessione di un oggetto impostazioni http back-end.</span><span class="sxs-lookup"><span data-stu-id="42e9d-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="42e9d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42e9d-107">EXAMPLES</span></span>

### <span data-ttu-id="42e9d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42e9d-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="42e9d-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="42e9d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="42e9d-110">Il secondo comando recupera le impostazioni HTTP di back-end denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings.</span><span class="sxs-lookup"><span data-stu-id="42e9d-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="42e9d-111">L'ultimo comando consente di modificare la configurazione di svuotamento della connessione dell'oggetto impostazioni HTTP back-end archiviato in $Settings impostando Enabled su false e DrainTimeoutInSec in 3600.</span><span class="sxs-lookup"><span data-stu-id="42e9d-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="42e9d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42e9d-112">PARAMETERS</span></span>

### <span data-ttu-id="42e9d-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="42e9d-113">-BackendHttpSettings</span></span>
<span data-ttu-id="42e9d-114">Impostazioni http di backend</span><span class="sxs-lookup"><span data-stu-id="42e9d-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42e9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e9d-115">-DefaultProfile</span></span>
<span data-ttu-id="42e9d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42e9d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42e9d-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="42e9d-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="42e9d-118">Il numero di secondi di svuotamento della connessione è attivo.</span><span class="sxs-lookup"><span data-stu-id="42e9d-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="42e9d-119">I valori accettabili sono da 1 secondo a 3600 secondi.</span><span class="sxs-lookup"><span data-stu-id="42e9d-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="42e9d-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="42e9d-120">-Enabled</span></span>
<span data-ttu-id="42e9d-121">Se lo svuotamento della connessione è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="42e9d-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="42e9d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e9d-122">CommonParameters</span></span>
<span data-ttu-id="42e9d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e9d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e9d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e9d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e9d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42e9d-125">INPUTS</span></span>

### <span data-ttu-id="42e9d-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="42e9d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="42e9d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42e9d-127">OUTPUTS</span></span>

### <span data-ttu-id="42e9d-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="42e9d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="42e9d-129">Note</span><span class="sxs-lookup"><span data-stu-id="42e9d-129">NOTES</span></span>

## <span data-ttu-id="42e9d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42e9d-130">RELATED LINKS</span></span>

[<span data-ttu-id="42e9d-131">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42e9d-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="42e9d-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="42e9d-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="42e9d-133">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="42e9d-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="42e9d-134">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="42e9d-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="42e9d-135">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="42e9d-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

