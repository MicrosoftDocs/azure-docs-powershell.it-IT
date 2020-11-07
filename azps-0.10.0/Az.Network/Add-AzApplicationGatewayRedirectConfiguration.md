---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 60b98db10aab4456ea8ca463f49ee3f7f58ffdd2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861009"
---
# <span data-ttu-id="13147-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="13147-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="13147-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13147-102">SYNOPSIS</span></span>
<span data-ttu-id="13147-103">Aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13147-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="13147-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13147-104">SYNTAX</span></span>

### <span data-ttu-id="13147-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="13147-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13147-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="13147-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13147-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="13147-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13147-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13147-108">DESCRIPTION</span></span>
<span data-ttu-id="13147-109">Il cmdlet **Add-AzApplicationGatewayRedirectConfiguration** aggiunge una configurazione di reindirizzamento a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13147-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="13147-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13147-110">EXAMPLES</span></span>

### <span data-ttu-id="13147-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13147-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="13147-112">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="13147-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="13147-113">Il secondo comando aggiunge la configurazione di reindirizzamento al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13147-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="13147-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13147-114">PARAMETERS</span></span>

### <span data-ttu-id="13147-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13147-115">-ApplicationGateway</span></span>
<span data-ttu-id="13147-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13147-116">The applicationGateway</span></span>

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

### <span data-ttu-id="13147-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13147-117">-DefaultProfile</span></span>
<span data-ttu-id="13147-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13147-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13147-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="13147-119">-IncludePath</span></span>
<span data-ttu-id="13147-120">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="13147-120">Include path in the redirected url.</span></span>
<span data-ttu-id="13147-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="13147-121">Default is true.</span></span>

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

### <span data-ttu-id="13147-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="13147-122">-IncludeQueryString</span></span>
<span data-ttu-id="13147-123">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="13147-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="13147-124">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="13147-124">Default is true.</span></span>

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

### <span data-ttu-id="13147-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="13147-125">-Name</span></span>
<span data-ttu-id="13147-126">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="13147-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="13147-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="13147-127">-RedirectType</span></span>
<span data-ttu-id="13147-128">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="13147-128">The type of redirect</span></span>

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

### <span data-ttu-id="13147-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="13147-129">-TargetListener</span></span>
<span data-ttu-id="13147-130">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="13147-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="13147-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="13147-131">-TargetListenerID</span></span>
<span data-ttu-id="13147-132">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="13147-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="13147-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="13147-133">-TargetUrl</span></span>
<span data-ttu-id="13147-134">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="13147-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="13147-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13147-135">CommonParameters</span></span>
<span data-ttu-id="13147-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13147-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13147-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13147-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13147-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13147-138">INPUTS</span></span>

### <span data-ttu-id="13147-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13147-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13147-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13147-140">OUTPUTS</span></span>

### <span data-ttu-id="13147-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13147-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13147-142">Note</span><span class="sxs-lookup"><span data-stu-id="13147-142">NOTES</span></span>

## <span data-ttu-id="13147-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13147-143">RELATED LINKS</span></span>

