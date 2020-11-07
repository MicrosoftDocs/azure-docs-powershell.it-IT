---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 1816b7407ec1d36f8eb5fd213484e22a9e89998c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865927"
---
# <span data-ttu-id="8e413-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e413-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="8e413-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e413-102">SYNOPSIS</span></span>
<span data-ttu-id="8e413-103">Aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8e413-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e413-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e413-104">SYNTAX</span></span>

### <span data-ttu-id="8e413-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e413-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e413-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8e413-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e413-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="8e413-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e413-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e413-108">DESCRIPTION</span></span>
<span data-ttu-id="8e413-109">Il cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8e413-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="8e413-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e413-110">EXAMPLES</span></span>

### <span data-ttu-id="8e413-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e413-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="8e413-112">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8e413-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8e413-113">Il secondo comando aggiunge la configurazione di reindirizzamento al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8e413-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="8e413-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e413-114">PARAMETERS</span></span>

### <span data-ttu-id="8e413-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e413-115">-ApplicationGateway</span></span>
<span data-ttu-id="8e413-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e413-116">The applicationGateway</span></span>

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

### <span data-ttu-id="8e413-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e413-117">-DefaultProfile</span></span>
<span data-ttu-id="8e413-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e413-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e413-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="8e413-119">-IncludePath</span></span>
<span data-ttu-id="8e413-120">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="8e413-120">Include path in the redirected url.</span></span>
<span data-ttu-id="8e413-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="8e413-121">Default is true.</span></span>

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

### <span data-ttu-id="8e413-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="8e413-122">-IncludeQueryString</span></span>
<span data-ttu-id="8e413-123">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="8e413-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="8e413-124">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="8e413-124">Default is true.</span></span>

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

### <span data-ttu-id="8e413-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e413-125">-Name</span></span>
<span data-ttu-id="8e413-126">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="8e413-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="8e413-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="8e413-127">-RedirectType</span></span>
<span data-ttu-id="8e413-128">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="8e413-128">The type of redirect</span></span>

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

### <span data-ttu-id="8e413-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="8e413-129">-TargetListener</span></span>
<span data-ttu-id="8e413-130">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="8e413-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="8e413-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="8e413-131">-TargetListenerID</span></span>
<span data-ttu-id="8e413-132">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="8e413-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="8e413-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="8e413-133">-TargetUrl</span></span>
<span data-ttu-id="8e413-134">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="8e413-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="8e413-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e413-135">CommonParameters</span></span>
<span data-ttu-id="8e413-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e413-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e413-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e413-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e413-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e413-138">INPUTS</span></span>

### <span data-ttu-id="8e413-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e413-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e413-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e413-140">OUTPUTS</span></span>

### <span data-ttu-id="8e413-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e413-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e413-142">Note</span><span class="sxs-lookup"><span data-stu-id="8e413-142">NOTES</span></span>

## <span data-ttu-id="8e413-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e413-143">RELATED LINKS</span></span>

