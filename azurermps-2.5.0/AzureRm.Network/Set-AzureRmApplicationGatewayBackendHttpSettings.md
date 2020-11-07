---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: c20faf9ca89892d952d553d0f85cfa28b90ac590
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866234"
---
# <span data-ttu-id="c9fb7-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c9fb7-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c9fb7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="c9fb7-103">Aggiorna le impostazioni HTTP di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9fb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9fb7-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9fb7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9fb7-105">DESCRIPTION</span></span>
<span data-ttu-id="c9fb7-106">Il cmdlet Set-AzureRmApplicationGatewayBackendHttpSettings aggiorna le impostazioni HTTP (back-end Hypertext Transfer Protocol) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="c9fb7-107">Le impostazioni HTTP di back-end vengono applicate a tutti i server back-end in un pool.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="c9fb7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9fb7-108">EXAMPLES</span></span>

### <span data-ttu-id="c9fb7-109">Esempio 1: aggiornare le impostazioni HTTP di back-end per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c9fb7-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="c9fb7-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c9fb7-111">Il secondo comando Aggiorna le impostazioni HTTP del gateway dell'applicazione nella variabile $AppGw per usare la porta 88, il protocollo HTTP e consente l'affinità basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="c9fb7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9fb7-112">PARAMETERS</span></span>

### <span data-ttu-id="c9fb7-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="c9fb7-113">-AffinityCookieName</span></span>
<span data-ttu-id="c9fb7-114">Nome del cookie da usare per il cookie di affinità</span><span class="sxs-lookup"><span data-stu-id="c9fb7-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="c9fb7-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9fb7-115">-ApplicationGateway</span></span>
<span data-ttu-id="c9fb7-116">Specifica un oggetto gateway dell'applicazione con cui questo cmdlet associa le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="c9fb7-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="c9fb7-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="c9fb7-118">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="c9fb7-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c9fb7-119">-ConnectionDraining</span></span>
<span data-ttu-id="c9fb7-120">Connessione che svuota la risorsa delle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="c9fb7-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="c9fb7-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="c9fb7-122">Specifica se l'affinità basata su cookie deve essere abilitata o disabilitata per il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="c9fb7-123">I valori accettabili per questo parametro sono: Disabled o Enabled.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="c9fb7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9fb7-124">-DefaultProfile</span></span>
<span data-ttu-id="c9fb7-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9fb7-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="c9fb7-126">-HostName</span></span>
<span data-ttu-id="c9fb7-127">Imposta l'intestazione host da inviare ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="c9fb7-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9fb7-128">-Name</span></span>
<span data-ttu-id="c9fb7-129">Specifica il nome dell'oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="c9fb7-130">-Path</span><span class="sxs-lookup"><span data-stu-id="c9fb7-130">-Path</span></span>
<span data-ttu-id="c9fb7-131">Percorso che deve essere usato come prefisso per tutte le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="c9fb7-132">Se per questo parametro non viene specificato alcun valore, non verrà preceduto alcun percorso.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="c9fb7-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="c9fb7-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="c9fb7-134">Contrassegna se l'intestazione host deve essere selezionata dal nome host del server back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="c9fb7-135">-Porta</span><span class="sxs-lookup"><span data-stu-id="c9fb7-135">-Port</span></span>
<span data-ttu-id="c9fb7-136">Specifica la porta da usare per ogni server nel pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="c9fb7-137">-Probe</span><span class="sxs-lookup"><span data-stu-id="c9fb7-137">-Probe</span></span>
<span data-ttu-id="c9fb7-138">Specifica una sonda da associare alle impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="c9fb7-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="c9fb7-139">-ProbeEnabled</span></span>
<span data-ttu-id="c9fb7-140">Contrassegno se la sonda deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="c9fb7-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c9fb7-141">-ProbeId</span></span>
<span data-ttu-id="c9fb7-142">Specifica l'ID del Probe da associare alle impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="c9fb7-143">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c9fb7-143">-Protocol</span></span>
<span data-ttu-id="c9fb7-144">Specifica il protocollo da usare per la comunicazione tra il gateway dell'applicazione e i server back-end.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="c9fb7-145">I valori accettabili per questo parametro sono: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="c9fb7-146">Questo parametro fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-146">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="c9fb7-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="c9fb7-147">-RequestTimeout</span></span>
<span data-ttu-id="c9fb7-148">Specifica un valore di timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-148">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="c9fb7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fb7-149">CommonParameters</span></span>
<span data-ttu-id="c9fb7-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9fb7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fb7-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9fb7-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fb7-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9fb7-152">INPUTS</span></span>

### <span data-ttu-id="c9fb7-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c9fb7-153">System.String</span></span>

## <span data-ttu-id="c9fb7-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9fb7-154">OUTPUTS</span></span>

### <span data-ttu-id="c9fb7-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9fb7-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9fb7-156">Note</span><span class="sxs-lookup"><span data-stu-id="c9fb7-156">NOTES</span></span>

## <span data-ttu-id="c9fb7-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9fb7-157">RELATED LINKS</span></span>

[<span data-ttu-id="c9fb7-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c9fb7-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c9fb7-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c9fb7-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c9fb7-160">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c9fb7-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c9fb7-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c9fb7-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

