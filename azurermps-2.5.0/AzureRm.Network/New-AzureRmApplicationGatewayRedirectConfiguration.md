---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865752"
---
# <span data-ttu-id="b01f0-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b01f0-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b01f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b01f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b01f0-103">Crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b01f0-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b01f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b01f0-104">SYNTAX</span></span>

### <span data-ttu-id="b01f0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b01f0-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b01f0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b01f0-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b01f0-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="b01f0-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b01f0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b01f0-108">DESCRIPTION</span></span>
<span data-ttu-id="b01f0-109">**Il cmdlet New-AzureRmApplicationGatewayRedirectConfiguration** crea una configurazione di reindirizzamento per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b01f0-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="b01f0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b01f0-110">EXAMPLES</span></span>

### <span data-ttu-id="b01f0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b01f0-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="b01f0-112">Questo comando crea una configurazione di reindirizzamento denominata Redirect01 e archivia il risultato nella variabile denominata $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="b01f0-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="b01f0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b01f0-113">PARAMETERS</span></span>

### <span data-ttu-id="b01f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01f0-114">-DefaultProfile</span></span>
<span data-ttu-id="b01f0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b01f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b01f0-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="b01f0-116">-IncludePath</span></span>
<span data-ttu-id="b01f0-117">Includere Path nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="b01f0-117">Include path in the redirected url.</span></span>
<span data-ttu-id="b01f0-118">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="b01f0-118">Default is true.</span></span>

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

### <span data-ttu-id="b01f0-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="b01f0-119">-IncludeQueryString</span></span>
<span data-ttu-id="b01f0-120">Includere una stringa di query nell'URL reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="b01f0-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="b01f0-121">L'impostazione predefinita è true.</span><span class="sxs-lookup"><span data-stu-id="b01f0-121">Default is true.</span></span>

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

### <span data-ttu-id="b01f0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b01f0-122">-Name</span></span>
<span data-ttu-id="b01f0-123">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b01f0-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="b01f0-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="b01f0-124">-RedirectType</span></span>
<span data-ttu-id="b01f0-125">Tipo di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b01f0-125">The type of redirect</span></span>

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

### <span data-ttu-id="b01f0-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="b01f0-126">-TargetListener</span></span>
<span data-ttu-id="b01f0-127">HTTPListener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="b01f0-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="b01f0-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="b01f0-128">-TargetListenerID</span></span>
<span data-ttu-id="b01f0-129">ID del listener per reindirizzare la richiesta a</span><span class="sxs-lookup"><span data-stu-id="b01f0-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="b01f0-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="b01f0-130">-TargetUrl</span></span>
<span data-ttu-id="b01f0-131">URL di destinazione per il reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b01f0-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="b01f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01f0-132">CommonParameters</span></span>
<span data-ttu-id="b01f0-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b01f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01f0-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b01f0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01f0-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b01f0-135">INPUTS</span></span>

### <span data-ttu-id="b01f0-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b01f0-136">None</span></span>

## <span data-ttu-id="b01f0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b01f0-137">OUTPUTS</span></span>

### <span data-ttu-id="b01f0-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b01f0-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b01f0-139">Note</span><span class="sxs-lookup"><span data-stu-id="b01f0-139">NOTES</span></span>

## <span data-ttu-id="b01f0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b01f0-140">RELATED LINKS</span></span>

