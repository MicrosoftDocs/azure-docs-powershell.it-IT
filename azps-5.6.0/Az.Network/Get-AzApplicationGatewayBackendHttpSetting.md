---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 957417d7751080a82ddc8785abdd124c8f723303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003613"
---
# <span data-ttu-id="f2e37-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f2e37-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="f2e37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e37-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e37-103">Recupera le impostazioni HTTP back-end di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2e37-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="f2e37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2e37-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2e37-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2e37-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e37-106">Il Get-AzApplicationGatewayBackendHttpSetting cmdlet recupera le impostazioni HTTP back-end di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2e37-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="f2e37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2e37-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e37-108">Esempio 1: Ottenere le impostazioni HTTP di back-end in base al nome</span><span class="sxs-lookup"><span data-stu-id="f2e37-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="f2e37-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile. Il secondo comando ottiene le impostazioni HTTP denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings locale.</span><span class="sxs-lookup"><span data-stu-id="f2e37-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="f2e37-110">Esempio 2: Ottenere una raccolta di impostazioni HTTP di back-end</span><span class="sxs-lookup"><span data-stu-id="f2e37-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="f2e37-111">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile. Il secondo comando ottiene la raccolta di impostazioni HTTP per $AppGw e archivia le impostazioni nella $SettingsList variabile.</span><span class="sxs-lookup"><span data-stu-id="f2e37-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="f2e37-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2e37-112">PARAMETERS</span></span>

### <span data-ttu-id="f2e37-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2e37-113">-ApplicationGateway</span></span>
<span data-ttu-id="f2e37-114">Specifica un oggetto gateway applicazione che contiene impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="f2e37-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f2e37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e37-115">-DefaultProfile</span></span>
<span data-ttu-id="f2e37-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e37-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e37-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f2e37-117">-Name</span></span>
<span data-ttu-id="f2e37-118">Specifica il nome delle impostazioni HTTP back-end che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="f2e37-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f2e37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e37-119">CommonParameters</span></span>
<span data-ttu-id="f2e37-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e37-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2e37-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e37-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2e37-122">INPUTS</span></span>

### <span data-ttu-id="f2e37-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2e37-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2e37-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2e37-124">OUTPUTS</span></span>

### <span data-ttu-id="f2e37-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f2e37-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f2e37-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2e37-126">NOTES</span></span>

## <span data-ttu-id="f2e37-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2e37-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2e37-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f2e37-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f2e37-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f2e37-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f2e37-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f2e37-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f2e37-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f2e37-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

