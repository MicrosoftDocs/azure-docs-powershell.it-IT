---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189481"
---
# <span data-ttu-id="3bc8a-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3bc8a-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="3bc8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3bc8a-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc8a-103">Aggiorna le impostazioni HTTP di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="3bc8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bc8a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc8a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bc8a-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc8a-106">Il cmdlet Set-AzApplicationGatewayBackendHttpSetting aggiorna le impostazioni HTTP (back-end Hypertext Transfer Protocol) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="3bc8a-107">Le impostazioni HTTP di back-end vengono applicate a tutti i server back-end in un pool.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="3bc8a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bc8a-108">EXAMPLES</span></span>

### <span data-ttu-id="3bc8a-109">Esempio 1: aggiornare le impostazioni HTTP di back-end per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3bc8a-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="3bc8a-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3bc8a-111">Il secondo comando Aggiorna le impostazioni HTTP del gateway dell'applicazione nella variabile $AppGw per usare la porta 88, il protocollo HTTP e consente l'affinità basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="3bc8a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3bc8a-112">PARAMETERS</span></span>

### <span data-ttu-id="3bc8a-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="3bc8a-113">-AffinityCookieName</span></span>
<span data-ttu-id="3bc8a-114">Nome del cookie da usare per il cookie di affinità</span><span class="sxs-lookup"><span data-stu-id="3bc8a-114">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3bc8a-115">-ApplicationGateway</span></span>
<span data-ttu-id="3bc8a-116">Specifica un oggetto gateway dell'applicazione con cui questo cmdlet associa le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="3bc8a-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="3bc8a-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="3bc8a-118">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-118">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="3bc8a-119">-ConnectionDraining</span></span>
<span data-ttu-id="3bc8a-120">Connessione che svuota la risorsa delle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-120">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="3bc8a-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="3bc8a-122">Specifica se l'affinità basata su cookie deve essere abilitata o disabilitata per il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="3bc8a-123">I valori accettabili per questo parametro sono: Disabled o Enabled.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc8a-124">-DefaultProfile</span></span>
<span data-ttu-id="3bc8a-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="3bc8a-126">-HostName</span></span>
<span data-ttu-id="3bc8a-127">Imposta l'intestazione host da inviare ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-127">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="3bc8a-128">-Name</span></span>
<span data-ttu-id="3bc8a-129">Specifica il nome dell'oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="3bc8a-130">-Path</span><span class="sxs-lookup"><span data-stu-id="3bc8a-130">-Path</span></span>
<span data-ttu-id="3bc8a-131">Percorso che deve essere usato come prefisso per tutte le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="3bc8a-132">Se per questo parametro non viene specificato alcun valore, non verrà preceduto alcun percorso.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="3bc8a-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="3bc8a-134">Contrassegna se l'intestazione host deve essere selezionata dal nome host del server back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-134">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-135">-Porta</span><span class="sxs-lookup"><span data-stu-id="3bc8a-135">-Port</span></span>
<span data-ttu-id="3bc8a-136">Specifica la porta da usare per ogni server nel pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-136">Specifies the port to use for each server in the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-137">-Probe</span><span class="sxs-lookup"><span data-stu-id="3bc8a-137">-Probe</span></span>
<span data-ttu-id="3bc8a-138">Specifica una sonda da associare alle impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="3bc8a-139">-ProbeId</span></span>
<span data-ttu-id="3bc8a-140">Specifica l'ID del Probe da associare alle impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-141">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="3bc8a-141">-Protocol</span></span>
<span data-ttu-id="3bc8a-142">Specifica il protocollo da usare per la comunicazione tra il gateway dell'applicazione e i server back-end.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="3bc8a-143">I valori accettabili per questo parametro sono: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="3bc8a-144">Questo parametro fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-144">This parameter is case-sensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="3bc8a-145">-RequestTimeout</span></span>
<span data-ttu-id="3bc8a-146">Specifica un valore di timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-146">Specifies a request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3bc8a-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="3bc8a-148">Certificati radice attendibili del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3bc8a-148">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc8a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc8a-149">CommonParameters</span></span>
<span data-ttu-id="3bc8a-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc8a-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc8a-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc8a-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3bc8a-152">INPUTS</span></span>

### <span data-ttu-id="3bc8a-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3bc8a-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3bc8a-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bc8a-154">OUTPUTS</span></span>

### <span data-ttu-id="3bc8a-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3bc8a-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3bc8a-156">Note</span><span class="sxs-lookup"><span data-stu-id="3bc8a-156">NOTES</span></span>

## <span data-ttu-id="3bc8a-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bc8a-157">RELATED LINKS</span></span>

[<span data-ttu-id="3bc8a-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3bc8a-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="3bc8a-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3bc8a-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="3bc8a-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3bc8a-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="3bc8a-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3bc8a-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

