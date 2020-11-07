---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 5070d455402548888e08e85ee3e8c5629e0282a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519407"
---
# <span data-ttu-id="19055-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="19055-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="19055-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19055-102">SYNOPSIS</span></span>
<span data-ttu-id="19055-103">Rimuove le impostazioni HTTP di back-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19055-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19055-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19055-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19055-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19055-105">DESCRIPTION</span></span>
<span data-ttu-id="19055-106">Il cmdlet Remove-AzureRmApplicationGatewayBackendHttpSettings rimuove le impostazioni HTTP (back-end Hypertext Transfer Protocol) da un gateway di applicazioni di Azure.</span><span class="sxs-lookup"><span data-stu-id="19055-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="19055-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19055-107">EXAMPLES</span></span>

### <span data-ttu-id="19055-108">Esempio 1: rimuovere le impostazioni HTTP di back-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="19055-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="19055-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="19055-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="19055-110">Il secondo comando rimuove l'impostazione HTTP back-end denominata BackEndSetting02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="19055-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="19055-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19055-111">PARAMETERS</span></span>

### <span data-ttu-id="19055-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19055-112">-ApplicationGateway</span></span>
<span data-ttu-id="19055-113">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="19055-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="19055-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19055-114">-DefaultProfile</span></span>
<span data-ttu-id="19055-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19055-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19055-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="19055-116">-Name</span></span>
<span data-ttu-id="19055-117">Specifica il nome delle impostazioni HTTP back-end rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19055-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19055-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19055-118">CommonParameters</span></span>
<span data-ttu-id="19055-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19055-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19055-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19055-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19055-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19055-121">INPUTS</span></span>

### <span data-ttu-id="19055-122">System. String</span><span class="sxs-lookup"><span data-stu-id="19055-122">System.String</span></span>

## <span data-ttu-id="19055-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19055-123">OUTPUTS</span></span>

### <span data-ttu-id="19055-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19055-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19055-125">Note</span><span class="sxs-lookup"><span data-stu-id="19055-125">NOTES</span></span>

## <span data-ttu-id="19055-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19055-126">RELATED LINKS</span></span>

[<span data-ttu-id="19055-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="19055-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="19055-128">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="19055-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="19055-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="19055-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="19055-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="19055-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()
