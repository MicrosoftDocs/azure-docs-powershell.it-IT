---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 385a77c2b7b11d20b3ffb8d3728720b46c431d4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982526"
---
# <span data-ttu-id="f1e04-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f1e04-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="f1e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e04-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e04-103">Aggiunge un codice di integrità a un Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f1e04-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="f1e04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1e04-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1e04-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f1e04-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e04-106">Il cmdlet Add-AzApplicationGatewayProbeConfig aggiunge una codice di integrità a un Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f1e04-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="f1e04-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1e04-107">EXAMPLES</span></span>

### <span data-ttu-id="f1e04-108">Esempio 1: Aggiungere una protezione dell'integrità a un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="f1e04-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="f1e04-109">Questo comando consente di aggiungere un nome di integrità Denominato Gateway01 per il gateway applicazione denominato Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1e04-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="f1e04-110">Il comando imposta anche la soglia non integra su 8 tentativi e il timeout dopo 120 secondi.</span><span class="sxs-lookup"><span data-stu-id="f1e04-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="f1e04-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1e04-111">PARAMETERS</span></span>

### <span data-ttu-id="f1e04-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1e04-112">-ApplicationGateway</span></span>
<span data-ttu-id="f1e04-113">Specifica il gateway applicazione a cui questo cmdlet aggiunge un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1e04-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="f1e04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e04-114">-DefaultProfile</span></span>
<span data-ttu-id="f1e04-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1e04-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1e04-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="f1e04-116">-HostName</span></span>
<span data-ttu-id="f1e04-117">Specifica il nome host a cui il cmdlet invia il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1e04-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="f1e04-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="f1e04-118">-Interval</span></span>
<span data-ttu-id="f1e04-119">Specifica l'intervallo in secondi.</span><span class="sxs-lookup"><span data-stu-id="f1e04-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="f1e04-120">L'intervallo di tempo che si trova tra due gruppi consecutivi.</span><span class="sxs-lookup"><span data-stu-id="f1e04-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="f1e04-121">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="f1e04-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="f1e04-122">-Match</span><span class="sxs-lookup"><span data-stu-id="f1e04-122">-Match</span></span>
<span data-ttu-id="f1e04-123">Corpo che deve essere contenuto nella risposta all'integrità.</span><span class="sxs-lookup"><span data-stu-id="f1e04-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="f1e04-124">Il valore predefinito è vuoto</span><span class="sxs-lookup"><span data-stu-id="f1e04-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e04-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="f1e04-125">-MinServers</span></span>
<span data-ttu-id="f1e04-126">Numero minimo di server contrassegnati sempre come integri.</span><span class="sxs-lookup"><span data-stu-id="f1e04-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="f1e04-127">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="f1e04-127">Default value is 0</span></span>

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

### <span data-ttu-id="f1e04-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f1e04-128">-Name</span></span>
<span data-ttu-id="f1e04-129">Specifica il nome della società.</span><span class="sxs-lookup"><span data-stu-id="f1e04-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="f1e04-130">-Path</span><span class="sxs-lookup"><span data-stu-id="f1e04-130">-Path</span></span>
<span data-ttu-id="f1e04-131">Specifica il percorso relativo di un file.</span><span class="sxs-lookup"><span data-stu-id="f1e04-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="f1e04-132">Percorso valido che inizia con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="f1e04-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="f1e04-133">Il file viene inviato a \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="f1e04-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="f1e04-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f1e04-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="f1e04-135">Se l'intestazione host deve essere selezionata dalle impostazioni http back-end.</span><span class="sxs-lookup"><span data-stu-id="f1e04-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="f1e04-136">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="f1e04-136">Default value is false</span></span>

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

### <span data-ttu-id="f1e04-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f1e04-137">-Protocol</span></span>
<span data-ttu-id="f1e04-138">Specifica il protocollo usato per inviare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="f1e04-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="f1e04-139">Questo cmdlet supporta solo HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1e04-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="f1e04-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="f1e04-140">-Timeout</span></span>
<span data-ttu-id="f1e04-141">Specifica il timeout in secondi.</span><span class="sxs-lookup"><span data-stu-id="f1e04-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="f1e04-142">Questo cmdlet contrassegna il messaggio come non riuscito se non si riceve una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="f1e04-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="f1e04-143">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="f1e04-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="f1e04-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="f1e04-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="f1e04-145">Specifica il numero di tentativi.</span><span class="sxs-lookup"><span data-stu-id="f1e04-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="f1e04-146">Il server back-end viene contrassegnato in modo non attivo dopo che il numero di errori imprevisti consecutivi raggiunge la soglia non integra.</span><span class="sxs-lookup"><span data-stu-id="f1e04-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="f1e04-147">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="f1e04-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="f1e04-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e04-148">CommonParameters</span></span>
<span data-ttu-id="f1e04-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e04-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e04-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e04-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e04-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="f1e04-151">INPUTS</span></span>

### <span data-ttu-id="f1e04-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1e04-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1e04-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1e04-153">OUTPUTS</span></span>

### <span data-ttu-id="f1e04-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1e04-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1e04-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="f1e04-155">NOTES</span></span>

## <span data-ttu-id="f1e04-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1e04-156">RELATED LINKS</span></span>

[<span data-ttu-id="f1e04-157">Aggiungere un modello a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="f1e04-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="f1e04-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f1e04-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f1e04-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f1e04-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f1e04-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f1e04-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f1e04-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f1e04-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

