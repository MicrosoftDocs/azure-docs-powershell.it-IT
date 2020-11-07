---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 449c3999a3041be819b9f5f665054969223c1557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687513"
---
# <span data-ttu-id="7ea56-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ea56-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7ea56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ea56-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea56-103">Aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ea56-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ea56-104">SYNTAX</span></span>

### <span data-ttu-id="7ea56-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea56-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea56-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7ea56-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea56-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="7ea56-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea56-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ea56-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea56-109">Il cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ea56-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="7ea56-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ea56-110">EXAMPLES</span></span>

### <span data-ttu-id="7ea56-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7ea56-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="7ea56-112">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7ea56-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7ea56-113">Il secondo comando aggiunge la configurazione di reindirizzamento al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ea56-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="7ea56-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ea56-114">PARAMETERS</span></span>

### <span data-ttu-id="7ea56-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ea56-115">-ApplicationGateway</span></span>
<span data-ttu-id="7ea56-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ea56-116">The applicationGateway</span></span>

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

### <span data-ttu-id="7ea56-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="7ea56-117">-IncludePath</span></span>
<span data-ttu-id="7ea56-118">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="7ea56-118">Include path in the redirected url.</span></span>
<span data-ttu-id="7ea56-119">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="7ea56-119">Default is true.</span></span>

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

### <span data-ttu-id="7ea56-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="7ea56-120">-IncludeQueryString</span></span>
<span data-ttu-id="7ea56-121">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="7ea56-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="7ea56-122">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="7ea56-122">Default is true.</span></span>

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

### <span data-ttu-id="7ea56-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ea56-123">-Name</span></span>
<span data-ttu-id="7ea56-124">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="7ea56-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="7ea56-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="7ea56-125">-RedirectType</span></span>
<span data-ttu-id="7ea56-126">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="7ea56-126">The type of redirect</span></span>

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

### <span data-ttu-id="7ea56-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="7ea56-127">-TargetListener</span></span>
<span data-ttu-id="7ea56-128">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="7ea56-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="7ea56-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="7ea56-129">-TargetListenerID</span></span>
<span data-ttu-id="7ea56-130">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="7ea56-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="7ea56-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="7ea56-131">-TargetUrl</span></span>
<span data-ttu-id="7ea56-132">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="7ea56-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="7ea56-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea56-133">-DefaultProfile</span></span>
<span data-ttu-id="7ea56-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea56-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ea56-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea56-135">CommonParameters</span></span>
<span data-ttu-id="7ea56-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea56-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea56-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea56-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea56-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ea56-138">INPUTS</span></span>

### <span data-ttu-id="7ea56-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ea56-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ea56-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ea56-140">OUTPUTS</span></span>

### <span data-ttu-id="7ea56-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ea56-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ea56-142">Note</span><span class="sxs-lookup"><span data-stu-id="7ea56-142">NOTES</span></span>

## <span data-ttu-id="7ea56-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ea56-143">RELATED LINKS</span></span>

