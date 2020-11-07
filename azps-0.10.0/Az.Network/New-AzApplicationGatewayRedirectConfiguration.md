---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 5cf1e01be8d0a76ba8dc319c5241f40613ad4304
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860553"
---
# <span data-ttu-id="a3010-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3010-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="a3010-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3010-102">SYNOPSIS</span></span>
<span data-ttu-id="a3010-103">Crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3010-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="a3010-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3010-104">SYNTAX</span></span>

### <span data-ttu-id="a3010-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3010-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3010-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a3010-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3010-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="a3010-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3010-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3010-108">DESCRIPTION</span></span>
<span data-ttu-id="a3010-109">**Il cmdlet New-AzApplicationGatewayRedirectConfiguration** crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3010-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="a3010-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3010-110">EXAMPLES</span></span>

### <span data-ttu-id="a3010-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3010-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="a3010-112">Questo comando crea una configurazione di reindirizzamento denominata Redirect01 e archivia il risultato nella variabile denominata $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="a3010-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="a3010-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3010-113">PARAMETERS</span></span>

### <span data-ttu-id="a3010-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3010-114">-DefaultProfile</span></span>
<span data-ttu-id="a3010-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3010-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3010-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="a3010-116">-IncludePath</span></span>
<span data-ttu-id="a3010-117">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="a3010-117">Include path in the redirected url.</span></span>
<span data-ttu-id="a3010-118">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="a3010-118">Default is true.</span></span>

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

### <span data-ttu-id="a3010-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="a3010-119">-IncludeQueryString</span></span>
<span data-ttu-id="a3010-120">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="a3010-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="a3010-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="a3010-121">Default is true.</span></span>

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

### <span data-ttu-id="a3010-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3010-122">-Name</span></span>
<span data-ttu-id="a3010-123">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="a3010-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="a3010-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="a3010-124">-RedirectType</span></span>
<span data-ttu-id="a3010-125">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="a3010-125">The type of redirect</span></span>

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

### <span data-ttu-id="a3010-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="a3010-126">-TargetListener</span></span>
<span data-ttu-id="a3010-127">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="a3010-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="a3010-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="a3010-128">-TargetListenerID</span></span>
<span data-ttu-id="a3010-129">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="a3010-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="a3010-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="a3010-130">-TargetUrl</span></span>
<span data-ttu-id="a3010-131">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="a3010-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="a3010-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3010-132">CommonParameters</span></span>
<span data-ttu-id="a3010-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3010-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3010-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3010-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3010-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3010-135">INPUTS</span></span>

### <span data-ttu-id="a3010-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a3010-136">None</span></span>

## <span data-ttu-id="a3010-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3010-137">OUTPUTS</span></span>

### <span data-ttu-id="a3010-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3010-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="a3010-139">Note</span><span class="sxs-lookup"><span data-stu-id="a3010-139">NOTES</span></span>

## <span data-ttu-id="a3010-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3010-140">RELATED LINKS</span></span>

