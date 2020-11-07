---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 3696b33b18314d58e950fa9786e1febac5c3d22c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862854"
---
# <span data-ttu-id="67b81-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67b81-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="67b81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67b81-102">SYNOPSIS</span></span>
<span data-ttu-id="67b81-103">Aggiorna le impostazioni HTTP di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67b81-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="67b81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67b81-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67b81-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67b81-105">DESCRIPTION</span></span>
<span data-ttu-id="67b81-106">Il cmdlet Set-AzApplicationGatewayBackendHttpSetting aggiorna le impostazioni HTTP (back-end Hypertext Transfer Protocol) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="67b81-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="67b81-107">Le impostazioni HTTP di back-end vengono applicate a tutti i server back-end in un pool.</span><span class="sxs-lookup"><span data-stu-id="67b81-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="67b81-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67b81-108">EXAMPLES</span></span>

### <span data-ttu-id="67b81-109">Esempio 1: aggiornare le impostazioni HTTP di back-end per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="67b81-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="67b81-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="67b81-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="67b81-111">Il secondo comando Aggiorna le impostazioni HTTP del gateway dell'applicazione nella variabile $AppGw per usare la porta 88, il protocollo HTTP e consente l'affinità basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="67b81-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="67b81-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67b81-112">PARAMETERS</span></span>

### <span data-ttu-id="67b81-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="67b81-113">-AffinityCookieName</span></span>
<span data-ttu-id="67b81-114">Nome del cookie da usare per il cookie di affinità</span><span class="sxs-lookup"><span data-stu-id="67b81-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="67b81-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67b81-115">-ApplicationGateway</span></span>
<span data-ttu-id="67b81-116">Specifica un oggetto gateway dell'applicazione con cui questo cmdlet associa le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="67b81-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="67b81-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="67b81-118">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67b81-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="67b81-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="67b81-119">-ConnectionDraining</span></span>
<span data-ttu-id="67b81-120">Connessione che svuota la risorsa delle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="67b81-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="67b81-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="67b81-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="67b81-122">Specifica se l'affinità basata su cookie deve essere abilitata o disabilitata per il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="67b81-123">I valori accettabili per questo parametro sono: Disabled o Enabled.</span><span class="sxs-lookup"><span data-stu-id="67b81-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="67b81-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b81-124">-DefaultProfile</span></span>
<span data-ttu-id="67b81-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67b81-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67b81-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="67b81-126">-HostName</span></span>
<span data-ttu-id="67b81-127">Imposta l'intestazione host da inviare ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="67b81-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="67b81-128">-Name</span></span>
<span data-ttu-id="67b81-129">Specifica il nome dell'oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="67b81-130">-Path</span><span class="sxs-lookup"><span data-stu-id="67b81-130">-Path</span></span>
<span data-ttu-id="67b81-131">Percorso che deve essere usato come prefisso per tutte le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="67b81-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="67b81-132">Se per questo parametro non viene specificato alcun valore, non verrà preceduto alcun percorso.</span><span class="sxs-lookup"><span data-stu-id="67b81-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="67b81-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="67b81-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="67b81-134">Contrassegna se l'intestazione host deve essere selezionata dal nome host del server back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="67b81-135">-Porta</span><span class="sxs-lookup"><span data-stu-id="67b81-135">-Port</span></span>
<span data-ttu-id="67b81-136">Specifica la porta da usare per ogni server nel pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="67b81-137">-Probe</span><span class="sxs-lookup"><span data-stu-id="67b81-137">-Probe</span></span>
<span data-ttu-id="67b81-138">Specifica una sonda da associare alle impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="67b81-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="67b81-139">-ProbeEnabled</span></span>
<span data-ttu-id="67b81-140">Contrassegno se la sonda deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="67b81-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="67b81-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="67b81-141">-ProbeId</span></span>
<span data-ttu-id="67b81-142">Specifica l'ID del Probe da associare alle impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="67b81-143">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="67b81-143">-Protocol</span></span>
<span data-ttu-id="67b81-144">Specifica il protocollo da usare per la comunicazione tra il gateway dell'applicazione e i server back-end.</span><span class="sxs-lookup"><span data-stu-id="67b81-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="67b81-145">I valori accettabili per questo parametro sono: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="67b81-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="67b81-146">Questo parametro fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="67b81-146">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="67b81-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="67b81-147">-RequestTimeout</span></span>
<span data-ttu-id="67b81-148">Specifica un valore di timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="67b81-148">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="67b81-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b81-149">CommonParameters</span></span>
<span data-ttu-id="67b81-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b81-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b81-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b81-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b81-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67b81-152">INPUTS</span></span>

### <span data-ttu-id="67b81-153">System. String</span><span class="sxs-lookup"><span data-stu-id="67b81-153">System.String</span></span>

## <span data-ttu-id="67b81-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67b81-154">OUTPUTS</span></span>

### <span data-ttu-id="67b81-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67b81-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="67b81-156">Note</span><span class="sxs-lookup"><span data-stu-id="67b81-156">NOTES</span></span>

## <span data-ttu-id="67b81-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67b81-157">RELATED LINKS</span></span>

[<span data-ttu-id="67b81-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67b81-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="67b81-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67b81-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="67b81-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67b81-160">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="67b81-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67b81-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

