---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032960"
---
# <span data-ttu-id="8aee3-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8aee3-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="8aee3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8aee3-102">SYNOPSIS</span></span>
<span data-ttu-id="8aee3-103">Ottiene le impostazioni HTTP di back-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8aee3-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="8aee3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8aee3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aee3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8aee3-105">DESCRIPTION</span></span>
<span data-ttu-id="8aee3-106">Il cmdlet Get-AzApplicationGatewayBackendHttpSetting ottiene le impostazioni HTTP di back-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8aee3-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="8aee3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8aee3-107">EXAMPLES</span></span>

### <span data-ttu-id="8aee3-108">Esempio 1: ottenere le impostazioni HTTP di back-end per nome</span><span class="sxs-lookup"><span data-stu-id="8aee3-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="8aee3-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene le impostazioni HTTP denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings.</span><span class="sxs-lookup"><span data-stu-id="8aee3-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="8aee3-110">Esempio 2: ottenere una raccolta di impostazioni HTTP di back-end</span><span class="sxs-lookup"><span data-stu-id="8aee3-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="8aee3-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene la raccolta di impostazioni HTTP per $AppGw e archivia le impostazioni nella variabile $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="8aee3-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="8aee3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8aee3-112">PARAMETERS</span></span>

### <span data-ttu-id="8aee3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8aee3-113">-ApplicationGateway</span></span>
<span data-ttu-id="8aee3-114">Specifica un oggetto gateway dell'applicazione che contiene le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="8aee3-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="8aee3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aee3-115">-DefaultProfile</span></span>
<span data-ttu-id="8aee3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8aee3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aee3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8aee3-117">-Name</span></span>
<span data-ttu-id="8aee3-118">Specifica il nome delle impostazioni HTTP di backend che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="8aee3-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aee3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aee3-119">CommonParameters</span></span>
<span data-ttu-id="8aee3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aee3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aee3-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aee3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aee3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8aee3-122">INPUTS</span></span>

### <span data-ttu-id="8aee3-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8aee3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8aee3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8aee3-124">OUTPUTS</span></span>

### <span data-ttu-id="8aee3-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8aee3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="8aee3-126">Note</span><span class="sxs-lookup"><span data-stu-id="8aee3-126">NOTES</span></span>

## <span data-ttu-id="8aee3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8aee3-127">RELATED LINKS</span></span>

[<span data-ttu-id="8aee3-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8aee3-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="8aee3-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8aee3-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="8aee3-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8aee3-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="8aee3-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8aee3-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

