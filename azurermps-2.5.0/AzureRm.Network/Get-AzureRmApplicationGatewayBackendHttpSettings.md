---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 366b3545e54c1465bf2eaf050a9e9199288fce5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866308"
---
# <span data-ttu-id="bbc22-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bbc22-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="bbc22-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbc22-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc22-103">Ottiene le impostazioni HTTP di back-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bbc22-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbc22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbc22-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbc22-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbc22-105">DESCRIPTION</span></span>
<span data-ttu-id="bbc22-106">Il cmdlet Get-AzureRmApplicationGatewayBackendHttpSettings ottiene le impostazioni HTTP di back-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bbc22-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="bbc22-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbc22-107">EXAMPLES</span></span>

### <span data-ttu-id="bbc22-108">Esempio 1: ottenere le impostazioni HTTP di back-end per nome</span><span class="sxs-lookup"><span data-stu-id="bbc22-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="bbc22-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene le impostazioni HTTP denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings.</span><span class="sxs-lookup"><span data-stu-id="bbc22-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="bbc22-110">Esempio 2: ottenere una raccolta di impostazioni HTTP di back-end</span><span class="sxs-lookup"><span data-stu-id="bbc22-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="bbc22-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene la raccolta di impostazioni HTTP per $AppGw e archivia le impostazioni nella variabile $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="bbc22-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="bbc22-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbc22-112">PARAMETERS</span></span>

### <span data-ttu-id="bbc22-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbc22-113">-ApplicationGateway</span></span>
<span data-ttu-id="bbc22-114">Specifica un oggetto gateway dell'applicazione che contiene le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="bbc22-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="bbc22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc22-115">-DefaultProfile</span></span>
<span data-ttu-id="bbc22-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc22-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbc22-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbc22-117">-Name</span></span>
<span data-ttu-id="bbc22-118">Specifica il nome delle impostazioni HTTP di backend che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="bbc22-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bbc22-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc22-119">CommonParameters</span></span>
<span data-ttu-id="bbc22-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc22-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc22-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc22-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc22-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbc22-122">INPUTS</span></span>

### <span data-ttu-id="bbc22-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bbc22-123">System.String</span></span>

## <span data-ttu-id="bbc22-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbc22-124">OUTPUTS</span></span>

### <span data-ttu-id="bbc22-125">Microsoft. Azure. Commands. Network. Models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bbc22-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="bbc22-126">Note</span><span class="sxs-lookup"><span data-stu-id="bbc22-126">NOTES</span></span>

## <span data-ttu-id="bbc22-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbc22-127">RELATED LINKS</span></span>

[<span data-ttu-id="bbc22-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bbc22-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="bbc22-129">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bbc22-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="bbc22-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bbc22-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="bbc22-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bbc22-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

