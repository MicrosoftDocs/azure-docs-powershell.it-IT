---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 6c5729ec4d450ad122e359b9bd009000212e3b0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678188"
---
# <span data-ttu-id="079a0-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="079a0-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="079a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="079a0-102">SYNOPSIS</span></span>
<span data-ttu-id="079a0-103">Rimuove le impostazioni HTTP di back-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="079a0-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="079a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="079a0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="079a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="079a0-105">DESCRIPTION</span></span>
<span data-ttu-id="079a0-106">Il cmdlet Remove-AzApplicationGatewayBackendHttpSetting rimuove le impostazioni HTTP (back-end Hypertext Transfer Protocol) da un gateway di applicazioni di Azure.</span><span class="sxs-lookup"><span data-stu-id="079a0-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="079a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="079a0-107">EXAMPLES</span></span>

### <span data-ttu-id="079a0-108">Esempio 1: rimuovere le impostazioni HTTP di back-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="079a0-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="079a0-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="079a0-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="079a0-110">Il secondo comando rimuove l'impostazione HTTP back-end denominata BackEndSetting02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="079a0-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="079a0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="079a0-111">PARAMETERS</span></span>

### <span data-ttu-id="079a0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="079a0-112">-ApplicationGateway</span></span>
<span data-ttu-id="079a0-113">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="079a0-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="079a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="079a0-114">-DefaultProfile</span></span>
<span data-ttu-id="079a0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="079a0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="079a0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="079a0-116">-Name</span></span>
<span data-ttu-id="079a0-117">Specifica il nome delle impostazioni HTTP back-end rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="079a0-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="079a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="079a0-118">CommonParameters</span></span>
<span data-ttu-id="079a0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="079a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="079a0-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="079a0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="079a0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="079a0-121">INPUTS</span></span>

### <span data-ttu-id="079a0-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="079a0-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="079a0-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="079a0-123">OUTPUTS</span></span>

### <span data-ttu-id="079a0-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="079a0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="079a0-125">Note</span><span class="sxs-lookup"><span data-stu-id="079a0-125">NOTES</span></span>

## <span data-ttu-id="079a0-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="079a0-126">RELATED LINKS</span></span>

[<span data-ttu-id="079a0-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="079a0-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="079a0-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="079a0-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="079a0-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="079a0-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="079a0-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="079a0-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

