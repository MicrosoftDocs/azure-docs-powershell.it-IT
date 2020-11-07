---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 01f7daf47fa62e346dc7323ee5978f81f5797e29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688408"
---
# <span data-ttu-id="b148a-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b148a-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b148a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b148a-102">SYNOPSIS</span></span>
<span data-ttu-id="b148a-103">Aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b148a-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b148a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b148a-104">SYNTAX</span></span>

### <span data-ttu-id="b148a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b148a-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b148a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b148a-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b148a-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="b148a-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b148a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b148a-108">DESCRIPTION</span></span>
<span data-ttu-id="b148a-109">Il cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b148a-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="b148a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b148a-110">EXAMPLES</span></span>

### <span data-ttu-id="b148a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b148a-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="b148a-112">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b148a-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b148a-113">Il secondo comando aggiunge la configurazione di reindirizzamento al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b148a-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="b148a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b148a-114">PARAMETERS</span></span>

### <span data-ttu-id="b148a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b148a-115">-ApplicationGateway</span></span>
<span data-ttu-id="b148a-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b148a-116">The applicationGateway</span></span>

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

### <span data-ttu-id="b148a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b148a-117">-DefaultProfile</span></span>
<span data-ttu-id="b148a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b148a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b148a-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="b148a-119">-IncludePath</span></span>
<span data-ttu-id="b148a-120">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="b148a-120">Include path in the redirected url.</span></span>
<span data-ttu-id="b148a-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="b148a-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b148a-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="b148a-122">-IncludeQueryString</span></span>
<span data-ttu-id="b148a-123">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="b148a-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="b148a-124">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="b148a-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b148a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b148a-125">-Name</span></span>
<span data-ttu-id="b148a-126">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b148a-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="b148a-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="b148a-127">-RedirectType</span></span>
<span data-ttu-id="b148a-128">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b148a-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b148a-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="b148a-129">-TargetListener</span></span>
<span data-ttu-id="b148a-130">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="b148a-130">HTTPListener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b148a-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="b148a-131">-TargetListenerID</span></span>
<span data-ttu-id="b148a-132">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="b148a-132">ID of  listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b148a-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="b148a-133">-TargetUrl</span></span>
<span data-ttu-id="b148a-134">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b148a-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b148a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b148a-135">CommonParameters</span></span>
<span data-ttu-id="b148a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b148a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b148a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b148a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b148a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b148a-138">INPUTS</span></span>

### <span data-ttu-id="b148a-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b148a-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b148a-140">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b148a-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b148a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b148a-141">OUTPUTS</span></span>

### <span data-ttu-id="b148a-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b148a-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b148a-143">Note</span><span class="sxs-lookup"><span data-stu-id="b148a-143">NOTES</span></span>

## <span data-ttu-id="b148a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b148a-144">RELATED LINKS</span></span>
