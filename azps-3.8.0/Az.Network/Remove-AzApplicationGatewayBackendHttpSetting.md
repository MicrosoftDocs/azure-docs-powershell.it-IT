---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020002"
---
# <span data-ttu-id="531fa-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="531fa-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="531fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="531fa-102">SYNOPSIS</span></span>
<span data-ttu-id="531fa-103">Rimuove le impostazioni HTTP di back-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="531fa-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="531fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="531fa-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="531fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="531fa-105">DESCRIPTION</span></span>
<span data-ttu-id="531fa-106">Il cmdlet Remove-AzApplicationGatewayBackendHttpSetting rimuove le impostazioni HTTP (back-end Hypertext Transfer Protocol) da un gateway di applicazioni di Azure.</span><span class="sxs-lookup"><span data-stu-id="531fa-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="531fa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="531fa-107">EXAMPLES</span></span>

### <span data-ttu-id="531fa-108">Esempio 1: rimuovere le impostazioni HTTP di back-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="531fa-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="531fa-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="531fa-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="531fa-110">Il secondo comando rimuove l'impostazione HTTP back-end denominata BackEndSetting02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="531fa-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="531fa-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="531fa-111">PARAMETERS</span></span>

### <span data-ttu-id="531fa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="531fa-112">-ApplicationGateway</span></span>
<span data-ttu-id="531fa-113">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="531fa-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="531fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531fa-114">-DefaultProfile</span></span>
<span data-ttu-id="531fa-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="531fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="531fa-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="531fa-116">-Name</span></span>
<span data-ttu-id="531fa-117">Specifica il nome delle impostazioni HTTP back-end rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="531fa-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="531fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531fa-118">CommonParameters</span></span>
<span data-ttu-id="531fa-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="531fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531fa-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="531fa-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531fa-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="531fa-121">INPUTS</span></span>

### <span data-ttu-id="531fa-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="531fa-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="531fa-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="531fa-123">OUTPUTS</span></span>

### <span data-ttu-id="531fa-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="531fa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="531fa-125">Note</span><span class="sxs-lookup"><span data-stu-id="531fa-125">NOTES</span></span>

## <span data-ttu-id="531fa-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="531fa-126">RELATED LINKS</span></span>

[<span data-ttu-id="531fa-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="531fa-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="531fa-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="531fa-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="531fa-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="531fa-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="531fa-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="531fa-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

