---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 27c677846889824ddd290871fd4507f1b8218365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515560"
---
# <span data-ttu-id="24275-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24275-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="24275-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24275-102">SYNOPSIS</span></span>
<span data-ttu-id="24275-103">Crea impostazioni HTTP di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24275-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24275-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24275-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24275-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24275-105">DESCRIPTION</span></span>
<span data-ttu-id="24275-106">Il cmdlet New-AzureRmApplicationGatewayBackendHttpSettings crea le impostazioni HTTP di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24275-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="24275-107">Le impostazioni HTTP di back-end vengono applicate a tutti i server back-end in un pool.</span><span class="sxs-lookup"><span data-stu-id="24275-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="24275-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24275-108">EXAMPLES</span></span>

### <span data-ttu-id="24275-109">Esempio 1: creare impostazioni HTTP di back-end</span><span class="sxs-lookup"><span data-stu-id="24275-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="24275-110">Questo comando crea le impostazioni HTTP di back-end denominate Setting01 sulla porta 80, usando il protocollo HTTP, con l'affinità basata su cookie disabilitata.</span><span class="sxs-lookup"><span data-stu-id="24275-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="24275-111">Le impostazioni sono archiviate nella variabile $Setting.</span><span class="sxs-lookup"><span data-stu-id="24275-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="24275-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24275-112">PARAMETERS</span></span>

### <span data-ttu-id="24275-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="24275-113">-AffinityCookieName</span></span>
<span data-ttu-id="24275-114">Nome del cookie da usare per il cookie di affinità</span><span class="sxs-lookup"><span data-stu-id="24275-114">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="24275-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="24275-116">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24275-116">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="24275-117">-ConnectionDraining</span></span>
<span data-ttu-id="24275-118">Connessione che svuota la risorsa delle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="24275-118">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="24275-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="24275-120">Specifica se l'affinità basata su cookie deve essere abilitata o disabilitata per il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="24275-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24275-121">-DefaultProfile</span></span>
<span data-ttu-id="24275-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24275-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24275-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="24275-123">-HostName</span></span>
<span data-ttu-id="24275-124">Imposta l'intestazione host da inviare ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="24275-124">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="24275-125">-Name</span></span>
<span data-ttu-id="24275-126">Specifica il nome delle impostazioni HTTP di back-end create da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24275-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="24275-127">-Path</span><span class="sxs-lookup"><span data-stu-id="24275-127">-Path</span></span>
<span data-ttu-id="24275-128">Percorso che deve essere usato come prefisso per tutte le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="24275-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="24275-129">Se per questo parametro non viene specificato alcun valore, non verrà preceduto alcun percorso.</span><span class="sxs-lookup"><span data-stu-id="24275-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="24275-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="24275-131">Contrassegna se l'intestazione host deve essere selezionata dal nome host del server back-end.</span><span class="sxs-lookup"><span data-stu-id="24275-131">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-132">-Porta</span><span class="sxs-lookup"><span data-stu-id="24275-132">-Port</span></span>
<span data-ttu-id="24275-133">Specifica la porta del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="24275-133">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-134">-Probe</span><span class="sxs-lookup"><span data-stu-id="24275-134">-Probe</span></span>
<span data-ttu-id="24275-135">Specifica una sonda da associare al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="24275-135">Specifies a probe to associate with the back-end server pool.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-136">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="24275-136">-ProbeEnabled</span></span>
<span data-ttu-id="24275-137">Contrassegno se la sonda deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="24275-137">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="24275-138">-ProbeId</span></span>
<span data-ttu-id="24275-139">Specifica l'ID del Probe da associare al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="24275-139">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-140">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="24275-140">-Protocol</span></span>
<span data-ttu-id="24275-141">Specifica il protocollo da usare per la comunicazione tra il gateway dell'applicazione e i server back-end.</span><span class="sxs-lookup"><span data-stu-id="24275-141">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="24275-142">I valori accettabili per questo parametro sono: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="24275-142">The acceptable values for this parameter are: Http and Https.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="24275-143">-RequestTimeout</span></span>
<span data-ttu-id="24275-144">Specifica un valore di timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="24275-144">Specifies a request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24275-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24275-145">CommonParameters</span></span>
<span data-ttu-id="24275-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24275-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24275-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24275-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24275-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24275-148">INPUTS</span></span>

### <span data-ttu-id="24275-149">System. String</span><span class="sxs-lookup"><span data-stu-id="24275-149">System.String</span></span>

## <span data-ttu-id="24275-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24275-150">OUTPUTS</span></span>

### <span data-ttu-id="24275-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24275-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="24275-152">Note</span><span class="sxs-lookup"><span data-stu-id="24275-152">NOTES</span></span>

## <span data-ttu-id="24275-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24275-153">RELATED LINKS</span></span>

[<span data-ttu-id="24275-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24275-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="24275-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24275-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="24275-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24275-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="24275-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24275-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

