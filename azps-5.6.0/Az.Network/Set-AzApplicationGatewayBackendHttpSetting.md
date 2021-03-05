---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: d784d3de33f535690e631c4deb21208b76f58078
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993521"
---
# <span data-ttu-id="9ac98-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ac98-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="9ac98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac98-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac98-103">Aggiorna le impostazioni HTTP back-end per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9ac98-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="9ac98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ac98-104">SYNTAX</span></span>

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

## <span data-ttu-id="9ac98-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9ac98-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac98-106">Il Set-AzApplicationGatewayBackendHttpSetting cmdlet aggiorna le impostazioni HTTP (Hypertext Transfer Protocol) back-end per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac98-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="9ac98-107">Le impostazioni HTTP di back-end vengono applicate a tutti i server back-end in un pool.</span><span class="sxs-lookup"><span data-stu-id="9ac98-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="9ac98-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ac98-108">EXAMPLES</span></span>

### <span data-ttu-id="9ac98-109">Esempio 1: Aggiornare le impostazioni HTTP back-end per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9ac98-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="9ac98-110">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="9ac98-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9ac98-111">Il secondo comando aggiorna le impostazioni HTTP del gateway applicazione nella variabile $AppGw per usare la porta 88, il protocollo HTTP e abilita l'affinità basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="9ac98-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="9ac98-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ac98-112">PARAMETERS</span></span>

### <span data-ttu-id="9ac98-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="9ac98-113">-AffinityCookieName</span></span>
<span data-ttu-id="9ac98-114">Nome cookie da usare per il cookie di affinità</span><span class="sxs-lookup"><span data-stu-id="9ac98-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="9ac98-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ac98-115">-ApplicationGateway</span></span>
<span data-ttu-id="9ac98-116">Specifica un oggetto gateway applicazione a cui questo cmdlet associa le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="9ac98-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="9ac98-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="9ac98-118">Specifica i certificati di autenticazione per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9ac98-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="9ac98-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac98-119">-ConnectionDraining</span></span>
<span data-ttu-id="9ac98-120">Esigomento della connessione della risorsa delle impostazioni http back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="9ac98-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="9ac98-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="9ac98-122">Specifica se l'affinità basata su cookie deve essere abilitata o disabilitata per il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="9ac98-123">I valori accettabili per questo parametro sono: Disabled o Enabled.</span><span class="sxs-lookup"><span data-stu-id="9ac98-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="9ac98-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac98-124">-DefaultProfile</span></span>
<span data-ttu-id="9ac98-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac98-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ac98-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="9ac98-126">-HostName</span></span>
<span data-ttu-id="9ac98-127">Imposta l'intestazione host da inviare ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="9ac98-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9ac98-128">-Name</span></span>
<span data-ttu-id="9ac98-129">Specifica il nome dell'oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="9ac98-130">-Path</span><span class="sxs-lookup"><span data-stu-id="9ac98-130">-Path</span></span>
<span data-ttu-id="9ac98-131">Percorso che deve essere usato come prefisso per tutte le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ac98-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="9ac98-132">Se per questo parametro non viene fornito alcun valore, non verrà specificato alcun percorso con prefisso.</span><span class="sxs-lookup"><span data-stu-id="9ac98-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="9ac98-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="9ac98-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="9ac98-134">Contrassegnare se è necessario selezionare l'intestazione host dal nome host del server back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="9ac98-135">-Port</span><span class="sxs-lookup"><span data-stu-id="9ac98-135">-Port</span></span>
<span data-ttu-id="9ac98-136">Specifica la porta da usare per ogni server nel pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="9ac98-137">-Snodato</span><span class="sxs-lookup"><span data-stu-id="9ac98-137">-Probe</span></span>
<span data-ttu-id="9ac98-138">Specifica un nome da associare alle impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="9ac98-139">-LambdaId</span><span class="sxs-lookup"><span data-stu-id="9ac98-139">-ProbeId</span></span>
<span data-ttu-id="9ac98-140">Specifica l'ID dell'elemento da associare alle impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="9ac98-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9ac98-141">-Protocol</span></span>
<span data-ttu-id="9ac98-142">Specifica il protocollo da usare per le comunicazioni tra il gateway applicazione e i server back-end.</span><span class="sxs-lookup"><span data-stu-id="9ac98-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="9ac98-143">I valori accettabili per questo parametro sono Http e Https.</span><span class="sxs-lookup"><span data-stu-id="9ac98-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="9ac98-144">Questo parametro fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9ac98-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="9ac98-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="9ac98-145">-RequestTimeout</span></span>
<span data-ttu-id="9ac98-146">Specifica un valore di timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="9ac98-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="9ac98-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9ac98-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="9ac98-148">Certificati radice attendibili per gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9ac98-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="9ac98-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac98-149">CommonParameters</span></span>
<span data-ttu-id="9ac98-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac98-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac98-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac98-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac98-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="9ac98-152">INPUTS</span></span>

### <span data-ttu-id="9ac98-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ac98-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ac98-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ac98-154">OUTPUTS</span></span>

### <span data-ttu-id="9ac98-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ac98-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ac98-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="9ac98-156">NOTES</span></span>

## <span data-ttu-id="9ac98-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ac98-157">RELATED LINKS</span></span>

[<span data-ttu-id="9ac98-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ac98-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9ac98-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ac98-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9ac98-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ac98-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9ac98-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ac98-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

