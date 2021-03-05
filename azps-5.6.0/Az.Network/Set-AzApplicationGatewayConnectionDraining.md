---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 84a9ccb86f9fd1d4995ad52e913059181c0b887e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967789"
---
# <span data-ttu-id="76d77-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76d77-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="76d77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d77-102">SYNOPSIS</span></span>
<span data-ttu-id="76d77-103">Modifica la configurazione di esecolo della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="76d77-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="76d77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76d77-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76d77-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76d77-105">DESCRIPTION</span></span>
<span data-ttu-id="76d77-106">Il cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione di esente della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="76d77-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="76d77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76d77-107">EXAMPLES</span></span>

### <span data-ttu-id="76d77-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76d77-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="76d77-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="76d77-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="76d77-110">Il secondo comando recupera le impostazioni HTTP di back-end denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="76d77-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="76d77-111">L'ultimo comando modifica la configurazione di escolo della connessione dell'oggetto impostazioni HTTP back-end archiviato in $Settings impostando Enabled su False e DrainTimeoutInSec su 3600.</span><span class="sxs-lookup"><span data-stu-id="76d77-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="76d77-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76d77-112">PARAMETERS</span></span>

### <span data-ttu-id="76d77-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76d77-113">-BackendHttpSettings</span></span>
<span data-ttu-id="76d77-114">Impostazioni http back-end</span><span class="sxs-lookup"><span data-stu-id="76d77-114">The backend http settings</span></span>

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

### <span data-ttu-id="76d77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d77-115">-DefaultProfile</span></span>
<span data-ttu-id="76d77-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76d77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76d77-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="76d77-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="76d77-118">Il numero di secondi per cui è attivo lo scaricamento della connessione.</span><span class="sxs-lookup"><span data-stu-id="76d77-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="76d77-119">I valori accettabili sono da 1 secondo a 3600 secondi.</span><span class="sxs-lookup"><span data-stu-id="76d77-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="76d77-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="76d77-120">-Enabled</span></span>
<span data-ttu-id="76d77-121">Se lo scaricamento delle connessioni è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="76d77-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="76d77-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d77-122">CommonParameters</span></span>
<span data-ttu-id="76d77-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d77-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d77-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76d77-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d77-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="76d77-125">INPUTS</span></span>

### <span data-ttu-id="76d77-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76d77-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="76d77-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76d77-127">OUTPUTS</span></span>

### <span data-ttu-id="76d77-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76d77-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="76d77-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="76d77-129">NOTES</span></span>

## <span data-ttu-id="76d77-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76d77-130">RELATED LINKS</span></span>

[<span data-ttu-id="76d77-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76d77-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="76d77-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="76d77-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="76d77-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76d77-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="76d77-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76d77-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="76d77-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76d77-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

