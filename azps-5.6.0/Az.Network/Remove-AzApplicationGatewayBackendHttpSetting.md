---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 24c3a0264250bf9defc8be8b046f48ea94f28244
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955774"
---
# <span data-ttu-id="a8738-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a8738-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="a8738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8738-102">SYNOPSIS</span></span>
<span data-ttu-id="a8738-103">Rimuove le impostazioni HTTP di back-end da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a8738-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="a8738-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8738-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8738-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8738-105">DESCRIPTION</span></span>
<span data-ttu-id="a8738-106">Il cmdlet Remove-AzApplicationGatewayBackendHttpSetting rimuove le impostazioni HTTP (Hypertext Transfer Protocol) back-end da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8738-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="a8738-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8738-107">EXAMPLES</span></span>

### <span data-ttu-id="a8738-108">Esempio 1: Rimuovere le impostazioni HTTP back-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="a8738-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="a8738-109">Il primo comando ottiene un gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="a8738-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a8738-110">Il secondo comando rimuove l'impostazione HTTP back-end denominata BackEndSetting02 dal gateway applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a8738-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a8738-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8738-111">PARAMETERS</span></span>

### <span data-ttu-id="a8738-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8738-112">-ApplicationGateway</span></span>
<span data-ttu-id="a8738-113">Specifica il gateway applicazione da cui questo cmdlet rimuove le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="a8738-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a8738-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8738-114">-DefaultProfile</span></span>
<span data-ttu-id="a8738-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8738-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8738-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a8738-116">-Name</span></span>
<span data-ttu-id="a8738-117">Specifica il nome delle impostazioni HTTP back-end rimosse dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8738-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8738-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8738-118">CommonParameters</span></span>
<span data-ttu-id="a8738-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8738-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8738-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8738-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8738-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8738-121">INPUTS</span></span>

### <span data-ttu-id="a8738-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8738-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a8738-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8738-123">OUTPUTS</span></span>

### <span data-ttu-id="a8738-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8738-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a8738-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8738-125">NOTES</span></span>

## <span data-ttu-id="a8738-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8738-126">RELATED LINKS</span></span>

[<span data-ttu-id="a8738-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a8738-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a8738-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a8738-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a8738-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a8738-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a8738-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a8738-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

