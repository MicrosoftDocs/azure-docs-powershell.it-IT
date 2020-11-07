---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 25db1c941975111cdf000ce142519e90f08cd101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678697"
---
# <span data-ttu-id="9c5c8-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9c5c8-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="9c5c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5c8-103">Aggiunge una sonda di integrità a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="9c5c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c5c8-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c5c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="9c5c8-106">Il cmdlet Add-AzApplicationGatewayProbeConfig aggiunge una sonda di integrità a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="9c5c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="9c5c8-108">Esempio 1: aggiungere una sonda di integrità a un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="9c5c8-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="9c5c8-109">Questo comando aggiunge una sonda di integrità denominata Probe01 per il gateway dell'applicazione denominato gateway.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="9c5c8-110">Il comando imposta anche la soglia non sana su 8 tentativi e timeout dopo 120 secondi.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="9c5c8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c5c8-111">PARAMETERS</span></span>

### <span data-ttu-id="9c5c8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c5c8-112">-ApplicationGateway</span></span>
<span data-ttu-id="9c5c8-113">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge un probe.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="9c5c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5c8-114">-DefaultProfile</span></span>
<span data-ttu-id="9c5c8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c5c8-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="9c5c8-116">-HostName</span></span>
<span data-ttu-id="9c5c8-117">Specifica il nome host a cui il cmdlet invia il probe.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="9c5c8-118">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="9c5c8-118">-Interval</span></span>
<span data-ttu-id="9c5c8-119">Specifica l'intervallo di probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="9c5c8-120">Questo è l'intervallo di tempo tra due sonde consecutive.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="9c5c8-121">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="9c5c8-122">-Match</span><span class="sxs-lookup"><span data-stu-id="9c5c8-122">-Match</span></span>
<span data-ttu-id="9c5c8-123">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="9c5c8-124">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="9c5c8-124">Default value is empty</span></span>

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

### <span data-ttu-id="9c5c8-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="9c5c8-125">-MinServers</span></span>
<span data-ttu-id="9c5c8-126">Numero minimo di server sempre contrassegnati come integri.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="9c5c8-127">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="9c5c8-127">Default value is 0</span></span>

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

### <span data-ttu-id="9c5c8-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c5c8-128">-Name</span></span>
<span data-ttu-id="9c5c8-129">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="9c5c8-130">-Path</span><span class="sxs-lookup"><span data-stu-id="9c5c8-130">-Path</span></span>
<span data-ttu-id="9c5c8-131">Specifica il percorso relativo di probe.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="9c5c8-132">Il percorso valido inizia con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="9c5c8-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="9c5c8-133">Il probe viene inviato al \< protocollo \> :// \< host \> : Path della \< porta \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="9c5c8-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="9c5c8-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9c5c8-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="9c5c8-135">Se l'intestazione host deve essere selezionata dalle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="9c5c8-136">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="9c5c8-136">Default value is false</span></span>

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

### <span data-ttu-id="9c5c8-137">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="9c5c8-137">-Protocol</span></span>
<span data-ttu-id="9c5c8-138">Specifica il protocollo usato per inviare Probe.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="9c5c8-139">Questo cmdlet supporta solo HTTP.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="9c5c8-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="9c5c8-140">-Timeout</span></span>
<span data-ttu-id="9c5c8-141">Specifica il timeout del probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="9c5c8-142">Questo cmdlet contrassegna la sonda come non riuscita se non viene ricevuta una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="9c5c8-143">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="9c5c8-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="9c5c8-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="9c5c8-145">Specifica il numero di tentativi di probe.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="9c5c8-146">Il server back-end viene contrassegnato in basso dopo il conteggio errori consecutivi Probe raggiunge la soglia non sana.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="9c5c8-147">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="9c5c8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5c8-148">CommonParameters</span></span>
<span data-ttu-id="9c5c8-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5c8-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5c8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5c8-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c5c8-151">INPUTS</span></span>

### <span data-ttu-id="9c5c8-152">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c5c8-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c5c8-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c5c8-153">OUTPUTS</span></span>

### <span data-ttu-id="9c5c8-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c5c8-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c5c8-155">Note</span><span class="sxs-lookup"><span data-stu-id="9c5c8-155">NOTES</span></span>

## <span data-ttu-id="9c5c8-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c5c8-156">RELATED LINKS</span></span>

[<span data-ttu-id="9c5c8-157">Aggiungere una sonda a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="9c5c8-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="9c5c8-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9c5c8-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="9c5c8-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9c5c8-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="9c5c8-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9c5c8-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="9c5c8-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9c5c8-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)
