---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f9be647a4c6cb9d5198edcc766a20b3588e7626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510908"
---
# <span data-ttu-id="877be-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="877be-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="877be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="877be-102">SYNOPSIS</span></span>
<span data-ttu-id="877be-103">Ottiene la configurazione di scala automatica del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="877be-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="877be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="877be-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="877be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="877be-105">DESCRIPTION</span></span>
<span data-ttu-id="877be-106">Il cmdlet **Get-AzureRmApplicationGatewayAutoscaleConfiguration** ottiene la configurazione di scala automatica del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="877be-106">The **Get-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="877be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="877be-107">EXAMPLES</span></span>

### <span data-ttu-id="877be-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="877be-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="877be-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="877be-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="877be-110">Il secondo comando estrae la configurazione di scala automatica dal gateway applicationg.</span><span class="sxs-lookup"><span data-stu-id="877be-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="877be-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="877be-111">PARAMETERS</span></span>

### <span data-ttu-id="877be-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="877be-112">-ApplicationGateway</span></span>
<span data-ttu-id="877be-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="877be-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="877be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877be-114">-DefaultProfile</span></span>
<span data-ttu-id="877be-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="877be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="877be-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877be-116">CommonParameters</span></span>
<span data-ttu-id="877be-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="877be-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877be-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="877be-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877be-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="877be-119">INPUTS</span></span>

### <span data-ttu-id="877be-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="877be-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="877be-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="877be-121">OUTPUTS</span></span>

### <span data-ttu-id="877be-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="877be-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="877be-123">Note</span><span class="sxs-lookup"><span data-stu-id="877be-123">NOTES</span></span>

## <span data-ttu-id="877be-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="877be-124">RELATED LINKS</span></span>
