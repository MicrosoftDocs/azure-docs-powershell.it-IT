---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 73d60d86110893005e72152c08e82d4152b1c482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509840"
---
# <span data-ttu-id="ce6fc-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce6fc-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="ce6fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6fc-103">Aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce6fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce6fc-104">SYNTAX</span></span>

### <span data-ttu-id="ce6fc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce6fc-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce6fc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ce6fc-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce6fc-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="ce6fc-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce6fc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce6fc-108">DESCRIPTION</span></span>
<span data-ttu-id="ce6fc-109">Il cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="ce6fc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce6fc-110">EXAMPLES</span></span>

### <span data-ttu-id="ce6fc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce6fc-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="ce6fc-112">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ce6fc-113">Il secondo comando aggiunge la configurazione di reindirizzamento al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="ce6fc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce6fc-114">PARAMETERS</span></span>

### <span data-ttu-id="ce6fc-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce6fc-115">-ApplicationGateway</span></span>
<span data-ttu-id="ce6fc-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce6fc-116">The applicationGateway</span></span>

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

### <span data-ttu-id="ce6fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce6fc-117">-DefaultProfile</span></span>
<span data-ttu-id="ce6fc-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce6fc-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="ce6fc-119">-IncludePath</span></span>
<span data-ttu-id="ce6fc-120">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-120">Include path in the redirected url.</span></span>
<span data-ttu-id="ce6fc-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6fc-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="ce6fc-122">-IncludeQueryString</span></span>
<span data-ttu-id="ce6fc-123">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="ce6fc-124">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-124">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6fc-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce6fc-125">-Name</span></span>
<span data-ttu-id="ce6fc-126">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="ce6fc-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="ce6fc-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="ce6fc-127">-RedirectType</span></span>
<span data-ttu-id="ce6fc-128">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="ce6fc-128">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6fc-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="ce6fc-129">-TargetListener</span></span>
<span data-ttu-id="ce6fc-130">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="ce6fc-130">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6fc-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="ce6fc-131">-TargetListenerID</span></span>
<span data-ttu-id="ce6fc-132">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="ce6fc-132">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6fc-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="ce6fc-133">-TargetUrl</span></span>
<span data-ttu-id="ce6fc-134">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="ce6fc-134">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6fc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce6fc-135">CommonParameters</span></span>
<span data-ttu-id="ce6fc-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce6fc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce6fc-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce6fc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce6fc-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce6fc-138">INPUTS</span></span>

### <span data-ttu-id="ce6fc-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce6fc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce6fc-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce6fc-140">OUTPUTS</span></span>

### <span data-ttu-id="ce6fc-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce6fc-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce6fc-142">Note</span><span class="sxs-lookup"><span data-stu-id="ce6fc-142">NOTES</span></span>

## <span data-ttu-id="ce6fc-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce6fc-143">RELATED LINKS</span></span>

