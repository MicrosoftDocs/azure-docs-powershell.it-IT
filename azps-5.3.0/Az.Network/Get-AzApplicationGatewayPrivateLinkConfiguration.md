---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475518"
---
# <span data-ttu-id="48af0-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="48af0-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="48af0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48af0-102">SYNOPSIS</span></span>
<span data-ttu-id="48af0-103">Ottiene la configurazione del collegamento privato di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48af0-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="48af0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48af0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48af0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48af0-105">DESCRIPTION</span></span>
<span data-ttu-id="48af0-106">Il cmdlet **Get-AzApplicationGatewayPrivateLinkConfiguration** ottiene la configurazione del collegamento privato di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48af0-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="48af0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48af0-107">EXAMPLES</span></span>

### <span data-ttu-id="48af0-108">Esempio 1: ottenere una configurazione di collegamento privato specificata</span><span class="sxs-lookup"><span data-stu-id="48af0-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="48af0-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="48af0-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="48af0-110">Il secondo comando ottiene la configurazione del collegamento privato denominata privateLinkConfig01 da $AppGw e la archivia nella variabile $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="48af0-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="48af0-111">Esempio 2: ottenere un elenco di configurazione dei collegamenti privati</span><span class="sxs-lookup"><span data-stu-id="48af0-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="48af0-112">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="48af0-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="48af0-113">Il secondo comando ottiene tutte le configurazioni di collegamenti privati da $AppGw e lo archivia nella variabile $PrivateLinkConfigurations.</span><span class="sxs-lookup"><span data-stu-id="48af0-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="48af0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48af0-114">PARAMETERS</span></span>

### <span data-ttu-id="48af0-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48af0-115">-ApplicationGateway</span></span>
<span data-ttu-id="48af0-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48af0-116">The applicationGateway</span></span>

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

### <span data-ttu-id="48af0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48af0-117">-DefaultProfile</span></span>
<span data-ttu-id="48af0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48af0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48af0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="48af0-119">-Name</span></span>
<span data-ttu-id="48af0-120">Nome della configurazione di privateLink del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="48af0-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="48af0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48af0-121">CommonParameters</span></span>
<span data-ttu-id="48af0-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48af0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48af0-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48af0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48af0-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48af0-124">INPUTS</span></span>

### <span data-ttu-id="48af0-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48af0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48af0-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48af0-126">OUTPUTS</span></span>

### <span data-ttu-id="48af0-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="48af0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="48af0-128">Note</span><span class="sxs-lookup"><span data-stu-id="48af0-128">NOTES</span></span>

## <span data-ttu-id="48af0-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48af0-129">RELATED LINKS</span></span>

[<span data-ttu-id="48af0-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="48af0-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="48af0-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="48af0-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="48af0-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="48af0-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="48af0-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="48af0-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)