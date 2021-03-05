---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: d3f774b078c1069fc5a2c2690996837f17a4c187
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994096"
---
# <span data-ttu-id="d5d3e-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d3e-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d5d3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d3e-103">Ottiene la configurazione del collegamento privato di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="d5d3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5d3e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5d3e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="d5d3e-106">Il cmdlet **Get-AzApplicationGatewayPrivateLinkConfiguration** ottiene la configurazione del collegamento privato di un gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="d5d3e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5d3e-107">EXAMPLES</span></span>

### <span data-ttu-id="d5d3e-108">Esempio 1: Ottenere una configurazione di collegamento privato specificata</span><span class="sxs-lookup"><span data-stu-id="d5d3e-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="d5d3e-109">Il primo comando ottiene un gateway applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d5d3e-110">Il secondo comando recupera la configurazione di collegamento privato denominata privateLinkConfig01 da $AppGw e la archivia nella variabile $PrivateLinkConfiguration private.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="d5d3e-111">Esempio 2: Ottenere un elenco di configurazione dei collegamenti privati</span><span class="sxs-lookup"><span data-stu-id="d5d3e-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="d5d3e-112">Il primo comando ottiene un gateway applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d5d3e-113">Il secondo comando recupera tutte le configurazioni di collegamento private $AppGw e le archivia nella $PrivateLinkConfigurations variabile.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="d5d3e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5d3e-114">PARAMETERS</span></span>

### <span data-ttu-id="d5d3e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5d3e-115">-ApplicationGateway</span></span>
<span data-ttu-id="d5d3e-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5d3e-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d3e-117">-DefaultProfile</span></span>
<span data-ttu-id="d5d3e-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d3e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d5d3e-119">-Name</span></span>
<span data-ttu-id="d5d3e-120">Nome della configurazione PrivateLink del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="d5d3e-120">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d3e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d3e-121">CommonParameters</span></span>
<span data-ttu-id="d5d3e-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d3e-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d3e-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5d3e-124">INPUTS</span></span>

### <span data-ttu-id="d5d3e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5d3e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5d3e-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5d3e-126">OUTPUTS</span></span>

### <span data-ttu-id="d5d3e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d3e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d5d3e-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5d3e-128">NOTES</span></span>

## <span data-ttu-id="d5d3e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5d3e-129">RELATED LINKS</span></span>

[<span data-ttu-id="d5d3e-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d3e-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d5d3e-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d3e-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d5d3e-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d3e-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d5d3e-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d3e-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)