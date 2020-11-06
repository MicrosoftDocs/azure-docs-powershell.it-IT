---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 7f3834e13ce6fb6c3e9a661fead09ffcfab78933
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520494"
---
# <span data-ttu-id="ead76-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ead76-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="ead76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ead76-102">SYNOPSIS</span></span>
<span data-ttu-id="ead76-103">Crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ead76-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ead76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ead76-104">SYNTAX</span></span>

### <span data-ttu-id="ead76-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ead76-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ead76-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ead76-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ead76-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="ead76-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ead76-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ead76-108">DESCRIPTION</span></span>
<span data-ttu-id="ead76-109">**Il cmdlet New-AzureRmApplicationGatewayRedirectConfiguration** crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ead76-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="ead76-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ead76-110">EXAMPLES</span></span>

### <span data-ttu-id="ead76-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ead76-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="ead76-112">Questo comando crea una configurazione di reindirizzamento denominata Redirect01 e archivia il risultato nella variabile denominata $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="ead76-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="ead76-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ead76-113">PARAMETERS</span></span>

### <span data-ttu-id="ead76-114">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="ead76-114">-IncludePath</span></span>
<span data-ttu-id="ead76-115">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="ead76-115">Include path in the redirected url.</span></span>
<span data-ttu-id="ead76-116">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="ead76-116">Default is true.</span></span>

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

### <span data-ttu-id="ead76-117">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="ead76-117">-IncludeQueryString</span></span>
<span data-ttu-id="ead76-118">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="ead76-118">Include query string in the redirected url.</span></span>
<span data-ttu-id="ead76-119">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="ead76-119">Default is true.</span></span>

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

### <span data-ttu-id="ead76-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ead76-120">-Name</span></span>
<span data-ttu-id="ead76-121">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="ead76-121">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="ead76-122">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="ead76-122">-RedirectType</span></span>
<span data-ttu-id="ead76-123">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="ead76-123">The type of redirect</span></span>

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

### <span data-ttu-id="ead76-124">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="ead76-124">-TargetListener</span></span>
<span data-ttu-id="ead76-125">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="ead76-125">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="ead76-126">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="ead76-126">-TargetListenerID</span></span>
<span data-ttu-id="ead76-127">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="ead76-127">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="ead76-128">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="ead76-128">-TargetUrl</span></span>
<span data-ttu-id="ead76-129">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="ead76-129">Target URL fo redirection</span></span>

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

### <span data-ttu-id="ead76-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead76-130">-DefaultProfile</span></span>
<span data-ttu-id="ead76-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ead76-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ead76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead76-132">CommonParameters</span></span>
<span data-ttu-id="ead76-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead76-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ead76-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead76-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ead76-135">INPUTS</span></span>

### <span data-ttu-id="ead76-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ead76-136">None</span></span>

## <span data-ttu-id="ead76-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ead76-137">OUTPUTS</span></span>

### <span data-ttu-id="ead76-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ead76-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="ead76-139">Note</span><span class="sxs-lookup"><span data-stu-id="ead76-139">NOTES</span></span>

## <span data-ttu-id="ead76-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ead76-140">RELATED LINKS</span></span>

