---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 014309ceb54b1d16b2a55c97b03887deaf4ef281
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853601"
---
# <span data-ttu-id="bc475-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bc475-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="bc475-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc475-102">SYNOPSIS</span></span>
<span data-ttu-id="bc475-103">Crea l'impostazione HTTP back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc475-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="bc475-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc475-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc475-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc475-105">DESCRIPTION</span></span>
<span data-ttu-id="bc475-106">Il cmdlet New-AzApplicationGatewayBackendHttpSetting crea le impostazioni HTTP di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc475-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="bc475-107">Le impostazioni HTTP di back-end vengono applicate a tutti i server back-end in un pool.</span><span class="sxs-lookup"><span data-stu-id="bc475-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="bc475-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc475-108">EXAMPLES</span></span>

### <span data-ttu-id="bc475-109">Esempio 1: creare impostazioni HTTP di back-end</span><span class="sxs-lookup"><span data-stu-id="bc475-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="bc475-110">Questo comando crea le impostazioni HTTP di back-end denominate Setting01 sulla porta 80, usando il protocollo HTTP, con l'affinità basata su cookie disabilitata.</span><span class="sxs-lookup"><span data-stu-id="bc475-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="bc475-111">Le impostazioni sono archiviate nella variabile $Setting.</span><span class="sxs-lookup"><span data-stu-id="bc475-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="bc475-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc475-112">PARAMETERS</span></span>

### <span data-ttu-id="bc475-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="bc475-113">-AffinityCookieName</span></span>
<span data-ttu-id="bc475-114">Nome del cookie da usare per il cookie di affinità</span><span class="sxs-lookup"><span data-stu-id="bc475-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="bc475-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="bc475-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="bc475-116">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc475-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="bc475-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bc475-117">-ConnectionDraining</span></span>
<span data-ttu-id="bc475-118">Connessione che svuota la risorsa delle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="bc475-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="bc475-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="bc475-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="bc475-120">Specifica se l'affinità basata su cookie deve essere abilitata o disabilitata per il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="bc475-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="bc475-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc475-121">-DefaultProfile</span></span>
<span data-ttu-id="bc475-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc475-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc475-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="bc475-123">-HostName</span></span>
<span data-ttu-id="bc475-124">Imposta l'intestazione host da inviare ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="bc475-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="bc475-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc475-125">-Name</span></span>
<span data-ttu-id="bc475-126">Specifica il nome delle impostazioni HTTP di back-end create da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc475-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bc475-127">-Path</span><span class="sxs-lookup"><span data-stu-id="bc475-127">-Path</span></span>
<span data-ttu-id="bc475-128">Percorso che deve essere usato come prefisso per tutte le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="bc475-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="bc475-129">Se per questo parametro non viene specificato alcun valore, non verrà preceduto alcun percorso.</span><span class="sxs-lookup"><span data-stu-id="bc475-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="bc475-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="bc475-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="bc475-131">Contrassegna se l'intestazione host deve essere selezionata dal nome host del server back-end.</span><span class="sxs-lookup"><span data-stu-id="bc475-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="bc475-132">-Porta</span><span class="sxs-lookup"><span data-stu-id="bc475-132">-Port</span></span>
<span data-ttu-id="bc475-133">Specifica la porta del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="bc475-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="bc475-134">-Probe</span><span class="sxs-lookup"><span data-stu-id="bc475-134">-Probe</span></span>
<span data-ttu-id="bc475-135">Specifica una sonda da associare al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="bc475-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="bc475-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="bc475-136">-ProbeId</span></span>
<span data-ttu-id="bc475-137">Specifica l'ID del Probe da associare al pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="bc475-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="bc475-138">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="bc475-138">-Protocol</span></span>
<span data-ttu-id="bc475-139">Specifica il protocollo da usare per la comunicazione tra il gateway dell'applicazione e i server back-end.</span><span class="sxs-lookup"><span data-stu-id="bc475-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="bc475-140">I valori accettabili per questo parametro sono: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bc475-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="bc475-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="bc475-141">-RequestTimeout</span></span>
<span data-ttu-id="bc475-142">Specifica un valore di timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="bc475-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="bc475-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bc475-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="bc475-144">Certificati radice attendibili del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="bc475-144">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="bc475-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc475-145">CommonParameters</span></span>
<span data-ttu-id="bc475-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc475-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc475-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc475-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc475-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc475-148">INPUTS</span></span>

### <span data-ttu-id="bc475-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bc475-149">None</span></span>

## <span data-ttu-id="bc475-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc475-150">OUTPUTS</span></span>

### <span data-ttu-id="bc475-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bc475-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="bc475-152">Note</span><span class="sxs-lookup"><span data-stu-id="bc475-152">NOTES</span></span>

## <span data-ttu-id="bc475-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc475-153">RELATED LINKS</span></span>

[<span data-ttu-id="bc475-154">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bc475-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="bc475-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bc475-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="bc475-156">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bc475-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="bc475-157">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bc475-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

